---
title: EFFECTs. effectType
description: Il metodo effectType Recupera il nome del registro di sistema della visualizzazione con l'indice del registro di sistema specificato. Questo nome è un ID univoco definito dall'autore della visualizzazione.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- EFFECTs. effectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328297"
---
# <a name="effectseffecttype"></a><span data-ttu-id="d1571-105">EFFECTs. effectType</span><span class="sxs-lookup"><span data-stu-id="d1571-105">EFFECTS.effectType</span></span>

<span data-ttu-id="d1571-106">Il metodo **effectType** Recupera il nome del registro di sistema della visualizzazione con l'indice del registro di sistema specificato.</span><span class="sxs-lookup"><span data-stu-id="d1571-106">The **effectType** method retrieves the registry name of the visualization with the specified registry index.</span></span> <span data-ttu-id="d1571-107">Questo nome è un ID univoco definito dall'autore della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d1571-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a><span data-ttu-id="d1571-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1571-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1571-109"><span id="index"></span><span id="INDEX"></span>*Indice*</span><span class="sxs-lookup"><span data-stu-id="d1571-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="d1571-110">**Numero** (**Long**) che contiene l'indice del registro di sistema di una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d1571-110">**Number** (**long**) containing the registry index of a visualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1571-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1571-111">Return Value</span></span>

<span data-ttu-id="d1571-112">Questo metodo restituisce una **stringa**.</span><span class="sxs-lookup"><span data-stu-id="d1571-112">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1571-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1571-113">Remarks</span></span>

<span data-ttu-id="d1571-114">Questo metodo è utile per passare da una visualizzazione all'altra nello script.</span><span class="sxs-lookup"><span data-stu-id="d1571-114">This method is useful for switching between visualizations in script.</span></span> <span data-ttu-id="d1571-115">Un'interfaccia utente può visualizzare il set di titoli, ma quando l'utente ne seleziona uno, lo script deve usare **currentEffectType** per cambiare le visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="d1571-115">A user interface could display the set of titles, but when the user selects one, the script must use **currentEffectType** to switch visualizations.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1571-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1571-116">Requirements</span></span>



| <span data-ttu-id="d1571-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1571-117">Requirement</span></span> | <span data-ttu-id="d1571-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d1571-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="d1571-119">Versione</span><span class="sxs-lookup"><span data-stu-id="d1571-119">Version</span></span><br/> | <span data-ttu-id="d1571-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d1571-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1571-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1571-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1571-122">**EFFECTs-elemento**</span><span class="sxs-lookup"><span data-stu-id="d1571-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="d1571-123">**EFFECTs. currentEffectType**</span><span class="sxs-lookup"><span data-stu-id="d1571-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





