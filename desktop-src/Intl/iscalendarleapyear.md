---
description: Deprecato. Indica se l'anno specificato è un anno bisestile nell'era specificata per il calendario specifico.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: IsCalendarLeapYear (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 484531f8107bacb70f9e24ba2537090317825e26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882134"
---
# <a name="iscalendarleapyear-function"></a><span data-ttu-id="22dc4-104">IsCalendarLeapYear (funzione)</span><span class="sxs-lookup"><span data-stu-id="22dc4-104">IsCalendarLeapYear function</span></span>

<span data-ttu-id="22dc4-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="22dc4-105">Deprecated.</span></span> <span data-ttu-id="22dc4-106">Indica se l'anno specificato è un anno bisestile nell'era specificata per il calendario specifico.</span><span class="sxs-lookup"><span data-stu-id="22dc4-106">Identifies whether the specified year is a leap year within the given era for the specific calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="22dc4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22dc4-107">Syntax</span></span>


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a><span data-ttu-id="22dc4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="22dc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22dc4-109">*CALID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22dc4-109">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22dc4-110">[Identificatore del calendario](calendar-identifiers.md) da utilizzare per il controllo dell'anno bisestile.</span><span class="sxs-lookup"><span data-stu-id="22dc4-110">The [calendar identifier](calendar-identifiers.md) to use for checking leap year.</span></span>

</dd> <dt>

<span data-ttu-id="22dc4-111">*anno* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22dc4-111">*year* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22dc4-112">Anno da verificare.</span><span class="sxs-lookup"><span data-stu-id="22dc4-112">The year to check.</span></span>

</dd> <dt>

<span data-ttu-id="22dc4-113">*era* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22dc4-113">*era* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22dc4-114">Era da verificare.</span><span class="sxs-lookup"><span data-stu-id="22dc4-114">The era to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22dc4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22dc4-115">Return value</span></span>

<span data-ttu-id="22dc4-116">Restituisce **true** se l'anno specificato è bisestile; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="22dc4-116">Returns **TRUE** if the specified year is a leap year, or **FALSE** otherwise.</span></span> <span data-ttu-id="22dc4-117">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="22dc4-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="22dc4-118">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="22dc4-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="22dc4-119">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="22dc4-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="22dc4-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="22dc4-120">Remarks</span></span>

<span data-ttu-id="22dc4-121">A questa funzione non è associato un file di intestazione o un file di libreria.</span><span class="sxs-lookup"><span data-stu-id="22dc4-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="22dc4-122">L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Kernel32.dll) per ottenere un handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="22dc4-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="22dc4-123">Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con tale handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.</span><span class="sxs-lookup"><span data-stu-id="22dc4-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="22dc4-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22dc4-124">Requirements</span></span>



| <span data-ttu-id="22dc4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="22dc4-125">Requirement</span></span> | <span data-ttu-id="22dc4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="22dc4-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22dc4-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22dc4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="22dc4-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22dc4-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="22dc4-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22dc4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="22dc4-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="22dc4-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="22dc4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="22dc4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22dc4-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22dc4-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22dc4-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22dc4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22dc4-134">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="22dc4-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="22dc4-135">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="22dc4-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> </dl>

 

 
