---
description: La modalità di indirizzamento dei colori del bordo, identificata dal \_ membro del bordo D3DTADDRESS del tipo enumerato D3DTEXTUREADDRESS, induce Direct3D a usare un colore arbitrario, noto come colore del bordo, per qualsiasi coordinate di trama non compresa nell'intervallo tra 0,0 e 1,0 inclusi.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Modalità di indirizzo della trama colore del bordo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42b18d88f3b9305d0602e43a9528357a9397d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401482"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a><span data-ttu-id="670e8-103">Modalità di indirizzo della trama colore del bordo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="670e8-103">Border Color Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="670e8-104">La modalità di indirizzamento dei colori del bordo, identificata dal \_ membro del bordo D3DTADDRESS del tipo enumerato [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , induce Direct3D a usare un colore arbitrario, noto come colore del bordo, per qualsiasi coordinate di trama non compresa nell'intervallo tra 0,0 e 1,0 inclusi.</span><span class="sxs-lookup"><span data-stu-id="670e8-104">The border color texture address mode, identified by the D3DTADDRESS\_BORDER member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to use an arbitrary color, known as the border color, for any texture coordinates outside the range of 0.0 through 1.0, inclusive.</span></span>

<span data-ttu-id="670e8-105">Nell'illustrazione seguente, l'applicazione specifica che la trama viene applicata alla primitiva usando un bordo rosso.</span><span class="sxs-lookup"><span data-stu-id="670e8-105">In the following illustration, the application specifies that the texture be applied to the primitive using a red border.</span></span>

![illustrazione di una trama e una trama con un bordo rosso](images/border.png)

<span data-ttu-id="670e8-107">Le applicazioni impostano il colore del bordo chiamando [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="670e8-107">Applications set the border color by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="670e8-108">Impostare il primo parametro per la chiamata all'identificatore della fase di trama desiderato, il secondo parametro per il \_ valore dello stato della fase BorderColor D3DSAMP e il terzo parametro al nuovo colore del bordo di RGBA.</span><span class="sxs-lookup"><span data-stu-id="670e8-108">Set the first parameter for the call to the desired texture stage identifier, the second parameter to the D3DSAMP\_BORDERCOLOR stage state value, and the third parameter to the new RGBA border color.</span></span>

## <a name="related-topics"></a><span data-ttu-id="670e8-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="670e8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="670e8-110">Modalità di indirizzamento delle trame</span><span class="sxs-lookup"><span data-stu-id="670e8-110">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
