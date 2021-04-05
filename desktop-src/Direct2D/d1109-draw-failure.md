---
title: Errore di D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Una chiamata di disegnare da una destinazione di rendering non è riuscita
keywords:
- Direct2D errore di D1109 di estrazione
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4b08dfb99d49dcb447443685e1fbfa01a2cbad1c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730079"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="2d759-104">D1109: errore di estrazione</span><span class="sxs-lookup"><span data-stu-id="2d759-104">D1109: Draw Failure</span></span>

<span data-ttu-id="2d759-105">Una chiamata di disegnare da una risorsa di destinazione di rendering non riuscita \[  \] .</span><span class="sxs-lookup"><span data-stu-id="2d759-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="2d759-106">Tag \[ *tag1*, *Tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="2d759-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="2d759-107">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="2d759-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="2d759-108"><span id="resource"></span><span id="RESOURCE"></span>*risorse*</span><span class="sxs-lookup"><span data-stu-id="2d759-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="2d759-109">Indirizzo della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="2d759-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="2d759-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="2d759-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="2d759-111">Il primo valore del tag (per ulteriori informazioni, vedere la pagina relativa ai [**tag**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).</span><span class="sxs-lookup"><span data-stu-id="2d759-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="2d759-112"><span id="tag2"></span><span id="TAG2"></span>*Tag2*</span><span class="sxs-lookup"><span data-stu-id="2d759-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="2d759-113">Il secondo valore del tag (per ulteriori informazioni, vedere la pagina relativa ai [**tag**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).</span><span class="sxs-lookup"><span data-stu-id="2d759-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="2d759-114">Livello di errore</span><span class="sxs-lookup"><span data-stu-id="2d759-114">Error Level</span></span> | <span data-ttu-id="2d759-115">Avviso</span><span class="sxs-lookup"><span data-stu-id="2d759-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="2d759-116">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="2d759-116">Possible Causes</span></span>

<span data-ttu-id="2d759-117">Esistono molti motivi per cui una chiamata di un progetto potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="2d759-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="2d759-118">Per ulteriori informazioni, vedere la documentazione di Direct2D SDK per il metodo che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2d759-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 