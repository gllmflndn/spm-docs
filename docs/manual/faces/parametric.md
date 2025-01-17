# Modelling and plotting parametric responses

In addition to analysing the data in the above \"categorical\" design,
we now illustrate an alternative \"parametric\" design in which
repetition is viewed as a continuum. In this case, the response to each
presentation of famous and non-famous faces is modulated by the time
interval (lag) since the previous presentation of that face (for first
presentations, this lag is infinite).

## Specification and estimation

Finally, consider the effects of the interval between first and second
presentations of famous and non-famous faces. For this purpose, an
alternative statistical model needs to be estimated, with four trial
types. (1) First and second presentation of a non-famous face (N1 and N2
collapsed). (2) First and second presentation of a famous face (F1 and
F2 collapsed). (3) Errors in judging non-famous faces. (4) Errors in
judging famous faces. These are modelled with the canonical hrf alone,
with two parametric (exponential) modulations added for second
presentations of non-famous and famous faces. See the README.txt for
details of design specification.

## Inference and plotting

After completion of model estimation, press 'Results' and select the
SPM.mat file. When the Contrast Manager appears, define an F-contrast
'Effect of Lag (on canonical N+F)' (name) and '0 1 0 1', and a
t-contrast 'Canonical: Faces $>$ Baseline' (name) and '1 0 1 0'. Select
the F-contrast, specify 'mask with other contrasts' (yes), select
'Canonical: Faces $>$ Baseline', specify 'uncorrected mask p-value'
(accept default), 'nature of mask (inclusive), 'title for comparison'
(accept default), 'corrected height threshold' (no), and 'corrected
p-value' (accept default). When the MIP appears, press 'Volume'.

The table displays all clusters where the exponential change in
activation between first and second presentations for famous OR
non-famous faces for the canonical hrf is significantly different from
zero AND the canonical hrf for the first two conditions is significantly
larger than zero (baseline). We can now plot these parametric effects at
particular voxels.

To plot these parametric effects, select the R fusiform region (45 -60
-18, similar to the region identified in the previous categorical
analysis for repetition effects), and press 'plot'. Select 'Plots of
parametric responses' and select 'F' (or 'N'). Note that the 'attrib'
option does not allow adjustment of the scale of the Z-axis; therefore,
to change the scale for all axes, type e.g. 'figure (1), axis (\[0 30 0
100 0 1\])' in the Matlab window.

Note that these repetition effects are transient (decrease with
increasing intervals between first and second presentations), especially
for famous faces.
