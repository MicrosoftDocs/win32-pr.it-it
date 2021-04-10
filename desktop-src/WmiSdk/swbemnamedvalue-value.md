---
description: La proprietà Value dell'oggetto SWbemNamedValue restituisce il valore Variant di un elemento SWbemNamedValue.
ms.assetid: f9609bd2-893a-48c3-9faa-93cd033c4109
ms.tgt_platform: multiple
title: Proprietà SWbemNamedValue. Value (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValue.Value
- ISWbemNamedValue.Value
- ISWbemNamedValue.get_Value
- ISWbemNamedValue.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bf63b15a27c1149341200f29e938bdba6cd7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130987"
---
# <a name="swbemnamedvaluevalue-property"></a><span data-ttu-id="ff4a7-103">Proprietà SWbemNamedValue. Value</span><span class="sxs-lookup"><span data-stu-id="ff4a7-103">SWbemNamedValue.Value property</span></span>

<span data-ttu-id="ff4a7-104">La proprietà **value** dell'oggetto [**SWbemNamedValue**](swbemnamedvalue.md) restituisce il valore Variant di un elemento **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="ff4a7-104">The **Value** property of the [**SWbemNamedValue**](swbemnamedvalue.md) object returns the variant value of an **SWbemNamedValue** item.</span></span> <span data-ttu-id="ff4a7-105">Si tratta della proprietà predefinita per gli oggetti **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="ff4a7-105">This is the default property for **SWbemNamedValue** objects.</span></span> <span data-ttu-id="ff4a7-106">Le modifiche apportate alla proprietà Value vengono riflesse automaticamente nella raccolta [**SWbemNamedValueSet**](swbemnamedvalueset.md) a cui appartiene l'oggetto **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="ff4a7-106">Changes made to the value property are reflected automatically in the [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection to which the **SWbemNamedValue** object belongs.</span></span>

<span data-ttu-id="ff4a7-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ff4a7-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="ff4a7-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ff4a7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff4a7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff4a7-109">Syntax</span></span>


```VB
SWbemNamedValue.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="ff4a7-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ff4a7-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="ff4a7-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff4a7-111">Requirements</span></span>



| <span data-ttu-id="ff4a7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff4a7-112">Requirement</span></span> | <span data-ttu-id="ff4a7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ff4a7-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff4a7-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff4a7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ff4a7-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff4a7-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff4a7-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff4a7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ff4a7-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff4a7-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff4a7-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff4a7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff4a7-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff4a7-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff4a7-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ff4a7-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff4a7-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ff4a7-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ff4a7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ff4a7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff4a7-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff4a7-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff4a7-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="ff4a7-124">CLSID</span></span><br/>                    | <span data-ttu-id="ff4a7-125">\_SWBEMNAMEDVALUE CLSID</span><span class="sxs-lookup"><span data-stu-id="ff4a7-125">CLSID\_SWbemNamedValue</span></span><br/>                                                       |
| <span data-ttu-id="ff4a7-126">IID</span><span class="sxs-lookup"><span data-stu-id="ff4a7-126">IID</span></span><br/>                      | <span data-ttu-id="ff4a7-127">\_ISWBEMNAMEDVALUE IID</span><span class="sxs-lookup"><span data-stu-id="ff4a7-127">IID\_ISWbemNamedValue</span></span><br/>                                                        |



 

 




