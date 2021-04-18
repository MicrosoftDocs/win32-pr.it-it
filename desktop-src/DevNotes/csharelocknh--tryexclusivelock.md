---
description: Ottiene un blocco in modo esclusivo se non ne è attualmente presente nessun altro.
ms.assetid: d655b89c-f2c8-4965-a21b-f539b1598296
title: 'Metodo CShareLockNH:: TryExclusiveLock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.TryExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8465e247807c4229821acef552e0786a5604a3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327349"
---
# <a name="csharelocknhtryexclusivelock-method"></a><span data-ttu-id="37bc4-103">Metodo CShareLockNH:: TryExclusiveLock</span><span class="sxs-lookup"><span data-stu-id="37bc4-103">CShareLockNH::TryExclusiveLock method</span></span>

<span data-ttu-id="37bc4-104">Ottiene un blocco in modo esclusivo se non ne è attualmente presente nessun altro.</span><span class="sxs-lookup"><span data-stu-id="37bc4-104">Obtains a lock exclusively if no others are currently hold it.</span></span>

## <a name="syntax"></a><span data-ttu-id="37bc4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37bc4-105">Syntax</span></span>


```C++
BOOL TryExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="37bc4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="37bc4-106">Parameters</span></span>

<span data-ttu-id="37bc4-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="37bc4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37bc4-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37bc4-108">Return value</span></span>

<span data-ttu-id="37bc4-109">Restituisce **true** se la funzione ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="37bc4-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="37bc4-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="37bc4-110">Remarks</span></span>

<span data-ttu-id="37bc4-111">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="37bc4-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="37bc4-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37bc4-112">Requirements</span></span>



| <span data-ttu-id="37bc4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="37bc4-113">Requirement</span></span> | <span data-ttu-id="37bc4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="37bc4-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="37bc4-115">DLL</span><span class="sxs-lookup"><span data-stu-id="37bc4-115">DLL</span></span><br/> | <dl> <span data-ttu-id="37bc4-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37bc4-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
