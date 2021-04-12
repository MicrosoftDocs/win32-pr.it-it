---
description: La proprietà AutoReconnect dell'oggetto SWbemRefresher è un valore booleano che indica se l'aggiornamento viene riconnesso automaticamente a un provider remoto se la connessione è interruppe.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Proprietà SWbemRefresher. AutoReconnect (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351321"
---
# <a name="swbemrefresherautoreconnect-property"></a><span data-ttu-id="b6add-103">Proprietà SWbemRefresher. AutoReconnect</span><span class="sxs-lookup"><span data-stu-id="b6add-103">SWbemRefresher.AutoReconnect property</span></span>

<span data-ttu-id="b6add-104">La proprietà **AutoReconnect** dell'oggetto [**SWbemRefresher**](swbemrefresher.md) è un valore booleano che indica se l'aggiornamento viene riconnesso automaticamente a un provider remoto se la connessione è interruppe.</span><span class="sxs-lookup"><span data-stu-id="b6add-104">The **AutoReconnect** property of the [**SWbemRefresher**](swbemrefresher.md) object is a Boolean value that indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span>

<span data-ttu-id="b6add-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b6add-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="b6add-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b6add-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6add-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6add-107">Syntax</span></span>


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b6add-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b6add-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="b6add-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6add-109">Remarks</span></span>

<span data-ttu-id="b6add-110">La modifica di questa proprietà ha effetto solo sugli oggetti nell'aggiornamento supportato da un provider ad alte prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b6add-110">Modifying this property affects only objects in the refresher that are backed by a high-performance provider.</span></span> <span data-ttu-id="b6add-111">Se il provider non è un provider a prestazioni elevate, l'impostazione della proprietà **AutoReconnect** su **true** non ha alcun effetto perché l'oggetto [**SWbemRefresher**](swbemrefresher.md) non si riconnette mai.</span><span class="sxs-lookup"><span data-stu-id="b6add-111">If the provider is not a high-performance provider, then setting the **AutoReconnect** property to **TRUE** has no effect because the [**SWbemRefresher**](swbemrefresher.md) object never reconnects.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6add-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6add-112">Requirements</span></span>



| <span data-ttu-id="b6add-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6add-113">Requirement</span></span> | <span data-ttu-id="b6add-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b6add-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6add-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6add-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b6add-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6add-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6add-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6add-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b6add-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6add-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6add-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6add-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6add-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6add-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6add-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b6add-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6add-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b6add-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b6add-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b6add-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6add-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6add-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b6add-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="b6add-125">CLSID</span></span><br/>                    | <span data-ttu-id="b6add-126">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="b6add-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="b6add-127">IID</span><span class="sxs-lookup"><span data-stu-id="b6add-127">IID</span></span><br/>                      | <span data-ttu-id="b6add-128">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="b6add-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="b6add-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6add-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6add-130">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="b6add-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




