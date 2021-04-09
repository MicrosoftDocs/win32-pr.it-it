---
description: La proprietà Keys dell'oggetto SWbemObjectPath è un oggetto SWbemNamedValueSet che contiene le associazioni del valore della chiave. Questa proprietà è di sola lettura.
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath. Keys (Adoctint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049757"
---
# <a name="swbemobjectpathkeys-property"></a><span data-ttu-id="daae5-104">Proprietà SWbemObjectPath. Keys</span><span class="sxs-lookup"><span data-stu-id="daae5-104">SWbemObjectPath.Keys property</span></span>

<span data-ttu-id="daae5-105">La proprietà **Keys** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) è un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che contiene le associazioni del valore della chiave.</span><span class="sxs-lookup"><span data-stu-id="daae5-105">The **Keys** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span> <span data-ttu-id="daae5-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="daae5-106">This property is read-only.</span></span>

<span data-ttu-id="daae5-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="daae5-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="daae5-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="daae5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="daae5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="daae5-109">Syntax</span></span>


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a><span data-ttu-id="daae5-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="daae5-110">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="daae5-111">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="daae5-111">Error codes</span></span>

<span data-ttu-id="daae5-112">Una volta recuperata la proprietà **Keys** , l'oggetto **Err** può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="daae5-112">After you retrieve the **Keys** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="daae5-113">**wbemErrNotSupported** -2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="daae5-113">**wbemErrNotSupported** - 2147749900 (0x8004100C)</span></span>
</dt> <dd>

<span data-ttu-id="daae5-114">La funzionalità o l'operazione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="daae5-114">The feature or operation is not supported.</span></span> <span data-ttu-id="daae5-115">Questo errore viene restituito se uno script tenta di scrivere in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="daae5-115">This error is returned if a script attempts to write to this property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="daae5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="daae5-116">Requirements</span></span>



| <span data-ttu-id="daae5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="daae5-117">Requirement</span></span> | <span data-ttu-id="daae5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="daae5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daae5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="daae5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="daae5-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="daae5-120">Windows Vista</span></span><br/>                                                                                   |
| <span data-ttu-id="daae5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="daae5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="daae5-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="daae5-122">Windows Server 2008</span></span><br/>                                                                             |
| <span data-ttu-id="daae5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="daae5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="daae5-124"><dt>Adoctint. h (include wbemdisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="daae5-124"><dt>Adoctint.h (include Wbemdisp.h)</dt></span></span> </dl> |
| <span data-ttu-id="daae5-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="daae5-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="daae5-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="daae5-126"><dt>Wbemdisp.tlb</dt></span></span> </dl>                    |
| <span data-ttu-id="daae5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="daae5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daae5-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daae5-128"><dt>Wbemdisp.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="daae5-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="daae5-129">CLSID</span></span><br/>                    | <span data-ttu-id="daae5-130">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="daae5-130">CLSID\_SWbemObjectPath</span></span><br/>                                                                          |
| <span data-ttu-id="daae5-131">IID</span><span class="sxs-lookup"><span data-stu-id="daae5-131">IID</span></span><br/>                      | <span data-ttu-id="daae5-132">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="daae5-132">IID\_ISWbemObjectPath</span></span><br/>                                                                           |



 

 




