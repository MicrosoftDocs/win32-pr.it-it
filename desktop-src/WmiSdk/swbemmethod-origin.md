---
description: La proprietà Origin dell'oggetto SWbemMethod restituisce il nome della classe in cui è stato introdotto il metodo.
ms.assetid: da98393b-af95-47ad-b589-663063f65afb
ms.tgt_platform: multiple
title: Proprietà SWbemMethod. Origin (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.Origin
- ISWbemMethod.Origin
- ISWbemMethod.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1b903a2c55bbd571a9cd1f36a51812a70c123cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226817"
---
# <a name="swbemmethodorigin-property"></a><span data-ttu-id="1d4e9-103">Proprietà SWbemMethod. Origin</span><span class="sxs-lookup"><span data-stu-id="1d4e9-103">SWbemMethod.Origin property</span></span>

<span data-ttu-id="1d4e9-104">La proprietà **Origin** dell'oggetto [**SWbemMethod**](swbemmethod.md) restituisce il nome della classe in cui è stato introdotto il metodo.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-104">The **Origin** property of the [**SWbemMethod**](swbemmethod.md) object returns the name of the class in which this method was introduced.</span></span> <span data-ttu-id="1d4e9-105">Per le classi con gerarchie di ereditarietà completa, è spesso opportuno individuare i metodi dichiarati in quali classi.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-105">For classes with deep inheritance hierarchies, it is often desirable to know which methods were declared in which classes.</span></span> <span data-ttu-id="1d4e9-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-106">This property is read-only.</span></span>

<span data-ttu-id="1d4e9-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1d4e9-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="1d4e9-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4e9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d4e9-109">Syntax</span></span>


```VB
SWbemMethod.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="1d4e9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1d4e9-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="1d4e9-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d4e9-111">Requirements</span></span>



| <span data-ttu-id="1d4e9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d4e9-112">Requirement</span></span> | <span data-ttu-id="1d4e9-113">Valore</span><span class="sxs-lookup"><span data-stu-id="1d4e9-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4e9-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d4e9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4e9-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d4e9-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d4e9-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d4e9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4e9-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d4e9-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d4e9-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d4e9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d4e9-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d4e9-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d4e9-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1d4e9-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d4e9-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1d4e9-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1d4e9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1d4e9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d4e9-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d4e9-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1d4e9-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="1d4e9-124">CLSID</span></span><br/>                    | <span data-ttu-id="1d4e9-125">\_SWBEMMETHOD CLSID</span><span class="sxs-lookup"><span data-stu-id="1d4e9-125">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="1d4e9-126">IID</span><span class="sxs-lookup"><span data-stu-id="1d4e9-126">IID</span></span><br/>                      | <span data-ttu-id="1d4e9-127">\_ISWBEMMETHOD IID</span><span class="sxs-lookup"><span data-stu-id="1d4e9-127">IID\_ISWbemMethod</span></span><br/>                                                            |



 

 




