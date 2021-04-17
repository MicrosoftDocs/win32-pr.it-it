---
description: Il metodo SWbemRefresher. Item restituisce il SWbemRefreshableItem specificato dalla raccolta. SWbemRefreshableItem dalla raccolta.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: Metodo SWbemRefresher. Item (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234494"
---
# <a name="swbemrefresheritem-method"></a><span data-ttu-id="0c9ee-103">Metodo SWbemRefresher. Item</span><span class="sxs-lookup"><span data-stu-id="0c9ee-103">SWbemRefresher.Item method</span></span>

<span data-ttu-id="0c9ee-104">Il metodo **SWbemRefresher. Item** restituisce il [**SWbemRefreshableItem**](swbemrefreshableitem.md) specificato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="0c9ee-104">The **SWbemRefresher.Item** method returns the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) from the collection.</span></span>

<span data-ttu-id="0c9ee-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0c9ee-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c9ee-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c9ee-106">Syntax</span></span>


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="0c9ee-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c9ee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c9ee-108">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="0c9ee-108">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="0c9ee-109">Valore di indice dell'elemento nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="0c9ee-109">Index value of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c9ee-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c9ee-110">Return value</span></span>

<span data-ttu-id="0c9ee-111">Se la chiamata ha esito positivo, viene restituito l'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="0c9ee-111">If the call is successful, the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0c9ee-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0c9ee-112">Error codes</span></span>

<span data-ttu-id="0c9ee-113">Se l'aggiornamento non ha alcun elemento con l'indice specificato, viene generato **wbemErrNotFound** .</span><span class="sxs-lookup"><span data-stu-id="0c9ee-113">If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c9ee-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c9ee-114">Requirements</span></span>



| <span data-ttu-id="0c9ee-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c9ee-115">Requirement</span></span> | <span data-ttu-id="0c9ee-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0c9ee-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c9ee-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c9ee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0c9ee-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c9ee-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c9ee-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c9ee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0c9ee-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c9ee-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c9ee-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c9ee-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c9ee-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c9ee-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c9ee-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0c9ee-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="0c9ee-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0c9ee-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0c9ee-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0c9ee-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c9ee-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c9ee-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0c9ee-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="0c9ee-127">CLSID</span></span><br/>                    | <span data-ttu-id="0c9ee-128">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="0c9ee-128">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="0c9ee-129">IID</span><span class="sxs-lookup"><span data-stu-id="0c9ee-129">IID</span></span><br/>                      | <span data-ttu-id="0c9ee-130">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="0c9ee-130">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="0c9ee-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c9ee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c9ee-132">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="0c9ee-132">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




