---
description: Fusione alfa di una bitmap
ms.assetid: 01ed3e2e-cfb3-42c9-9030-b64f9db088f1
title: Fusione alfa di una bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54870ccf13ec27b982669dc43382c357a932ea9052e5855200f27825ab96eb35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038299"
---
# <a name="alpha-blending-a-bitmap"></a>Fusione alfa di una bitmap

Nell'esempio di codice seguente una finestra viene suddivisa in tre aree orizzontali. Disegna quindi una bitmap con sfumatura alfa in ognuna delle aree della finestra come indicato di seguito:

-   Nell'area superiore, alfa costante = 50%, ma non è presente alcun alfa di origine.
-   Nell'area centrale, la costante alpha = 100% (disabilitata) e il valore alfa di origine è 0 (trasparente) al centro della bitmap e 0xff (opaco) altrove.
-   Nell'area inferiore, la costante alpha = 75% e il valore alfa di origine cambiano.


```C++
void DrawAlphaBlend (HWND hWnd, HDC hdcwnd)
{
    HDC hdc;               // handle of the DC we will create  
    BLENDFUNCTION bf;      // structure for alpha blending 
    HBITMAP hbitmap;       // bitmap handle 
    BITMAPINFO bmi;        // bitmap header 
    VOID *pvBits;          // pointer to DIB section 
    ULONG   ulWindowWidth, ulWindowHeight;      // window width/height 
    ULONG   ulBitmapWidth, ulBitmapHeight;      // bitmap width/height 
    RECT    rt;            // used for getting window dimensions 
    UINT32   x,y;          // stepping variables 
    UCHAR ubAlpha;         // used for doing transparent gradient 
    UCHAR ubRed;        
    UCHAR ubGreen;
    UCHAR ubBlue;
    float fAlphaFactor;    // used to do premultiply 
            
    // get window dimensions 
    GetClientRect(hWnd, &rt);
    
    // calculate window width/height 
    ulWindowWidth = rt.right - rt.left;  
    ulWindowHeight = rt.bottom - rt.top;  

    // make sure we have at least some window size 
    if ((!ulWindowWidth) || (!ulWindowHeight))
        return;

    // divide the window into 3 horizontal areas 
    ulWindowHeight = ulWindowHeight / 3;

    // create a DC for our bitmap -- the source DC for AlphaBlend  
    hdc = CreateCompatibleDC(hdcwnd);
    
    // zero the memory for the bitmap info 
    ZeroMemory(&bmi, sizeof(BITMAPINFO));

    // setup bitmap info  
    // set the bitmap width and height to 60% of the width and height of each of the three horizontal areas. Later on, the blending will occur in the center of each of the three areas. 
    bmi.bmiHeader.biSize = sizeof(BITMAPINFOHEADER);
    bmi.bmiHeader.biWidth = ulBitmapWidth = ulWindowWidth - (ulWindowWidth/5)*2;
    bmi.bmiHeader.biHeight = ulBitmapHeight = ulWindowHeight - (ulWindowHeight/5)*2;
    bmi.bmiHeader.biPlanes = 1;
    bmi.bmiHeader.biBitCount = 32;         // four 8-bit components 
    bmi.bmiHeader.biCompression = BI_RGB;
    bmi.bmiHeader.biSizeImage = ulBitmapWidth * ulBitmapHeight * 4;

    // create our DIB section and select the bitmap into the dc 
    hbitmap = CreateDIBSection(hdc, &bmi, DIB_RGB_COLORS, &pvBits, NULL, 0x0);
    SelectObject(hdc, hbitmap);

    // in top window area, constant alpha = 50%, but no source alpha 
    // the color format for each pixel is 0xaarrggbb  
    // set all pixels to blue and set source alpha to zero 
    for (y = 0; y < ulBitmapHeight; y++)
        for (x = 0; x < ulBitmapWidth; x++)
            ((UINT32 *)pvBits)[x + y * ulBitmapWidth] = 0x000000ff; 

    bf.BlendOp = AC_SRC_OVER;
    bf.BlendFlags = 0;
    bf.SourceConstantAlpha = 0x7f;  // half of 0xff = 50% transparency 
    bf.AlphaFormat = 0;             // ignore source alpha channel 

    if (!AlphaBlend(hdcwnd, ulWindowWidth/5, ulWindowHeight/5, 
                    ulBitmapWidth, ulBitmapHeight, 
                    hdc, 0, 0, ulBitmapWidth, ulBitmapHeight, bf))
        return;                     // alpha blend failed 
    
    // in middle window area, constant alpha = 100% (disabled), source  
    // alpha is 0 in middle of bitmap and opaque in rest of bitmap  
    for (y = 0; y < ulBitmapHeight; y++)
        for (x = 0; x < ulBitmapWidth; x++)
            if ((x > (int)(ulBitmapWidth/5)) && (x < (ulBitmapWidth-ulBitmapWidth/5)) &&
                (y > (int)(ulBitmapHeight/5)) && (y < (ulBitmapHeight-ulBitmapHeight/5)))
                //in middle of bitmap: source alpha = 0 (transparent). 
                // This means multiply each color component by 0x00. 
                // Thus, after AlphaBlend, we have a, 0x00 * r,  
                // 0x00 * g,and 0x00 * b (which is 0x00000000) 
                // for now, set all pixels to red 
                ((UINT32 *)pvBits)[x + y * ulBitmapWidth] = 0x00ff0000; 
            else
                // in the rest of bitmap, source alpha = 0xff (opaque)  
                // and set all pixels to blue  
                ((UINT32 *)pvBits)[x + y * ulBitmapWidth] = 0xff0000ff; 
            endif;
    
    bf.BlendOp = AC_SRC_OVER;
    bf.BlendFlags = 0;
    bf.AlphaFormat = AC_SRC_ALPHA;  // use source alpha  
    bf.SourceConstantAlpha = 0xff;  // opaque (disable constant alpha) 
   
    if (!AlphaBlend(hdcwnd, ulWindowWidth/5, ulWindowHeight/5+ulWindowHeight, ulBitmapWidth, ulBitmapHeight, hdc, 0, 0, ulBitmapWidth, ulBitmapHeight, bf))
        return;

    // bottom window area, use constant alpha = 75% and a changing 
    // source alpha. Create a gradient effect using source alpha, and  
    // then fade it even more with constant alpha 
    ubRed = 0x00;
    ubGreen = 0x00;
    ubBlue = 0xff;
    
    for (y = 0; y < ulBitmapHeight; y++)
        for (x = 0; x < ulBitmapWidth; x++)
        {
            // for a simple gradient, base the alpha value on the x  
            // value of the pixel  
            ubAlpha = (UCHAR)((float)x / (float)ulBitmapWidth * 255);
            //calculate the factor by which we multiply each component 
            fAlphaFactor = (float)ubAlpha / (float)0xff; 
            // multiply each pixel by fAlphaFactor, so each component  
            // is less than or equal to the alpha value. 
            ((UINT32 *)pvBits)[x + y * ulBitmapWidth] 
                = (ubAlpha << 24) |                       //0xaa000000 
                 ((UCHAR)(ubRed * fAlphaFactor) << 16) |  //0x00rr0000 
                 ((UCHAR)(ubGreen * fAlphaFactor) << 8) | //0x0000gg00 
                 ((UCHAR)(ubBlue   * fAlphaFactor));      //0x000000bb 
        }

    bf.BlendOp = AC_SRC_OVER;
    bf.BlendFlags = 0;
    bf.AlphaFormat = AC_SRC_ALPHA;   // use source alpha  
    bf.SourceConstantAlpha = 0xbf;   // use constant alpha, with  
                                     // 75% opaqueness 

    AlphaBlend(hdcwnd, ulWindowWidth/5, 
               ulWindowHeight/5+2*ulWindowHeight, ulBitmapWidth, 
               ulBitmapHeight, hdc, 0, 0, ulBitmapWidth, 
               ulBitmapHeight, bf);

    // do cleanup 
    DeleteObject(hbitmap);
    DeleteDC(hdc);
    
}
```



 

 



