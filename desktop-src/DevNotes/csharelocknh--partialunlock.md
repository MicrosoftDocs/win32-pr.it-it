---
description: Rilascia un blocco parziale in modo che sia ora possibile immettere altri acquirenti di blocchi esclusivi o parziali.
ms.assetid: 95a3e0d1-4e8b-4e30-b4fd-709b9db465de
title: CShareLockNH::P metodo artialUnlock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 930c0f51e199c1668a70f2dd017b0280939b0710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327358"
---
# <a name="csharelocknhpartialunlock-method"></a><span data-ttu-id="e0f2e-103">CShareLockNH::P metodo artialUnlock</span><span class="sxs-lookup"><span data-stu-id="e0f2e-103">CShareLockNH::PartialUnlock method</span></span>

<span data-ttu-id="e0f2e-104">Rilascia un blocco parziale in modo che sia ora possibile immettere altri acquirenti di blocchi esclusivi o parziali.</span><span class="sxs-lookup"><span data-stu-id="e0f2e-104">Releases a partial lock so that other exclusive or partial lock acquirers can now enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f2e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0f2e-105">Syntax</span></span>


```C++
void PartialUnlock();
```



## <a name="parameters"></a><span data-ttu-id="e0f2e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0f2e-106">Parameters</span></span>

<span data-ttu-id="e0f2e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e0f2e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0f2e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0f2e-108">Return value</span></span>

<span data-ttu-id="e0f2e-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e0f2e-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0f2e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0f2e-110">Remarks</span></span>

<span data-ttu-id="e0f2e-111">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e0f2e-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f2e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0f2e-112">Requirements</span></span>



| <span data-ttu-id="e0f2e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0f2e-113">Requirement</span></span> | <span data-ttu-id="e0f2e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e0f2e-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f2e-115">DLL</span><span class="sxs-lookup"><span data-stu-id="e0f2e-115">DLL</span></span><br/> | <dl> <span data-ttu-id="e0f2e-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0f2e-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
