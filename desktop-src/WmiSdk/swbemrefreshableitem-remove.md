---
description: Il metodo SWbemRefreshableItem. Remove rimuove l'oggetto SWbemRefreshableItem dall'oggetto SWbemRefresher padre. Oggetto SWbemRefreshableItem dall'oggetto SWbemRefresher padre.
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: Metodo SWbemRefreshableItem. Remove (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320585"
---
# <a name="swbemrefreshableitemremove-method"></a><span data-ttu-id="ec65b-103">Metodo SWbemRefreshableItem. Remove</span><span class="sxs-lookup"><span data-stu-id="ec65b-103">SWbemRefreshableItem.Remove method</span></span>

<span data-ttu-id="ec65b-104">Il metodo **SWbemRefreshableItem. Remove** rimuove l'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) dall'oggetto [**SWbemRefresher**](swbemrefresher.md) padre.</span><span class="sxs-lookup"><span data-stu-id="ec65b-104">The **SWbemRefreshableItem.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object from the parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="ec65b-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ec65b-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec65b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec65b-106">Syntax</span></span>


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ec65b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec65b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec65b-108">*è* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ec65b-108">*lFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec65b-109">Questo parametro deve essere impostato su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="ec65b-109">This parameter must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec65b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec65b-110">Return value</span></span>

<span data-ttu-id="ec65b-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ec65b-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec65b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec65b-112">Remarks</span></span>

<span data-ttu-id="ec65b-113">**Codici di errore** Se l'aggiornamento non ha alcun elemento con l'indice specificato, viene generato **wbemErrNotFound** .</span><span class="sxs-lookup"><span data-stu-id="ec65b-113">**Error Codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec65b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec65b-114">Requirements</span></span>



| <span data-ttu-id="ec65b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec65b-115">Requirement</span></span> | <span data-ttu-id="ec65b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ec65b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec65b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec65b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ec65b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec65b-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec65b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec65b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ec65b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec65b-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec65b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec65b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec65b-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec65b-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec65b-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ec65b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec65b-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec65b-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec65b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ec65b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec65b-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec65b-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec65b-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="ec65b-127">CLSID</span></span><br/>                    | <span data-ttu-id="ec65b-128">\_SWBEMREFRESHABLEITEM CLSID</span><span class="sxs-lookup"><span data-stu-id="ec65b-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="ec65b-129">IID</span><span class="sxs-lookup"><span data-stu-id="ec65b-129">IID</span></span><br/>                      | <span data-ttu-id="ec65b-130">\_ISWBEMREFRESHABLEITEM IID</span><span class="sxs-lookup"><span data-stu-id="ec65b-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="ec65b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec65b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec65b-132">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="ec65b-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="ec65b-133">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="ec65b-133">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




