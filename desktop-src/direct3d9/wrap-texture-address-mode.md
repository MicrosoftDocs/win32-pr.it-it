---
description: La modalità di indirizzamento della trama a capo, identificata dal \_ membro D3DTADDRESS wrap del tipo enumerato D3DTEXTUREADDRESS, consente a Direct3D di ripetere la trama in ogni giunzione di interi.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Modalità di indirizzamento della trama a capo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225332"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a><span data-ttu-id="403ce-103">Modalità di indirizzamento della trama a capo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="403ce-103">Wrap Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="403ce-104">La modalità di indirizzamento della trama a capo, identificata dal \_ membro D3DTADDRESS wrap del tipo enumerato [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , consente a Direct3D di ripetere la trama in ogni giunzione di interi.</span><span class="sxs-lookup"><span data-stu-id="403ce-104">The wrap texture address mode, identified by the D3DTADDRESS\_WRAP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, makes Direct3D repeat the texture on every integer junction.</span></span> <span data-ttu-id="403ce-105">Si supponga, ad esempio, che l'applicazione crei una primitiva quadrata e specifichi le coordinate di trama (0,0, 0,0), (0.0, 3.0), (3.0, 3.0) e (3.0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="403ce-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="403ce-106">Impostando la modalità di indirizzamento della trama su D3DTADDRESS \_ wrap, la trama viene applicata tre volte nelle direzioni u-e-v, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="403ce-106">Setting the texture addressing mode to D3DTADDRESS\_WRAP results in the texture being applied three times in both the u-and v-directions, as shown in the following illustration.</span></span>

![illustrazione di una trama del volto racchiusa tra la direzione u e la direzione della v](images/wrap.png)

<span data-ttu-id="403ce-108">Gli effetti di questa modalità di indirizzamento della trama sono simili a, ma distinti da quelli della modalità mirror.</span><span class="sxs-lookup"><span data-stu-id="403ce-108">The effects of this texture address mode are similar to, but distinct from, those of the mirror mode.</span></span> <span data-ttu-id="403ce-109">Per ulteriori informazioni, vedere [modalità address texture mirror (Direct3D 9)](mirror-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="403ce-109">For more information, see [Mirror Texture Address Mode (Direct3D 9)](mirror-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="403ce-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="403ce-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="403ce-111">Modalità di indirizzamento delle trame</span><span class="sxs-lookup"><span data-stu-id="403ce-111">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
