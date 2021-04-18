---
description: Il metodo SetAsClass dell'oggetto SWbemObjectPath impone al percorso di indirizzare una classe WMI.
ms.assetid: d341b980-bac9-4db4-a55f-eb971fb385da
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath. SetAsClass (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsClass
- ISWbemObjectPath.SetAsClass
- ISWbemObjectPath.put_SetAsClass
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 371fe95c3a7152767c45849191658c4bcb661750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309804"
---
# <a name="swbemobjectpathsetasclass-property"></a><span data-ttu-id="31492-103">Proprietà SWbemObjectPath. SetAsClass</span><span class="sxs-lookup"><span data-stu-id="31492-103">SWbemObjectPath.SetAsClass property</span></span>

<span data-ttu-id="31492-104">Il metodo **SetAsClass** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) impone al percorso di indirizzare una classe WMI.</span><span class="sxs-lookup"><span data-stu-id="31492-104">The **SetAsClass** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a WMI class.</span></span>

<span data-ttu-id="31492-105">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="31492-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="31492-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31492-106">Syntax</span></span>


```VB
SWbemObjectPath.SetAsClass
```



## <a name="property-value"></a><span data-ttu-id="31492-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="31492-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="31492-108">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="31492-108">Error codes</span></span>

<span data-ttu-id="31492-109">Quando si ottiene o si imposta la proprietà **SetAsClass** , l'oggetto **Err** può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="31492-109">After you get or set the **SetAsClass** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="31492-110">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="31492-110">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="31492-111">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="31492-111">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31492-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31492-112">Requirements</span></span>



| <span data-ttu-id="31492-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="31492-113">Requirement</span></span> | <span data-ttu-id="31492-114">Valore</span><span class="sxs-lookup"><span data-stu-id="31492-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31492-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31492-115">Minimum supported client</span></span><br/> | <span data-ttu-id="31492-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31492-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31492-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31492-117">Minimum supported server</span></span><br/> | <span data-ttu-id="31492-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31492-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31492-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31492-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="31492-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="31492-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="31492-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="31492-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="31492-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="31492-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="31492-123">DLL</span><span class="sxs-lookup"><span data-stu-id="31492-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31492-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31492-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="31492-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="31492-125">CLSID</span></span><br/>                    | <span data-ttu-id="31492-126">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="31492-126">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="31492-127">IID</span><span class="sxs-lookup"><span data-stu-id="31492-127">IID</span></span><br/>                      | <span data-ttu-id="31492-128">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="31492-128">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




