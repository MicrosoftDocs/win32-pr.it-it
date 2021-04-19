---
description: Un effetto viene creato caricando il valore nel Framework degli effetti.
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: Creazione di un effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304602"
---
# <a name="create-an-effect-direct3d-10"></a><span data-ttu-id="24eab-103">Creazione di un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="24eab-103">Create an Effect (Direct3D 10)</span></span>

<span data-ttu-id="24eab-104">Un effetto viene creato caricando il valore nel Framework degli effetti.</span><span class="sxs-lookup"><span data-stu-id="24eab-104">An effect is created by loading it into the effects framework.</span></span> <span data-ttu-id="24eab-105">Se l'effetto non è mai stato compilato, verrà compilato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="24eab-105">If the effect has never been compiled, it will be compiled when it is created.</span></span> <span data-ttu-id="24eab-106">Gli effetti già caricati nella memoria possono essere creati chiamando [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="24eab-106">Effects that are already loaded into memory can be created by calling [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md).</span></span> <span data-ttu-id="24eab-107">Nell'esempio di codice seguente viene usato [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) per creare un effetto da un file.</span><span class="sxs-lookup"><span data-stu-id="24eab-107">The following code example uses [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) to create an effect from a file.</span></span>


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



<span data-ttu-id="24eab-108">Per la lettura di un effetto sono necessari gli stessi parametri della compilazione di un effetto, oltre a un dispositivo e a un pool.</span><span class="sxs-lookup"><span data-stu-id="24eab-108">Reading an effect requires the same parameters as compiling an effect, plus a device and a pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24eab-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24eab-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24eab-110">Rendering di un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="24eab-110">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



