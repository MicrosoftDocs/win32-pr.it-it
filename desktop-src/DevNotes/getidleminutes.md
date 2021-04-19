---
description: Ottiene l'intervallo di tempo, in minuti, dall'ultima attività dell'utente.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: GetIdleMinutes (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: da3064ea96eb8e9835ed1e9d2f564bf922d2f091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326794"
---
# <a name="getidleminutes-function"></a><span data-ttu-id="21024-103">GetIdleMinutes (funzione)</span><span class="sxs-lookup"><span data-stu-id="21024-103">GetIdleMinutes function</span></span>

<span data-ttu-id="21024-104">\[Questa funzione non è supportata e può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="21024-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="21024-105">Usare invece la funzione **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="21024-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="21024-106">Ottiene l'intervallo di tempo, in minuti, dall'ultima attività dell'utente.</span><span class="sxs-lookup"><span data-stu-id="21024-106">Gets the length of time, in minutes, since the user's last activity.</span></span>

## <a name="syntax"></a><span data-ttu-id="21024-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21024-107">Syntax</span></span>


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="21024-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="21024-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21024-109">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="21024-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="21024-110">Questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="21024-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21024-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21024-111">Return value</span></span>

<span data-ttu-id="21024-112">Restituisce il numero di minuti trascorsi dall'ultima attività dell'utente.</span><span class="sxs-lookup"><span data-stu-id="21024-112">Returns the number of minutes since the user's last activity.</span></span>

## <a name="remarks"></a><span data-ttu-id="21024-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="21024-113">Remarks</span></span>

<span data-ttu-id="21024-114">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="21024-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="21024-115">Questa funzione non viene esportata per nome; specificare il numero ordinale 8 quando si chiama **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="21024-115">This function is not exported by name; specify ordinal 8 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="21024-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21024-116">Requirements</span></span>



| <span data-ttu-id="21024-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="21024-117">Requirement</span></span> | <span data-ttu-id="21024-118">Valore</span><span class="sxs-lookup"><span data-stu-id="21024-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21024-119">DLL</span><span class="sxs-lookup"><span data-stu-id="21024-119">DLL</span></span><br/> | <dl> <span data-ttu-id="21024-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21024-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21024-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21024-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21024-122">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="21024-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
