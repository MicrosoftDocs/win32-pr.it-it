---
description: Definisce un frame di coordinate o &\# 0034; frame di riferimento. &\# 0034; Il modello di frame è aperto e può contenere qualsiasi oggetto. Le funzioni di caricamento mesh D3DX riconoscono le istanze di modelli mesh, FrameTransformMatrix e frame come oggetti figlio durante il caricamento di un'istanza di frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Frame (grafica Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81cc9d02b1bcbc21cc299739d93272afcf110c92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876197"
---
# <a name="frame-direct3d-9-graphics"></a><span data-ttu-id="3e559-104">Frame (grafica Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3e559-104">Frame (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="3e559-105">Definisce un frame di coordinate o un "frame di riferimento".</span><span class="sxs-lookup"><span data-stu-id="3e559-105">Defines a coordinate frame, or "frame of reference."</span></span> <span data-ttu-id="3e559-106">Il modello di frame è aperto e può contenere qualsiasi oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e559-106">The Frame template is open and can contain any object.</span></span> <span data-ttu-id="3e559-107">Le funzioni di caricamento mesh D3DX riconoscono le istanze di modelli [**mesh**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md)e **frame** come oggetti figlio durante il caricamento di un'istanza di **frame** .</span><span class="sxs-lookup"><span data-stu-id="3e559-107">The D3DX mesh-loading functions recognize [**Mesh**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md), and **Frame** template instances as child objects when loading a **Frame** instance.</span></span>

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

<span data-ttu-id="3e559-108">Il modello di frame riconosce i **nodi figlio e** i nodi [**mesh**](mesh.md) all'interno di un frame e può riconoscere i modelli definiti dall'utente tramite una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="3e559-108">The frame template recognizes child **Frame** and [**Mesh**](mesh.md) nodes inside a frame and can recognize user-defined templates through a callback function.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e559-109">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e559-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e559-110">Modelli</span><span class="sxs-lookup"><span data-stu-id="3e559-110">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



