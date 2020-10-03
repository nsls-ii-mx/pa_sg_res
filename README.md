pa_sg_res
    by Wuxian Shi, 13 Feb 2017
    adapted to keyword arguments by H. J. Bernstein
    window args added by D. Kreitler
    merged with ps_sg_res_cut by H. J. Bernstein

pa_sg_res [-1<first_frame>] [-N<frame_cutoff>] [-R<reslow>] [-r<reshigh>]
   [-S<spacegroup>] [-i<infile>] [-o<outfile>] [-l<logfile>]

 -h produces a short help messaage< --help produces this help message

pa_sg_res is a bash shell script wrapper for aimless and pointless, for
the downstream processing of fast_dp output. This script allows for trimming
integrated reflection files (from XDS) based on resolution and frame number
in addition to spacegroup assignment/enforcement.

Caveat: The impact of crystal misalignment and/or unreliable indexing in the
first few frames of data collection may still be present even if those frames
are excluded from pointless/aimless. In such cases re-running fast_dp is
recommended.

Input arg variables match those of fast_dp (where overlap occurs)
Input arg variables changed to match pa_sg_res_cut (N for f, swap r and R)

infile defaults to XDS_ASCII.HKL, outfile to aimless.mtz
logfile in pa_sg_res.log

