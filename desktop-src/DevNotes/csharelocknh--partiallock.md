---
description: Impedisce a più di un thread di completare l'acquisizione di un blocco.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: CShareLockNH::P metodo artialLock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 0b7b7d55c9fd8d979aa14f12939df922e7a89099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327359"
---
# <a name="csharelocknhpartiallock-method"></a><span data-ttu-id="83517-103">CShareLockNH::P metodo artialLock</span><span class="sxs-lookup"><span data-stu-id="83517-103">CShareLockNH::PartialLock method</span></span>

<span data-ttu-id="83517-104">Impedisce a più di un thread di completare l'acquisizione di un blocco.</span><span class="sxs-lookup"><span data-stu-id="83517-104">Prevents more than one thread from completing acquiring a lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="83517-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83517-105">Syntax</span></span>


```C++
void PartialLock();
```



## <a name="parameters"></a><span data-ttu-id="83517-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83517-106">Parameters</span></span>

<span data-ttu-id="83517-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="83517-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83517-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83517-108">Return value</span></span>

<span data-ttu-id="83517-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="83517-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83517-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="83517-110">Remarks</span></span>

<span data-ttu-id="83517-111">Mentre **PartialLock** è attivo, gli altri thread che chiamano [**ShareLock**](csharelocknh--sharelock.md) possono immettere il blocco.</span><span class="sxs-lookup"><span data-stu-id="83517-111">While **PartialLock** is in effect, other threads calling [**ShareLock**](csharelocknh--sharelock.md) can enter the lock.</span></span>

<span data-ttu-id="83517-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="83517-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="83517-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83517-113">Requirements</span></span>



| <span data-ttu-id="83517-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="83517-114">Requirement</span></span> | <span data-ttu-id="83517-115">Valore</span><span class="sxs-lookup"><span data-stu-id="83517-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="83517-116">DLL</span><span class="sxs-lookup"><span data-stu-id="83517-116">DLL</span></span><br/> | <dl> <span data-ttu-id="83517-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83517-117"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
