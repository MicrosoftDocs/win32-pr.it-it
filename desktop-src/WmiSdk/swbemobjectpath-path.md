---
description: La proprietà Path dell'oggetto SWbemObjectPath contiene il percorso assoluto. Corrisponde alla \_ \_ proprietà Path nell'API com. Si tratta della proprietà predefinita di questo oggetto.
ms.assetid: cc0d2c56-bb69-4008-8688-0166714ea5fd
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath. Path (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Path
- ISWbemObjectPath.Path
- ISWbemObjectPath.get_Path
- ISWbemObjectPath.put_Path
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02a3dfbf6dbc24434ad4d9807ab5e39dbc121043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313679"
---
# <a name="swbemobjectpathpath-property"></a><span data-ttu-id="fef11-105">Proprietà SWbemObjectPath. Path</span><span class="sxs-lookup"><span data-stu-id="fef11-105">SWbemObjectPath.Path property</span></span>

<span data-ttu-id="fef11-106">La proprietà **path** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) contiene il percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="fef11-106">The **Path** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the absolute path.</span></span> <span data-ttu-id="fef11-107">Corrisponde alla proprietà [ \_ \_ path](wmi-system-properties.md) nell'API com.</span><span class="sxs-lookup"><span data-stu-id="fef11-107">This is the same as the [\_\_Path](wmi-system-properties.md) property in the COM API.</span></span> <span data-ttu-id="fef11-108">Si tratta della proprietà predefinita di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="fef11-108">This is the default property of this object.</span></span>

<span data-ttu-id="fef11-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fef11-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="fef11-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fef11-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef11-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fef11-111">Syntax</span></span>


```VB
SWbemObjectPath.Path As String
```



## <a name="property-value"></a><span data-ttu-id="fef11-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fef11-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="fef11-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fef11-113">Requirements</span></span>



| <span data-ttu-id="fef11-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fef11-114">Requirement</span></span> | <span data-ttu-id="fef11-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fef11-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fef11-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fef11-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fef11-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fef11-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fef11-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fef11-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fef11-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fef11-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fef11-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fef11-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fef11-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fef11-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fef11-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fef11-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="fef11-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fef11-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fef11-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fef11-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fef11-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fef11-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fef11-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="fef11-126">CLSID</span></span><br/>                    | <span data-ttu-id="fef11-127">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="fef11-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="fef11-128">IID</span><span class="sxs-lookup"><span data-stu-id="fef11-128">IID</span></span><br/>                      | <span data-ttu-id="fef11-129">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="fef11-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




