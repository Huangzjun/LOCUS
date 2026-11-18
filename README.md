# LOCUS: Causal Support Windows for Attribute Control in Autoregressive Image Generation

Unified autoregressive image generators often miss object attributes when one prompt binds several of them at once. These attributes can be read from the image-token latents, but editing the latents at test time is unreliable: a fixed direction added at the prefix can reinforce an attribute the prompt already asks for, and rarely override a conflicting one.

LOCUS measures, for each attribute, where along the image-token sequence an intervention can still change what is rendered. Structural attributes (count and position) respond in early, narrow windows. Appearance attributes (color, size, and material) respond later, over broader windows, and the responsive region follows the object rather than raster order. Given a failed generation, LOCUS routes test-time latent optimization to the failed attribute's window. The generator stays frozen.

Code coming soon.
