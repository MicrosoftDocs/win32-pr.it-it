---
description: Indica la versione di CTL3D attualmente in esecuzione.
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Ctl3dGetVer (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: e548d8933538ea85ba94f6e120032453079d69ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331671"
---
# <a name="ctl3dgetver-function"></a><span data-ttu-id="77047-103">Ctl3dGetVer (funzione)</span><span class="sxs-lookup"><span data-stu-id="77047-103">Ctl3dGetVer function</span></span>

<span data-ttu-id="77047-104">Indica la versione di CTL3D attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="77047-104">Indicates the version of CTL3D that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="77047-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77047-105">Syntax</span></span>


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a><span data-ttu-id="77047-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="77047-106">Parameters</span></span>

<span data-ttu-id="77047-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="77047-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="77047-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77047-108">Return value</span></span>

<span data-ttu-id="77047-109">Restituisce un valore che contiene il numero di versione principale nel byte di ordine superiore e il numero di versione secondario nel byte di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="77047-109">Returns a value that contains the major version number in the high-order byte and the minor version number in the low-order byte.</span></span>

## <a name="remarks"></a><span data-ttu-id="77047-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="77047-110">Remarks</span></span>

<span data-ttu-id="77047-111">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="77047-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="77047-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77047-112">Requirements</span></span>



| <span data-ttu-id="77047-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="77047-113">Requirement</span></span> | <span data-ttu-id="77047-114">Valore</span><span class="sxs-lookup"><span data-stu-id="77047-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77047-115">DLL</span><span class="sxs-lookup"><span data-stu-id="77047-115">DLL</span></span><br/> | <dl> <span data-ttu-id="77047-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77047-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
