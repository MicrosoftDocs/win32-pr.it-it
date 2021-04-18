---
title: EFFECTs. currentEffectType
description: L'attributo currentEffectType specifica o Recupera il nome del registro di sistema della visualizzazione corrente. Questo nome è un ID univoco definito dall'autore della visualizzazione.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- EFFECTs. currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325847"
---
# <a name="effectscurrenteffecttype"></a><span data-ttu-id="37bc1-105">EFFECTs. currentEffectType</span><span class="sxs-lookup"><span data-stu-id="37bc1-105">EFFECTS.currentEffectType</span></span>

<span data-ttu-id="37bc1-106">L'attributo **currentEffectType** specifica o Recupera il nome del registro di sistema della visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="37bc1-106">The **currentEffectType** attribute specifies or retrieves the registry name of the current visualization.</span></span> <span data-ttu-id="37bc1-107">Questo nome è un ID univoco definito dall'autore della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="37bc1-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a><span data-ttu-id="37bc1-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="37bc1-108">Possible Values</span></span>

<span data-ttu-id="37bc1-109">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="37bc1-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="37bc1-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="37bc1-110">Remarks</span></span>

<span data-ttu-id="37bc1-111">È possibile usare questo attributo in fase di esecuzione per modificare l'effetto attualmente visualizzato.</span><span class="sxs-lookup"><span data-stu-id="37bc1-111">You can use this attribute at run time to change the currently displayed effect.</span></span> <span data-ttu-id="37bc1-112">A questo scopo, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="37bc1-112">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="37bc1-113">Usare **effectCount** per recuperare il conteggio degli effetti registrati.</span><span class="sxs-lookup"><span data-stu-id="37bc1-113">Use **effectCount** to retrieve the count of registered effects.</span></span>
2.  <span data-ttu-id="37bc1-114">In un ciclo recuperare il nome di ogni effetto registrato utilizzando **effectType**.</span><span class="sxs-lookup"><span data-stu-id="37bc1-114">In a loop, retrieve the name of each registered effect by using **effectType**.</span></span>
3.  <span data-ttu-id="37bc1-115">Specificare uno dei nomi recuperati per **currentEffectType** per impostare l'effetto corrente.</span><span class="sxs-lookup"><span data-stu-id="37bc1-115">Specify one of the names you retrieved for **currentEffectType** to set the current effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="37bc1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37bc1-116">Requirements</span></span>



| <span data-ttu-id="37bc1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="37bc1-117">Requirement</span></span> | <span data-ttu-id="37bc1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="37bc1-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="37bc1-119">Versione</span><span class="sxs-lookup"><span data-stu-id="37bc1-119">Version</span></span><br/> | <span data-ttu-id="37bc1-120">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="37bc1-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37bc1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37bc1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37bc1-122">**EFFECTs-elemento**</span><span class="sxs-lookup"><span data-stu-id="37bc1-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="37bc1-123">**EFFECTs. currentEffect**</span><span class="sxs-lookup"><span data-stu-id="37bc1-123">**EFFECTS.currentEffect**</span></span>](effects-currenteffect.md)
</dt> <dt>

[<span data-ttu-id="37bc1-124">**EFFECTs. effectCount**</span><span class="sxs-lookup"><span data-stu-id="37bc1-124">**EFFECTS.effectCount**</span></span>](effects-effectcount.md)
</dt> <dt>

[<span data-ttu-id="37bc1-125">**EFFECTs. effectType**</span><span class="sxs-lookup"><span data-stu-id="37bc1-125">**EFFECTS.effectType**</span></span>](effects-effecttype.md)
</dt> </dl>

 

 





