---
description: Recupera il livello di isolamento e il valore di timeout di una transazione ospitata nel contesto di transazione radice.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: 'Metodo IContextTransactionInfo:: GetTxIsolationLevelAndTimeout'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305324"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a><span data-ttu-id="f1768-103">Metodo IContextTransactionInfo:: GetTxIsolationLevelAndTimeout</span><span class="sxs-lookup"><span data-stu-id="f1768-103">IContextTransactionInfo::GetTxIsolationLevelAndTimeout method</span></span>

<span data-ttu-id="f1768-104">Recupera il livello di isolamento e il valore di timeout di una transazione ospitata nel contesto di transazione radice.</span><span class="sxs-lookup"><span data-stu-id="f1768-104">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1768-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1768-105">Syntax</span></span>


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a><span data-ttu-id="f1768-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1768-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1768-107">*pIsoLevel* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f1768-107">*pIsoLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1768-108">Valore [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) per la transazione.</span><span class="sxs-lookup"><span data-stu-id="f1768-108">The [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) value for the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="f1768-109">*dwTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f1768-109">*dwTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1768-110">Timeout della transazione, in secondi.</span><span class="sxs-lookup"><span data-stu-id="f1768-110">The timeout of the transaction, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1768-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1768-111">Return value</span></span>

<span data-ttu-id="f1768-112">Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f1768-112">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1768-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1768-113">Requirements</span></span>



| <span data-ttu-id="f1768-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1768-114">Requirement</span></span> | <span data-ttu-id="f1768-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f1768-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f1768-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1768-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f1768-117">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1768-117">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f1768-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1768-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f1768-119">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="f1768-119">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1768-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1768-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1768-121">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="f1768-121">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

