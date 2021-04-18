---
description: Termina il monitoraggio dell'inattività.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: EndIdleDetection (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: e50679c53123ad140324f7d159ef938367c02af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328565"
---
# <a name="endidledetection-function"></a><span data-ttu-id="92a52-103">EndIdleDetection (funzione)</span><span class="sxs-lookup"><span data-stu-id="92a52-103">EndIdleDetection function</span></span>

<span data-ttu-id="92a52-104">\[Questa funzione non è supportata e può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="92a52-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="92a52-105">Usare invece la funzione **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="92a52-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="92a52-106">Termina il monitoraggio dell'inattività.</span><span class="sxs-lookup"><span data-stu-id="92a52-106">Ends monitoring of inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a52-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92a52-107">Syntax</span></span>


```C++
BOOL WINAPI EndIdleDetection(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="92a52-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="92a52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a52-109">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="92a52-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="92a52-110">Questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="92a52-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a52-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92a52-111">Return value</span></span>

<span data-ttu-id="92a52-112">Restituisce **true** se la funzione ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="92a52-112">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a52-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="92a52-113">Remarks</span></span>

<span data-ttu-id="92a52-114">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="92a52-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="92a52-115">Questa funzione non viene esportata per nome; specificare il numero ordinale 4 quando si chiama **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="92a52-115">This function is not exported by name; specify ordinal 4 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92a52-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92a52-116">Requirements</span></span>



| <span data-ttu-id="92a52-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="92a52-117">Requirement</span></span> | <span data-ttu-id="92a52-118">Valore</span><span class="sxs-lookup"><span data-stu-id="92a52-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92a52-119">DLL</span><span class="sxs-lookup"><span data-stu-id="92a52-119">DLL</span></span><br/> | <dl> <span data-ttu-id="92a52-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a52-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92a52-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92a52-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a52-122">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="92a52-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
