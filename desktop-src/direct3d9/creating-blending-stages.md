---
description: Una fase di fusione è un set di operazioni di trama e i relativi argomenti che definiscono il modo in cui vengono combinate le trame.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Creazione di fasi di fusione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126882"
---
# <a name="creating-blending-stages-direct3d-9"></a><span data-ttu-id="bbbba-103">Creazione di fasi di fusione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bbbba-103">Creating Blending Stages (Direct3D 9)</span></span>

<span data-ttu-id="bbbba-104">Una fase di fusione è un set di operazioni di trama e i relativi argomenti che definiscono il modo in cui vengono combinate le trame.</span><span class="sxs-lookup"><span data-stu-id="bbbba-104">A blending stage is a set of texture operations and their arguments that define how textures are blended.</span></span> <span data-ttu-id="bbbba-105">Quando si crea una fase di fusione, le applicazioni C++ richiamano il metodo [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="bbbba-105">When making a blending stage, C++ applications invoke the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="bbbba-106">La prima chiamata specifica l'operazione eseguita.</span><span class="sxs-lookup"><span data-stu-id="bbbba-106">The first call specifies the operation that is performed.</span></span> <span data-ttu-id="bbbba-107">Due chiamate aggiuntive definiscono gli argomenti a cui viene applicata l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bbbba-107">Two additional invocations define the arguments to which the operation is applied.</span></span> <span data-ttu-id="bbbba-108">Nell'esempio di codice seguente viene illustrata la creazione di una fase di Blend.</span><span class="sxs-lookup"><span data-stu-id="bbbba-108">The following code example illustrates the creation of a blending stage.</span></span>


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



<span data-ttu-id="bbbba-109">I dati Texel nelle trame contengono valori di colore e alfa.</span><span class="sxs-lookup"><span data-stu-id="bbbba-109">Texel data in textures contain color and alpha values.</span></span> <span data-ttu-id="bbbba-110">Le applicazioni possono definire operazioni separate per i valori di colore e alfa in una singola fase di fusione.</span><span class="sxs-lookup"><span data-stu-id="bbbba-110">Applications can define separate operations for both color and alpha values in a single blending stage.</span></span> <span data-ttu-id="bbbba-111">Ogni operazione, colore e alfa ha i propri argomenti.</span><span class="sxs-lookup"><span data-stu-id="bbbba-111">Each operation, color, and alpha, has its own arguments.</span></span> <span data-ttu-id="bbbba-112">Per informazioni dettagliate, vedere [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="bbbba-112">For details, see [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

<span data-ttu-id="bbbba-113">Sebbene non faccia parte dell'API Direct3D, è possibile inserire le macro seguenti nell'applicazione per abbreviare il codice necessario per la creazione di fasi di blending delle trame.</span><span class="sxs-lookup"><span data-stu-id="bbbba-113">Although not part of the Direct3D API, you can insert the following macros into your application to abbreviate the code required for creating texture blending stages.</span></span>


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a><span data-ttu-id="bbbba-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbbba-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbbba-115">Combinazione di trame</span><span class="sxs-lookup"><span data-stu-id="bbbba-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
