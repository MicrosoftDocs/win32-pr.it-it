---
title: Errore di disegno D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Una chiamata di disegno da parte di una destinazione di rendering non è riuscita
keywords:
- Errore di disegno D1109 Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 09d84f549b2361d2753ac40650ce057de9e4f84c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549966"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="610d9-104">D1109: Errore di disegno</span><span class="sxs-lookup"><span data-stu-id="610d9-104">D1109: Draw Failure</span></span>

<span data-ttu-id="610d9-105">Una chiamata di disegno da parte di una risorsa di destinazione di rendering non \[ *è riuscita.* \]</span><span class="sxs-lookup"><span data-stu-id="610d9-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="610d9-106">Tag1 \[ , *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="610d9-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="610d9-107">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="610d9-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="610d9-108"><span id="resource"></span><span id="RESOURCE"></span>*Risorsa*</span><span class="sxs-lookup"><span data-stu-id="610d9-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="610d9-109">Indirizzo della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="610d9-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="610d9-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="610d9-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="610d9-111">Il primo valore del tag (per [**altre informazioni, vedere SetTags).**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)</span><span class="sxs-lookup"><span data-stu-id="610d9-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="610d9-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="610d9-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="610d9-113">Il secondo valore del tag (per [**altre informazioni, vedere SetTags).**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)</span><span class="sxs-lookup"><span data-stu-id="610d9-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="610d9-114">Livello di errore</span><span class="sxs-lookup"><span data-stu-id="610d9-114">Error Level</span></span> | <span data-ttu-id="610d9-115">Avviso</span><span class="sxs-lookup"><span data-stu-id="610d9-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="610d9-116">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="610d9-116">Possible Causes</span></span>

<span data-ttu-id="610d9-117">Esistono molti motivi per cui una chiamata di disegno potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="610d9-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="610d9-118">Per altre informazioni, vedere la documentazione di Direct2D SDK per il metodo che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="610d9-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 