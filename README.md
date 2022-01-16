# Deep-Rock-Galactic-ray-tracing

Added RGTI profile for Deep Rock Galactic as below.
Example slide shots (opens in new tab): <a href="https://imgsli.com/OTExODk" target="_blank">(link)</a>, <a href="https://imgsli.com/OTExOTA" target="_blank">(link)</a>, <a href="https://imgsli.com/OTExOTE"  target="_blank">(link)</a>, <a href="https://imgsli.com/OTExOTM" target="_blank">(link)</a>, <a href="https://imgsli.com/OTExOTQ" target="_blank">(link)</a>, <a href="https://imgsli.com/OTExOTU" target="_blank">(link)</a>, <a href="https://imgsli.com/OTExOTY" target="_blank">(link)</a>, <a href="https://imgsli.com/OTExODc" target="_blank">(link)</a>, <a href="https://imgsli.com/OTExODg" target="_blank">(link)</a>

See PSO example for full details, this is just the difference for this game.

```
ReShade.ini:
PreprocessorDefinitions=RESHADE_DEPTH_LINEARIZATION_FAR_PLANE=1000.0,RESHADE_DEPTH_INPUT_IS_UPSIDE_DOWN=0,RESHADE_DEPTH_INPUT_IS_REVERSED=1,RESHADE_DEPTH_INPUT_IS_LOGARITHMIC=0```

DeepRockGalactic_Preset.ini:
PreprocessorDefinitions=MATERIAL_TYPE=1
Techniques=MXAO@qUINT_mxao.fx,RTGlobalIllumination@qUINT_rtgi.fx,DELC_Sharpen@qUINT_sharp.fx
TechniqueSorting=MXAO@qUINT_mxao.fx,Daltonize@Daltonize.fx,UIMask_Top@UIMask.fx,UIMask_Bottom@UIMask.fx,DisplayDepth@DisplayDepth.fx,Debanding@qUINT_deband.fx,SSR@qUINT_ssr.fx,Deband@Deband.fx,LUT@LUT.fx,ADOF@qUINT_dof.fx,Lightroom@qUINT_lightroom.fx,Bloom@qUINT_bloom.fx,RTGlobalIllumination@qUINT_rtgi.fx,DELC_Sharpen@qUINT_sharp.fx

[qUINT_bloom.fx]
BLOOM_ADAPT_EXPOSURE=0.000000
BLOOM_ADAPT_MODE=0
BLOOM_ADAPT_SPEED=1.000000
BLOOM_ADAPT_STRENGTH=0.000000
BLOOM_CURVE=10.000000
BLOOM_INTENSITY=2.500000
BLOOM_LAYER_MULT_1=0.001000
BLOOM_LAYER_MULT_2=0.003000
BLOOM_LAYER_MULT_3=0.000000
BLOOM_LAYER_MULT_4=0.008000
BLOOM_LAYER_MULT_5=0.041000
BLOOM_LAYER_MULT_6=0.092000
BLOOM_LAYER_MULT_7=0.046000
BLOOM_SAT=1.000000
BLOOM_TONEMAP_COMPRESSION=10.000000

[qUINT_mxao.fx]
MXAO_BLEND_TYPE=0
MXAO_DEBUG_VIEW_ENABLE=0
MXAO_FADE_DEPTH_END=1.000000
MXAO_FADE_DEPTH_START=0.000000
MXAO_GLOBAL_RENDER_SCALE=1.000000
MXAO_GLOBAL_SAMPLE_QUALITY_PRESET=3
MXAO_SAMPLE_NORMAL_BIAS=0.402000
MXAO_SAMPLE_RADIUS=5.000000
MXAO_SSAO_AMOUNT=0.500000

[qUINT_rtgi.fx]
FADEOUT_MODE_UI=2
RT_AO_AMOUNT=0.000000
RT_BACKFACE_MIRROR=0
RT_DEBUG_VIEW=0
RT_DO_RENDER=0
RT_FADE_DEPTH=1.000000
RT_HIGHP_LIGHT_SPREAD=1
RT_IL_AMOUNT=10.000000
RT_RAY_AMOUNT=11
RT_RAY_STEPS=26
RT_ROUGHNESS=0.290000
RT_SAMPLE_RADIUS=4.000000
RT_SAMPLE_RADIUS_FAR=0.000000
RT_SPECULAR=0.320000
RT_Z_THICKNESS=0.060000
UIHELP=0
UIHELP2=0

[qUINT_sharp.fx]
DEPTH_MASK_ENABLE=1
RMS_MASK_ENABLE=1
SHARPEN_MODE=1
SHARP_STRENGTH=0.700000
