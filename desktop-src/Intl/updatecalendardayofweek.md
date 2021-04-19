---
description: Deprecato. Ottiene il giorno della settimana che corrisponde a un giorno specificato e popola il membro DayOfWeek nella struttura CALDATETIME specificata con tale valore.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: UpdateCalendarDayOfWeek (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 316af539e6ca0476f0f8d575a160fcd7c3219e90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319486"
---
# <a name="updatecalendardayofweek-function"></a><span data-ttu-id="4a859-104">UpdateCalendarDayOfWeek (funzione)</span><span class="sxs-lookup"><span data-stu-id="4a859-104">UpdateCalendarDayOfWeek function</span></span>

<span data-ttu-id="4a859-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4a859-105">Deprecated.</span></span> <span data-ttu-id="4a859-106">Ottiene il giorno della settimana che corrisponde a un giorno specificato e popola il membro **DayOfWeek** nella struttura [**CALDATETIME**](caldatetime.md) specificata con tale valore.</span><span class="sxs-lookup"><span data-stu-id="4a859-106">Gets the day of the week that corresponds to a specified day and populates the **DayOfWeek** member in the specified [**CALDATETIME**](caldatetime.md) structure with that value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a859-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a859-107">Syntax</span></span>


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="4a859-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a859-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a859-109">*lpCalDateTime* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4a859-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a859-110">Puntatore alla struttura [**CALDATETIME**](caldatetime.md) contenente la data in cui impostare il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="4a859-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure containing the date for which to set the day of the week.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a859-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a859-111">Return value</span></span>

<span data-ttu-id="4a859-112">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4a859-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="4a859-113">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="4a859-113">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="4a859-114">\_Data di errore non \_ compresa nell' \_ \_ intervallo.</span><span class="sxs-lookup"><span data-stu-id="4a859-114">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="4a859-115">La data specificata non è compresa nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="4a859-115">The specified date was out of range.</span></span>
-   <span data-ttu-id="4a859-116">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="4a859-116">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="4a859-117">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="4a859-117">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a859-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a859-118">Remarks</span></span>

<span data-ttu-id="4a859-119">A questa funzione non è associato un file di intestazione o un file di libreria.</span><span class="sxs-lookup"><span data-stu-id="4a859-119">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="4a859-120">L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Kernel32.dll) per ottenere un handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="4a859-120">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="4a859-121">Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con tale handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.</span><span class="sxs-lookup"><span data-stu-id="4a859-121">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a859-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a859-122">Requirements</span></span>



| <span data-ttu-id="4a859-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a859-123">Requirement</span></span> | <span data-ttu-id="4a859-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4a859-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a859-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a859-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4a859-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a859-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4a859-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a859-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4a859-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a859-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4a859-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4a859-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a859-130"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a859-130"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a859-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a859-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a859-132">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="4a859-132">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="4a859-133">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="4a859-133">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="4a859-134">**CALDATETIME**</span><span class="sxs-lookup"><span data-stu-id="4a859-134">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
