---
description: La proprietà Origin dell'oggetto SWbemProperty Recupera il nome della classe WMI in cui è stata introdotta la proprietà. Per le classi con gerarchie di ereditarietà completa, è spesso opportuno individuare le proprietà dichiarate nelle classi.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Proprietà SWbemProperty. Origin (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231821"
---
# <a name="swbempropertyorigin-property"></a><span data-ttu-id="2e5c6-104">Proprietà SWbemProperty. Origin</span><span class="sxs-lookup"><span data-stu-id="2e5c6-104">SWbemProperty.Origin property</span></span>

<span data-ttu-id="2e5c6-105">La proprietà **Origin** dell'oggetto [**SWbemProperty**](swbemproperty.md) Recupera il nome della classe WMI in cui è stata introdotta la proprietà.</span><span class="sxs-lookup"><span data-stu-id="2e5c6-105">The **Origin** property of the [**SWbemProperty**](swbemproperty.md) object retrieves the name of the WMI class in which this property was introduced.</span></span> <span data-ttu-id="2e5c6-106">Per le classi con gerarchie di ereditarietà completa, è spesso opportuno individuare le proprietà dichiarate nelle classi.</span><span class="sxs-lookup"><span data-stu-id="2e5c6-106">For classes with deep inheritance hierarchies, it is often desirable to know which properties were declared in which classes.</span></span>

<span data-ttu-id="2e5c6-107">Se la proprietà è locale (vedere [**oggetto SWbemQualifier. setlocale**](swbemqualifier-islocal.md)), questo valore corrisponde alla classe proprietaria.</span><span class="sxs-lookup"><span data-stu-id="2e5c6-107">If the property is local (see [**SWbemQualifier.IsLocal**](swbemqualifier-islocal.md)), this value is the same as the owning class.</span></span> <span data-ttu-id="2e5c6-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2e5c6-108">This property is read-only.</span></span>

<span data-ttu-id="2e5c6-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2e5c6-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="2e5c6-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2e5c6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e5c6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e5c6-111">Syntax</span></span>


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="2e5c6-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2e5c6-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="2e5c6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e5c6-113">Requirements</span></span>



| <span data-ttu-id="2e5c6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e5c6-114">Requirement</span></span> | <span data-ttu-id="2e5c6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2e5c6-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e5c6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e5c6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e5c6-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e5c6-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e5c6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e5c6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e5c6-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e5c6-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e5c6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e5c6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e5c6-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e5c6-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e5c6-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2e5c6-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e5c6-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2e5c6-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2e5c6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2e5c6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e5c6-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e5c6-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2e5c6-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="2e5c6-126">CLSID</span></span><br/>                    | <span data-ttu-id="2e5c6-127">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="2e5c6-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="2e5c6-128">IID</span><span class="sxs-lookup"><span data-stu-id="2e5c6-128">IID</span></span><br/>                      | <span data-ttu-id="2e5c6-129">\_ISWBEMPROPERTY IID</span><span class="sxs-lookup"><span data-stu-id="2e5c6-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




