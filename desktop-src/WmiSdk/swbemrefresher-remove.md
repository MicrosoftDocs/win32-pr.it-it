---
description: Il metodo SWbemRefresher. Remove rimuove l'oggetto SWbemRefreshableItem con l'indice specificato dall'aggiornamento.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: Metodo SWbemRefresher. Remove (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968932"
---
# <a name="swbemrefresherremove-method"></a><span data-ttu-id="d60a9-103">Metodo SWbemRefresher. Remove</span><span class="sxs-lookup"><span data-stu-id="d60a9-103">SWbemRefresher.Remove method</span></span>

<span data-ttu-id="d60a9-104">Il metodo **SWbemRefresher. Remove** rimuove l'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) con l'indice specificato dall'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d60a9-104">The **SWbemRefresher.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object with the specified index from the refresher.</span></span> <span data-ttu-id="d60a9-105">L'oggetto **SWbemRefreshableItem** può rappresentare un singolo oggetto o un set di oggetti.</span><span class="sxs-lookup"><span data-stu-id="d60a9-105">The **SWbemRefreshableItem** object can represent either a single object or an object set.</span></span>

<span data-ttu-id="d60a9-106">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d60a9-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d60a9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d60a9-107">Syntax</span></span>


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d60a9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d60a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d60a9-109">*LIndex*</span><span class="sxs-lookup"><span data-stu-id="d60a9-109">*LIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="d60a9-110">Indice dell'elemento nell'oggetto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="d60a9-110">Index of the item in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="d60a9-111">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d60a9-111">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d60a9-112">I flag devono essere impostati T0 (zero).</span><span class="sxs-lookup"><span data-stu-id="d60a9-112">Flags must be set t0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="d60a9-113">*objWbemNamedvalueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="d60a9-113">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d60a9-114">Null.</span><span class="sxs-lookup"><span data-stu-id="d60a9-114">Null.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d60a9-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d60a9-115">Return value</span></span>

<span data-ttu-id="d60a9-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d60a9-116">This method has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d60a9-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d60a9-117">Remarks</span></span>

<span data-ttu-id="d60a9-118">**Codici di errore** Se l'aggiornamento non ha alcun elemento con l'indice specificato, viene generato **wbemErrNotFound** .</span><span class="sxs-lookup"><span data-stu-id="d60a9-118">**Error codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="d60a9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d60a9-119">Requirements</span></span>



| <span data-ttu-id="d60a9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d60a9-120">Requirement</span></span> | <span data-ttu-id="d60a9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d60a9-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d60a9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d60a9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d60a9-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d60a9-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d60a9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d60a9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d60a9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d60a9-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d60a9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d60a9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d60a9-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d60a9-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d60a9-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d60a9-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="d60a9-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d60a9-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d60a9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d60a9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d60a9-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d60a9-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d60a9-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="d60a9-132">CLSID</span></span><br/>                    | <span data-ttu-id="d60a9-133">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="d60a9-133">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="d60a9-134">IID</span><span class="sxs-lookup"><span data-stu-id="d60a9-134">IID</span></span><br/>                      | <span data-ttu-id="d60a9-135">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="d60a9-135">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="d60a9-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d60a9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d60a9-137">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="d60a9-137">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




