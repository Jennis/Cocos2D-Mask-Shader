#Cocos2D-Mask-Shader
======================

##Mask sprite with OpenGL ES 2.0 shader in Cocos2D
(Adapted from <https://github.com/HarrisonJackson/Cocos2D-HJMasked-Sprite>)

Getting started :

* Copy the files of the src folder into your project;
* Don't forget to add the .fsh files to the "Copy Bundles Resources" in "Build Phases" tab;
* Make sure that the .fsh files are not in the "Compile Sources";

![Cocos2D-Mask-Shader - preview](https://raw.github.com/tonybeltramelli/Cocos2D-Mask-Shader/master/ShaderMask/Resources/preview.jpg)

Usage :
```objc
		// EXAMPLES MaskNegative
        //
        // example 1
        
        CCSprite *spriteToMask = [CCSprite spriteWithFile:@"image_to_mask.jpg"];
        CCSprite *spriteMask = [CCSprite spriteWithFile:@"mask.png"];
        
        TBSpriteMask *maskedSprite = [[TBSpriteMask alloc] initWithSprite:spriteMask andMaskSprite:spriteToMask];
        [self addChild:maskedSprite];
        
        // example 2
        
        CCSprite *spriteMask = [CCSprite spriteWithFile:@"mask.png"];
        
        TBSpriteMask *maskedSprite = [[TBSpriteMask alloc] initWithSprite:spriteMask andMaskFile:@"image_to_mask.jpg"];
        [self addChild:maskedSprite];
        
        // example 3
        
        CCSprite *spriteToMask = [CCSprite spriteWithFile:@"image_to_mask.jpg"];
        
        TBSpriteMask *maskedSprite = [[TBSpriteMask alloc] initWithFile:@"mask.png" andMaskSprite:spriteToMask];
        [self addChild:maskedSprite];
        
        // example 4
        
        TBSpriteMask *maskedSprite = [[TBSpriteMask alloc] initWithFile:@"mask.png" andMaskFile:@"image_to_mask.jpg"];
        [self addChild:maskedSprite];
        
        //
        // EXAMPLES MaskPositive
        //
        // example 1
        
        CCSprite *spriteToMask = [CCSprite spriteWithFile:@"image_to_mask.jpg"];
        CCSprite *spriteMask = [CCSprite spriteWithFile:@"mask.png"];
         
        TBSpriteMask *maskedSprite = [[TBSpriteMask alloc] initWithSprite:spriteMask andMaskSprite:spriteToMask andType:TRUE];
        [self addChild:maskedSprite];
        
        // example 2
        
        CCSprite *spriteMask = [CCSprite spriteWithFile:@"mask.png"];
         
        TBSpriteMask *maskedSprite = [[TBSpriteMask alloc] initWithSprite:spriteMask andMaskFile:@"image_to_mask.jpg" andType:TRUE];
        [self addChild:maskedSprite];
        
        // example 3
        
        CCSprite *spriteToMask = [CCSprite spriteWithFile:@"image_to_mask.jpg"];
         
        TBSpriteMask *maskedSprite = [[TBSpriteMask alloc] initWithFile:@"mask.png" andMaskSprite:spriteToMask andType:TRUE];
        [self addChild:maskedSprite];
         
        // example 4
        
        TBSpriteMask *maskedSprite = [[TBSpriteMask alloc] initWithFile:@"mask.png" andMaskFile:@"image_to_mask.jpg" andType:TRUE];
        [self addChild:maskedSprite];
        
        //
        // EXAMPLES update
        //
        // example 1
        
        CCSprite *spriteMask = [CCSprite spriteWithFile:@"mask.png"];
        [maskedSprite updateWithSprite:spriteMask];
        
        // example 2
        
        [maskedSprite updateWithFile:@"mask.png"];
```

Have fun !
@Tbeltramelli <http://twitter.com/#!/tbeltramelli/>