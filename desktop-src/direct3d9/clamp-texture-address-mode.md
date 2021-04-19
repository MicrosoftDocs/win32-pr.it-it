---
description: La modalità di indirizzamento della trama del morsetto, identificata dal \_ membro del morsetto D3DTADDRESS del tipo enumerato D3DTEXTUREADDRESS, induce Direct3D a bloccare le coordinate di trama nell' \[ intervallo 0,0, 1,0 \] .
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Modalità di indirizzamento della trama del morsetto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153ed1f044bacaec6b87420eb7df22a2557349a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305189"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a><span data-ttu-id="e1ad9-103">Modalità di indirizzamento della trama del morsetto (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e1ad9-103">Clamp Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="e1ad9-104">La modalità di indirizzamento della trama del morsetto, identificata dal \_ membro del morsetto D3DTADDRESS del tipo enumerato [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , induce Direct3D a bloccare le coordinate di trama nell' \[ intervallo 0,0, 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="e1ad9-104">The clamp texture address mode, identified by the D3DTADDRESS\_CLAMP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to clamp your texture coordinates to the \[0.0, 1.0\] range.</span></span> <span data-ttu-id="e1ad9-105">Ovvero applica la trama una volta, quindi striscierà il colore dei pixel perimetrali.</span><span class="sxs-lookup"><span data-stu-id="e1ad9-105">That is, it applies the texture once, then smears the color of edge pixels.</span></span> <span data-ttu-id="e1ad9-106">Si supponga, ad esempio, che l'applicazione crei una primitiva quadrata e assegna le coordinate di trama (0,0, 0,0), (0.0, 3.0), (3.0, 3.0) e (3.0, 0,0) ai vertici della primitiva.</span><span class="sxs-lookup"><span data-stu-id="e1ad9-106">For example, suppose that your application creates a square primitive and assigns texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0) to the primitive's vertices.</span></span> <span data-ttu-id="e1ad9-107">Impostando la modalità di indirizzamento della trama su D3DTADDRESS \_ Clamp, la trama viene applicata una sola volta.</span><span class="sxs-lookup"><span data-stu-id="e1ad9-107">Setting the texture addressing mode to D3DTADDRESS\_CLAMP results in the texture being applied once.</span></span> <span data-ttu-id="e1ad9-108">I colori dei pixel nella parte superiore delle colonne e la fine delle righe vengono estesi rispettivamente alla parte superiore e a destra della primitiva.</span><span class="sxs-lookup"><span data-stu-id="e1ad9-108">The pixel colors at the top of the columns and the end of the rows are extended to the top and right of the primitive respectively.</span></span>

<span data-ttu-id="e1ad9-109">La figura seguente mostra una trama fissa.</span><span class="sxs-lookup"><span data-stu-id="e1ad9-109">The following illustration shows a clamped texture.</span></span>

![illustrazione di una trama e di una trama fissa](images/clamp.png)

## <a name="related-topics"></a><span data-ttu-id="e1ad9-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e1ad9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1ad9-112">Modalità di indirizzamento delle trame</span><span class="sxs-lookup"><span data-stu-id="e1ad9-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
