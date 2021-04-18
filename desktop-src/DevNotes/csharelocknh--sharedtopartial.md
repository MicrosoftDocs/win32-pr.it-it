---
description: Modifica un blocco condiviso in un blocco parziale.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: 'Metodo CShareLockNH:: SharedToPartial'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: a997c5a437063a4c55b74d837dc77fd506688158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327351"
---
# <a name="csharelocknhsharedtopartial-method"></a><span data-ttu-id="4c78e-103">Metodo CShareLockNH:: SharedToPartial</span><span class="sxs-lookup"><span data-stu-id="4c78e-103">CShareLockNH::SharedToPartial method</span></span>

<span data-ttu-id="4c78e-104">Modifica un blocco condiviso in un blocco parziale.</span><span class="sxs-lookup"><span data-stu-id="4c78e-104">Changes a shared lock to a partial lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c78e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c78e-105">Syntax</span></span>


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a><span data-ttu-id="4c78e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c78e-106">Parameters</span></span>

<span data-ttu-id="4c78e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4c78e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c78e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c78e-108">Return value</span></span>

<span data-ttu-id="4c78e-109">Restituisce **true** se viene ottenuto il blocco parziale. in caso contrario, restituisce **false** e il blocco rimane in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="4c78e-109">Returns **TRUE** if the partial lock is obtained; otherwise, it returns **FALSE** and the lock remains in shared mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c78e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c78e-110">Remarks</span></span>

<span data-ttu-id="4c78e-111">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4c78e-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c78e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c78e-112">Requirements</span></span>



| <span data-ttu-id="4c78e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c78e-113">Requirement</span></span> | <span data-ttu-id="4c78e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4c78e-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4c78e-115">DLL</span><span class="sxs-lookup"><span data-stu-id="4c78e-115">DLL</span></span><br/> | <dl> <span data-ttu-id="4c78e-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c78e-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
