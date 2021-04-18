---
title: EFFECTs. allowAll
description: L'attributo allowAll specifica o recupera un valore che indica se includere tutte le visualizzazioni presenti nel registro di sistema.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- EFFECTs. allowAll Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325859"
---
# <a name="effectsallowall"></a><span data-ttu-id="7207a-104">EFFECTs. allowAll</span><span class="sxs-lookup"><span data-stu-id="7207a-104">EFFECTS.allowAll</span></span>

<span data-ttu-id="7207a-105">L'attributo **allowAll** specifica o recupera un valore che indica se includere tutte le visualizzazioni presenti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7207a-105">The **allowAll** attribute specifies or retrieves a value indicating whether to include all the visualizations that are in the registry.</span></span>

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a><span data-ttu-id="7207a-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="7207a-106">Possible Values</span></span>

<span data-ttu-id="7207a-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7207a-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="7207a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="7207a-108">Value</span></span> | <span data-ttu-id="7207a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7207a-109">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="7207a-110">true</span><span class="sxs-lookup"><span data-stu-id="7207a-110">true</span></span>  | <span data-ttu-id="7207a-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7207a-111">Default.</span></span> <span data-ttu-id="7207a-112">Consente il ciclo di tutte le visualizzazioni nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7207a-112">Allows cycling of all visualizations on the user's system.</span></span> |
| <span data-ttu-id="7207a-113">false</span><span class="sxs-lookup"><span data-stu-id="7207a-113">false</span></span> | <span data-ttu-id="7207a-114">Limita il ciclo alle visualizzazioni visualizzate all'interno dei tag **degli effetti** .</span><span class="sxs-lookup"><span data-stu-id="7207a-114">Limits cycling to visualizations appearing within **EFFECTS** tags.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7207a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7207a-115">Remarks</span></span>

<span data-ttu-id="7207a-116">Se questo attributo è impostato su false, solo le visualizzazioni visualizzate all'interno dei tag **Effects** possono essere ciclate usando Previous/Next.</span><span class="sxs-lookup"><span data-stu-id="7207a-116">If this attribute is set to false, only the visualizations appearing within **EFFECTS** tags can be cycled through using previous/next.</span></span> <span data-ttu-id="7207a-117">Se è impostato su true, tutte le visualizzazioni registrate nel sistema dell'utente possono essere ciclate tramite.</span><span class="sxs-lookup"><span data-stu-id="7207a-117">If it is set to true, then all visualizations that are registered on the user's system can be cycled through.</span></span> <span data-ttu-id="7207a-118">Se è impostato su true e si specificano le visualizzazioni all'interno dei tag **Effects** , gli attributi specificati in questi tag vengono applicati a tutte le visualizzazioni nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7207a-118">If it is set to true and you specify any visualizations within **EFFECTS** tags, then the attributes specified in these tags are applied to all visualizations on the user's system.</span></span>

## <a name="requirements"></a><span data-ttu-id="7207a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7207a-119">Requirements</span></span>



| <span data-ttu-id="7207a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7207a-120">Requirement</span></span> | <span data-ttu-id="7207a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7207a-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7207a-122">Versione</span><span class="sxs-lookup"><span data-stu-id="7207a-122">Version</span></span><br/> | <span data-ttu-id="7207a-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="7207a-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7207a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7207a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7207a-125">**EFFECTs-elemento**</span><span class="sxs-lookup"><span data-stu-id="7207a-125">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





