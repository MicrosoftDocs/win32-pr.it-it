---
description: Direct3D mantiene un elenco di un massimo di otto trame correnti. Combina queste trame su tutte le primitive di cui esegue il rendering. Nel set di trame correnti è possibile usare solo trame create come puntatori dell'interfaccia di trama.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Assegnazione delle trame correnti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483981"
---
# <a name="assigning-the-current-textures-direct3d-9"></a><span data-ttu-id="c2db6-105">Assegnazione delle trame correnti (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c2db6-105">Assigning the Current Textures (Direct3D 9)</span></span>

<span data-ttu-id="c2db6-106">Direct3D mantiene un elenco di un massimo di otto trame correnti.</span><span class="sxs-lookup"><span data-stu-id="c2db6-106">Direct3D maintains a list of up to eight current textures.</span></span> <span data-ttu-id="c2db6-107">Combina queste trame su tutte le primitive di cui esegue il rendering.</span><span class="sxs-lookup"><span data-stu-id="c2db6-107">It blends these textures onto all the primitive it renders.</span></span> <span data-ttu-id="c2db6-108">Nel set di trame correnti è possibile usare solo trame create come puntatori dell'interfaccia di trama.</span><span class="sxs-lookup"><span data-stu-id="c2db6-108">Only textures created as texture interface pointers can be used in the set of current textures.</span></span>

<span data-ttu-id="c2db6-109">Le applicazioni chiamano il metodo [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) per assegnare trame al set di trame correnti.</span><span class="sxs-lookup"><span data-stu-id="c2db6-109">Applications call the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method to assign textures into the set of current textures.</span></span> <span data-ttu-id="c2db6-110">Il primo parametro deve essere un numero compreso nell'intervallo 0-7, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="c2db6-110">The first parameter must be a number in the range of 0-7, inclusive.</span></span> <span data-ttu-id="c2db6-111">Passare il puntatore all'interfaccia di trama come secondo parametro.</span><span class="sxs-lookup"><span data-stu-id="c2db6-111">Pass the texture interface pointer as the second parameter.</span></span>

<span data-ttu-id="c2db6-112">Nell'esempio di codice C++ riportato di seguito viene illustrato il modo in cui una trama può essere assegnata al set di trame correnti.</span><span class="sxs-lookup"><span data-stu-id="c2db6-112">The following C++ code example demonstrates how a texture can be assigned to the set of current textures.</span></span>


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> <span data-ttu-id="c2db6-113">I dispositivi software non supportano l'assegnazione di una trama a più di una fase di trama alla volta.</span><span class="sxs-lookup"><span data-stu-id="c2db6-113">Software devices do not support assigning a texture to more than one texture stage at a time.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c2db6-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2db6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2db6-115">Combinazione di trame</span><span class="sxs-lookup"><span data-stu-id="c2db6-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
