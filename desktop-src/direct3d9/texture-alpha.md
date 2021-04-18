---
description: I valori alfa possono anche essere forniti dalle trame.
ms.assetid: b9f53783-d4d8-4339-8cf3-5ad8305ff627
title: Trama alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694f8a72d3faede36c3e69ce1b6841b8f6450a3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304369"
---
# <a name="texture-alpha-direct3d-9"></a><span data-ttu-id="83a9b-103">Trama alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="83a9b-103">Texture Alpha (Direct3D 9)</span></span>

<span data-ttu-id="83a9b-104">I valori alfa possono anche essere forniti dalle trame.</span><span class="sxs-lookup"><span data-stu-id="83a9b-104">Alpha values can also be provided by textures.</span></span> <span data-ttu-id="83a9b-105">In primo luogo, è necessario creare la trama.</span><span class="sxs-lookup"><span data-stu-id="83a9b-105">First, the texture must be created.</span></span> <span data-ttu-id="83a9b-106">In secondo luogo, è necessario aggiungere i valori alfa alla trama.</span><span class="sxs-lookup"><span data-stu-id="83a9b-106">Second, the alpha values must be added to the texture.</span></span> <span data-ttu-id="83a9b-107">Per eseguire il rendering con la trama, impostare la trama su una fase della trama e selezionare l'operazione e gli operandi della fase di trama appropriati.</span><span class="sxs-lookup"><span data-stu-id="83a9b-107">To render with the texture, set the texture to a texture stage and select the appropriate texture stage operation and operands.</span></span> <span data-ttu-id="83a9b-108">Quando viene chiamato il metodo di richiamo, viene eseguito il rendering della primitiva con trasparenza.</span><span class="sxs-lookup"><span data-stu-id="83a9b-108">When draw is called, the primitive will be rendered with transparency.</span></span> <span data-ttu-id="83a9b-109">Questo esempio crea una risorsa di trama, quindi carica il canale alfa.</span><span class="sxs-lookup"><span data-stu-id="83a9b-109">This example creates a texture resource, and then loads the alpha channel.</span></span>


```
LPDIRECT3DTEXTURE9 m_pTexture;

// Create an alpha texture
D3DXCreateTexture(m_d3dDevice, 128, 128, 0, D3DUSAGE_RENDERTARGET, 
    D3DFMT_A8R8G8B8, D3DPOOL_MANAGED, &m_pTexture);

// Initialize the alpha channel
int  yGrad, xGrad;
D3DLOCKED_RECT lockedRect;

if(SUCCEEDED(pTexture->LockRect(0, &lockedRect, NULL, D3DLOCK_DISCARD )))
{
    m_pRGBAData = new DWORD[128*128];
    if( m_pRGBAData != NULL )
    {
        for( DWORD y=0; y < m_dwHeight; y++ )
        {   
            DWORD dwOffset = y*m_dwWidth;
            yGrad = (int)(((float)y/(float)m_dwWidth) * 255.0f);
            
            for( DWORD x=0; x < m_dwWidth; x )
            {
                xGrad = (int)(((float)x/(float)m_dwWidth) * 255.0f);

                DWORD b = (DWORD)(xGrad + (255 - yGrad))/2 & 0xFF;
                DWORD g = (DWORD)((255 - xGrad) + yGrad)/2 & 0xFF;
                DWORD r = (DWORD)(xGrad + yGrad)/2 & 0xFF;
                DWORD a = (DWORD)(xGrad + yGrad)/2 & 0xFF;

                lockedRect.pBits[dwOffset+x] = ((a<<24L)+(r<<16L)+(g<<8L)+(b));
                x++;
            }
        }
    }
    pTexture->UnlockRect(&lockedRect);
}
```



<span data-ttu-id="83a9b-110">Il valore alfa viene calcolato in base alla posizione x/y relativa al pixel corrente all'interno delle dimensioni della trama.</span><span class="sxs-lookup"><span data-stu-id="83a9b-110">The alpha value is calculated based on the current pixel's relative x/y position within the texture size.</span></span> <span data-ttu-id="83a9b-111">Assegnare quindi la trama a una fase di trama e impostare la fase della trama.</span><span class="sxs-lookup"><span data-stu-id="83a9b-111">Next, assign the texture to a texture stage and set up the texture stage.</span></span>


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

// Assign texture
m_pd3dDevice->SetTexture(0, m_pTexture);

// Texture stage states
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);  

m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE);

m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE);
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG2, D3DTA_DIFFUSE);

m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAOP, D3DTOP_MODULATE);

```



<span data-ttu-id="83a9b-112">In questo modo si ottiene una primitiva con una sfumatura di trasparenza.</span><span class="sxs-lookup"><span data-stu-id="83a9b-112">This results in a primitive with a transparency gradient.</span></span> <span data-ttu-id="83a9b-113">La sfumatura è trasparente dove x = 0 e Opaque dove x è il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="83a9b-113">The gradient is transparent where x = 0, and opaque where x is its maximum value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83a9b-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83a9b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83a9b-115">Fusione alfa</span><span class="sxs-lookup"><span data-stu-id="83a9b-115">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



