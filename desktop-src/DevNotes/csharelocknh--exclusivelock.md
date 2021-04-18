---
description: Acquisisce un blocco in lettura/scrittura.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'Metodo CShareLockNH:: ExclusiveLock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331682"
---
# <a name="csharelocknhexclusivelock-method"></a><span data-ttu-id="c849a-103">Metodo CShareLockNH:: ExclusiveLock</span><span class="sxs-lookup"><span data-stu-id="c849a-103">CShareLockNH::ExclusiveLock method</span></span>

<span data-ttu-id="c849a-104">Acquisisce un blocco in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c849a-104">Acquires a reader/writer lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="c849a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c849a-105">Syntax</span></span>


```C++
void ExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="c849a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c849a-106">Parameters</span></span>

<span data-ttu-id="c849a-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c849a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c849a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c849a-108">Return value</span></span>

<span data-ttu-id="c849a-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c849a-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c849a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c849a-110">Remarks</span></span>

<span data-ttu-id="c849a-111">Ogni chiamata a **ExclusiveLock** deve essere abbinata esattamente a una chiamata a [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) per evitare il rischio di un deadlock.</span><span class="sxs-lookup"><span data-stu-id="c849a-111">Each call to **ExclusiveLock** must be paired with exactly one call to [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="c849a-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c849a-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c849a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c849a-113">Requirements</span></span>



| <span data-ttu-id="c849a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c849a-114">Requirement</span></span> | <span data-ttu-id="c849a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c849a-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c849a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="c849a-116">DLL</span></span><br/> | <dl> <span data-ttu-id="c849a-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c849a-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c849a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c849a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c849a-119">**ExclusiveUnlock**</span><span class="sxs-lookup"><span data-stu-id="c849a-119">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
