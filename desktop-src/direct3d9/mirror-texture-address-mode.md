---
description: La modalità address texture mirror, identificata dal \_ membro mirror D3DTADDRESS del tipo enumerato D3DTEXTUREADDRESS, fa sì che Direct3D rispecchi la trama a ogni limite intero.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Modalità address texture mirror (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471ad8b715d9375947162c66474687b9d6376bec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401167"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a><span data-ttu-id="ed1de-103">Modalità address texture mirror (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ed1de-103">Mirror Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="ed1de-104">La modalità address texture mirror, identificata dal \_ membro mirror D3DTADDRESS del tipo enumerato [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , fa sì che Direct3D rispecchi la trama a ogni limite intero.</span><span class="sxs-lookup"><span data-stu-id="ed1de-104">The mirror texture address mode, identified by the D3DTADDRESS\_MIRROR member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to mirror the texture at every integer boundary.</span></span> <span data-ttu-id="ed1de-105">Si supponga, ad esempio, che l'applicazione crei una primitiva quadrata e specifichi le coordinate di trama (0,0, 0,0), (0.0, 3.0), (3.0, 3.0) e (3.0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="ed1de-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="ed1de-106">Impostando la modalità di indirizzamento della trama su D3DTADDRESS \_ mirror, la trama viene applicata tre volte nelle direzioni u-e-v.</span><span class="sxs-lookup"><span data-stu-id="ed1de-106">Setting the texture addressing mode to D3DTADDRESS\_MIRROR results in the texture being applied three times in both the u- and v-directions.</span></span> <span data-ttu-id="ed1de-107">Ogni altra riga e colonna a cui viene applicato è un'immagine speculare della riga o della colonna precedente, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="ed1de-107">Every other row and column that it is applied to is a mirror image of the preceding row or column, as shown in the following illustration.</span></span>

![illustrazione delle immagini speculari in una griglia 3x3](images/mirror.png)

<span data-ttu-id="ed1de-109">Gli effetti di questa modalità di indirizzamento della trama sono simili a quelli della modalità a capo, ma distinti.</span><span class="sxs-lookup"><span data-stu-id="ed1de-109">The effects of this texture address mode are similar to, but distinct from, those of the wrap mode.</span></span> <span data-ttu-id="ed1de-110">Per altre informazioni, vedere [modalità di indirizzamento della trama a capo (Direct3D 9)](wrap-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="ed1de-110">For more information, see [Wrap Texture Address Mode (Direct3D 9)](wrap-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed1de-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed1de-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed1de-112">Modalità di indirizzamento delle trame</span><span class="sxs-lookup"><span data-stu-id="ed1de-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
