Scallion as a Service
=====================

I am now offering to generate vanity onion addresses using Scallion's [secure remote generation](README.md#SRKG) feature as a service to you, the GPU-less user. The secure remote generation feature only requires CPU time. If you're interested, please contact me at ```scallion@aftbit.com```.

Cost Breakdown
--------------

| Length | Cost                                               | My Time    | Pubkeys Needed | Your Time    | Pubkey File Size |
|:------:|:--------------------------------------------------:|:----------:|:--------------:|:------------:|:----------------:|
| 1-6    | Use [shallot](https://github.com/katmagic/Shallot) |            |                | < 5 minutes  |                  |
| 7      | 0.001 BTC (note 1)                                 | 30 seconds | 80             | 5 seconds    | 25 KB            |
| 8      | 0.01 BTC (note 1)                                  | 20 minutes | 2580           | 1 minute     | 800 KB           |
| 9      | 0.1 BTC                                            | 10 hours   | 82565          | 28 minutes   | 28 MB            |
| 10     | 4.0 BTC                                            | 14 days    | 2642160        | 15 hours     | 780 MB           |
| 11     | Forget about it                                    | 400 days   | 84549200       | 20 days      | 24 GB            |

Note 1: For the 7 and 8 length prefixes, I'll accept an original dirty limerick (somehow featuring Tor) in lieu of Bitcoins.

The My Time values are averages. As Scallion is probabilistic, it could take any amount of time. If I don't find an address matching your pattern, I will certainly refund your payment.

If you supply multiple patterns, the times, keys, and storage required decrease linearly with the number of patterns. Consequently, the cost decreases linearly as well. This applies to regexp patterns as well.
If you supply patterns of different lengths, you'll be charged for the shortest one (and almost certainly receive a hash matching the shortest pattern).

For example, the pattern `scallion2` would cost 0.1BTC and take me ~10 hours to generate and ~28 MB of pubkey storage. The pattern `scallion[234567]`, however, would cost 0.017 BTC and take only ~1.7 hours to generate and ~6 MB of public key storage.

The "Your Time" estimates are all based around a quad-core i7 (although Scallion's key generation code is currently single threaded, so it could be up to 4x faster if and when I implement that.
Total file storage requirements will be approximately 4x the amount shown here, as you need to keep a database of private keys as well. These files are somewhat compressible, achieving a total size of about 70% of what is shown here.

