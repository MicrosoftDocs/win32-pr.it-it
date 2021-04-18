---
description: Rilascia un blocco acquisito utilizzando ExclusiveLock in modalità condivisa.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'Metodo CShareLockNH:: ExclusiveUnlock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331678"
---
# <a name="csharelocknhexclusiveunlock-method"></a><span data-ttu-id="d180d-103">Metodo CShareLockNH:: ExclusiveUnlock</span><span class="sxs-lookup"><span data-stu-id="d180d-103">CShareLockNH::ExclusiveUnlock method</span></span>

<span data-ttu-id="d180d-104">Rilascia un blocco acquisito utilizzando [**ExclusiveLock**](csharelocknh--exclusivelock.md) in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="d180d-104">Releases a lock acquired by using [**ExclusiveLock**](csharelocknh--exclusivelock.md) to shared mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="d180d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d180d-105">Syntax</span></span>


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a><span data-ttu-id="d180d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d180d-106">Parameters</span></span>

<span data-ttu-id="d180d-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d180d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d180d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d180d-108">Return value</span></span>

<span data-ttu-id="d180d-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d180d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d180d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d180d-110">Remarks</span></span>

<span data-ttu-id="d180d-111">Ogni chiamata a [**ExclusiveLock**](csharelocknh--exclusivelock.md) deve essere abbinata esattamente a una chiamata a **ExclusiveUnlock** per evitare il rischio di un deadlock.</span><span class="sxs-lookup"><span data-stu-id="d180d-111">Each call to [**ExclusiveLock**](csharelocknh--exclusivelock.md) must be paired with exactly one call to **ExclusiveUnlock** to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="d180d-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d180d-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d180d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d180d-113">Requirements</span></span>



| <span data-ttu-id="d180d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d180d-114">Requirement</span></span> | <span data-ttu-id="d180d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d180d-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d180d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d180d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d180d-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d180d-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d180d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d180d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d180d-119">**ExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="d180d-119">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
