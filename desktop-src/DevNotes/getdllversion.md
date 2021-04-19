---
description: La funzione GetDllVersion Recupera il numero di versione di Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: GetDllVersion (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326674"
---
# <a name="getdllversion-function"></a><span data-ttu-id="4ee77-103">GetDllVersion (funzione)</span><span class="sxs-lookup"><span data-stu-id="4ee77-103">GetDllVersion function</span></span>

<span data-ttu-id="4ee77-104">\[Questa funzione non è più supportata, pertanto non è possibile garantirne il comportamento.</span><span class="sxs-lookup"><span data-stu-id="4ee77-104">\[This function is no longer supported, so its behavior cannot be guaranteed.</span></span> <span data-ttu-id="4ee77-105">\]</span><span class="sxs-lookup"><span data-stu-id="4ee77-105">\]</span></span>

<span data-ttu-id="4ee77-106">La funzione **GetDllVersion** Recupera il numero di versione di Cabinet.dll.</span><span class="sxs-lookup"><span data-stu-id="4ee77-106">The **GetDllVersion** function retrieves the version number of Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee77-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ee77-107">Syntax</span></span>


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a><span data-ttu-id="4ee77-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ee77-108">Parameters</span></span>

<span data-ttu-id="4ee77-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="4ee77-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ee77-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ee77-110">Return value</span></span>

<span data-ttu-id="4ee77-111">Il numero di versione del file (vedere la [risorsa VERSIONINFO](../menurc/versioninfo-resource.md)).</span><span class="sxs-lookup"><span data-stu-id="4ee77-111">The version number of the file (see [VERSIONINFO Resource](../menurc/versioninfo-resource.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ee77-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ee77-112">Remarks</span></span>

<span data-ttu-id="4ee77-113">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4ee77-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee77-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ee77-114">Requirements</span></span>



| <span data-ttu-id="4ee77-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ee77-115">Requirement</span></span> | <span data-ttu-id="4ee77-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4ee77-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee77-117">DLL</span><span class="sxs-lookup"><span data-stu-id="4ee77-117">DLL</span></span><br/> | <dl> <span data-ttu-id="4ee77-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ee77-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ee77-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ee77-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee77-120">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="4ee77-120">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 
