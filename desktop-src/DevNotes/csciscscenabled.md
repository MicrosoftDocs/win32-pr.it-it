---
description: Determina se File offline è abilitato.
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: CSCIsCSCEnabled (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 13db7ebbb11f678c00a5a755ffe8114f8684b315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331193"
---
# <a name="csciscscenabled-function"></a><span data-ttu-id="a99d8-103">CSCIsCSCEnabled (funzione)</span><span class="sxs-lookup"><span data-stu-id="a99d8-103">CSCIsCSCEnabled function</span></span>

<span data-ttu-id="a99d8-104">\[Questa funzione non è supportata e non deve essere utilizzata.\]</span><span class="sxs-lookup"><span data-stu-id="a99d8-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="a99d8-105">Determina se File offline è abilitato.</span><span class="sxs-lookup"><span data-stu-id="a99d8-105">Determines whether Offline Files is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="a99d8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a99d8-106">Syntax</span></span>


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="a99d8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a99d8-107">Parameters</span></span>

<span data-ttu-id="a99d8-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="a99d8-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a99d8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a99d8-109">Return value</span></span>

<span data-ttu-id="a99d8-110">Questa funzione restituisce **true** se file offline è abilitato e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a99d8-110">This function returns **TRUE** if Offline Files is enabled and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a99d8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a99d8-111">Remarks</span></span>

<span data-ttu-id="a99d8-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a99d8-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a99d8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a99d8-113">Requirements</span></span>



| <span data-ttu-id="a99d8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a99d8-114">Requirement</span></span> | <span data-ttu-id="a99d8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a99d8-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a99d8-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a99d8-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a99d8-117"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a99d8-117"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a99d8-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a99d8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a99d8-119">**CSCQueryDatabaseStatus**</span><span class="sxs-lookup"><span data-stu-id="a99d8-119">**CSCQueryDatabaseStatus**</span></span>](cscquerydatabasestatus.md)
</dt> </dl>

 

 
