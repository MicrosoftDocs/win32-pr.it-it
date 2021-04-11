---
description: Recupera la transazione o il proxy di transazione associato al contesto corrente, se presente.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'Metodo IContextTransactionInfo:: FetchTransaction'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127031"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a><span data-ttu-id="3da0b-103">Metodo IContextTransactionInfo:: FetchTransaction</span><span class="sxs-lookup"><span data-stu-id="3da0b-103">IContextTransactionInfo::FetchTransaction method</span></span>

<span data-ttu-id="3da0b-104">Recupera la transazione o il proxy di transazione associato al contesto corrente, se presente.</span><span class="sxs-lookup"><span data-stu-id="3da0b-104">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da0b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3da0b-105">Syntax</span></span>


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="3da0b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3da0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da0b-107">*punk* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3da0b-107">*pUnk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3da0b-108">Transazione o proxy di transazione associato al contesto corrente. in caso contrario, **null**.</span><span class="sxs-lookup"><span data-stu-id="3da0b-108">The transaction or transaction proxy that is associated with the current context; otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da0b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3da0b-109">Return value</span></span>

<span data-ttu-id="3da0b-110">Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3da0b-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da0b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3da0b-111">Requirements</span></span>



| <span data-ttu-id="3da0b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3da0b-112">Requirement</span></span> | <span data-ttu-id="3da0b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="3da0b-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3da0b-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3da0b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3da0b-115">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3da0b-115">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3da0b-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3da0b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3da0b-117">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="3da0b-117">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3da0b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3da0b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da0b-119">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="3da0b-119">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




