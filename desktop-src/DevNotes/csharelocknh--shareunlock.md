---
description: Rilascia un blocco condiviso.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'Metodo CShareLockNH:: ShareUnlock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 80c4311f4bf66000440dac38da6300888a8e5d59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327350"
---
# <a name="csharelocknhshareunlock-method"></a><span data-ttu-id="2a196-103">Metodo CShareLockNH:: ShareUnlock</span><span class="sxs-lookup"><span data-stu-id="2a196-103">CShareLockNH::ShareUnlock method</span></span>

<span data-ttu-id="2a196-104">Rilascia un blocco condiviso.</span><span class="sxs-lookup"><span data-stu-id="2a196-104">Releases a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a196-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a196-105">Syntax</span></span>


```C++
void ShareUnlock();
```



## <a name="parameters"></a><span data-ttu-id="2a196-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a196-106">Parameters</span></span>

<span data-ttu-id="2a196-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2a196-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a196-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a196-108">Return value</span></span>

<span data-ttu-id="2a196-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2a196-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a196-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a196-110">Remarks</span></span>

<span data-ttu-id="2a196-111">Ogni chiamata a [**ShareLock**](csharelocknh--sharelock.md) deve essere abbinata esattamente a una chiamata a **ShareUnlock**.</span><span class="sxs-lookup"><span data-stu-id="2a196-111">Each call to [**ShareLock**](csharelocknh--sharelock.md) must be paired with exactly one call to **ShareUnlock**.</span></span> <span data-ttu-id="2a196-112">Solo un thread che chiama correttamente **ShareLock** può chiamare **ShareUnlock**; in caso contrario, può verificarsi un deadlock.</span><span class="sxs-lookup"><span data-stu-id="2a196-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="2a196-113">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2a196-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a196-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a196-114">Requirements</span></span>



| <span data-ttu-id="2a196-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a196-115">Requirement</span></span> | <span data-ttu-id="2a196-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2a196-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2a196-117">DLL</span><span class="sxs-lookup"><span data-stu-id="2a196-117">DLL</span></span><br/> | <dl> <span data-ttu-id="2a196-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a196-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a196-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a196-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a196-120">**ShareLock**</span><span class="sxs-lookup"><span data-stu-id="2a196-120">**ShareLock**</span></span>](csharelocknh--sharelock.md)
</dt> </dl>

 

 
