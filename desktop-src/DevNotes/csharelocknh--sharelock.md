---
description: Ottiene un blocco condiviso.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'Metodo CShareLockNH:: ShareLock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327352"
---
# <a name="csharelocknhsharelock-method"></a><span data-ttu-id="2e58e-103">Metodo CShareLockNH:: ShareLock</span><span class="sxs-lookup"><span data-stu-id="2e58e-103">CShareLockNH::ShareLock method</span></span>

<span data-ttu-id="2e58e-104">Ottiene un blocco condiviso.</span><span class="sxs-lookup"><span data-stu-id="2e58e-104">Obtains a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e58e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e58e-105">Syntax</span></span>


```C++
void ShareLock();
```



## <a name="parameters"></a><span data-ttu-id="2e58e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e58e-106">Parameters</span></span>

<span data-ttu-id="2e58e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2e58e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e58e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e58e-108">Return value</span></span>

<span data-ttu-id="2e58e-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2e58e-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e58e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e58e-110">Remarks</span></span>

<span data-ttu-id="2e58e-111">Ogni chiamata a **ShareLock** deve essere abbinata esattamente a una chiamata a [**ShareUnlock**](csharelocknh--shareunlock.md).</span><span class="sxs-lookup"><span data-stu-id="2e58e-111">Each call to **ShareLock** must be paired with exactly one call to [**ShareUnlock**](csharelocknh--shareunlock.md).</span></span> <span data-ttu-id="2e58e-112">Solo un thread che chiama correttamente **ShareLock** può chiamare **ShareUnlock**; in caso contrario, può verificarsi un deadlock.</span><span class="sxs-lookup"><span data-stu-id="2e58e-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="2e58e-113">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2e58e-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e58e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e58e-114">Requirements</span></span>



| <span data-ttu-id="2e58e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e58e-115">Requirement</span></span> | <span data-ttu-id="2e58e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2e58e-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2e58e-117">DLL</span><span class="sxs-lookup"><span data-stu-id="2e58e-117">DLL</span></span><br/> | <dl> <span data-ttu-id="2e58e-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e58e-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e58e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e58e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e58e-120">**ShareUnlock**</span><span class="sxs-lookup"><span data-stu-id="2e58e-120">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
