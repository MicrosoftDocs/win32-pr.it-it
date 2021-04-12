---
description: La proprietà singleton dell'oggetto SWbemObjectPath è un valore booleano che indica se il percorso rappresenta un'istanza singleton. Un'istanza singleton è un'istanza di una classe che non può mai avere più di un'istanza. Questa proprietà è di sola lettura.
ms.assetid: 0d0533be-89fe-4ab6-bafa-2da6195ff02c
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath. Singleton (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.IsSingleton
- ISWbemObjectPath.IsSingleton
- ISWbemObjectPath.get_IsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bd267c3d8ad36459a04b835cb2f130c3e98420a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233802"
---
# <a name="swbemobjectpathissingleton-property"></a><span data-ttu-id="7711a-105">Proprietà SWbemObjectPath. Singleton</span><span class="sxs-lookup"><span data-stu-id="7711a-105">SWbemObjectPath.IsSingleton property</span></span>

<span data-ttu-id="7711a-106">La proprietà **singleton** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) è un valore booleano che indica se il percorso rappresenta un'istanza singleton.</span><span class="sxs-lookup"><span data-stu-id="7711a-106">The **IsSingleton** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is a Boolean value that indicates if this path represents a singleton instance.</span></span> <span data-ttu-id="7711a-107">Un'istanza singleton è un'istanza di una classe che non può mai avere più di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="7711a-107">A singleton instance is an instance of a class that can never have more than one instance.</span></span> <span data-ttu-id="7711a-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7711a-108">This property is read-only.</span></span>

<span data-ttu-id="7711a-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7711a-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="7711a-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7711a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7711a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7711a-111">Syntax</span></span>


```VB
SWbemObjectPath.IsSingleton As Boolean
```



## <a name="property-value"></a><span data-ttu-id="7711a-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7711a-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="7711a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7711a-113">Requirements</span></span>



| <span data-ttu-id="7711a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7711a-114">Requirement</span></span> | <span data-ttu-id="7711a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7711a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7711a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7711a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7711a-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7711a-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7711a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7711a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7711a-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7711a-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7711a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7711a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7711a-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7711a-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7711a-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7711a-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="7711a-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7711a-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7711a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7711a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7711a-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7711a-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7711a-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="7711a-126">CLSID</span></span><br/>                    | <span data-ttu-id="7711a-127">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="7711a-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="7711a-128">IID</span><span class="sxs-lookup"><span data-stu-id="7711a-128">IID</span></span><br/>                      | <span data-ttu-id="7711a-129">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="7711a-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




