---
title: AmbientAttributes. Enabled
description: L'attributo enabled specifica o recupera un valore che indica se il controllo è abilitato o disabilitato.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- Media Player Windows AmbientAttributes. Enabled
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324753"
---
# <a name="ambientattributesenabled"></a><span data-ttu-id="d6478-104">AmbientAttributes. Enabled</span><span class="sxs-lookup"><span data-stu-id="d6478-104">AmbientAttributes.enabled</span></span>

<span data-ttu-id="d6478-105">L'attributo **Enabled** specifica o recupera un valore che indica se il controllo è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d6478-105">The **enabled** attribute specifies or retrieves a value indicating whether the control is enabled or disabled.</span></span>

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a><span data-ttu-id="d6478-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d6478-106">Possible Values</span></span>

<span data-ttu-id="d6478-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d6478-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="d6478-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d6478-108">Value</span></span> | <span data-ttu-id="d6478-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6478-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="d6478-110">true</span><span class="sxs-lookup"><span data-stu-id="d6478-110">true</span></span>  | <span data-ttu-id="d6478-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d6478-111">Default.</span></span> <span data-ttu-id="d6478-112">Controllo abilitato.</span><span class="sxs-lookup"><span data-stu-id="d6478-112">Control enabled.</span></span> |
| <span data-ttu-id="d6478-113">false</span><span class="sxs-lookup"><span data-stu-id="d6478-113">false</span></span> | <span data-ttu-id="d6478-114">Controllo disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d6478-114">Control disabled.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="d6478-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6478-115">Remarks</span></span>

<span data-ttu-id="d6478-116">Se il controllo è abilitato, può avere una tabulazione e riceverà tutti gli eventi di ambiente.</span><span class="sxs-lookup"><span data-stu-id="d6478-116">If the control is enabled, it can have a tab stop, and will receive all ambient events.</span></span> <span data-ttu-id="d6478-117">Quando è disabilitato, il controllo non ha una tabulazione e non riceve alcun evento mouse o tastiera di ambiente attivato.</span><span class="sxs-lookup"><span data-stu-id="d6478-117">When disabled, the control does not have a tab stop, and does not receive any ambient mouse or keyboard events fired to it.</span></span> <span data-ttu-id="d6478-118">Continuerà comunque a ricevere tutti gli altri eventi di ambiente generati.</span><span class="sxs-lookup"><span data-stu-id="d6478-118">(However, it will continue to receive all other ambient events fired to it.)</span></span>

<span data-ttu-id="d6478-119">Questo attributo non è supportato per l'elemento di **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="d6478-119">This attribute is not supported for the **SUBVIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6478-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6478-120">Requirements</span></span>



| <span data-ttu-id="d6478-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6478-121">Requirement</span></span> | <span data-ttu-id="d6478-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d6478-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d6478-123">Versione</span><span class="sxs-lookup"><span data-stu-id="d6478-123">Version</span></span><br/> | <span data-ttu-id="d6478-124">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="d6478-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6478-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6478-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6478-126">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="d6478-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





