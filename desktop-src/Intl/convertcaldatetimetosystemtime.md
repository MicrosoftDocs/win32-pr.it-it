---
description: Deprecato. Converte una struttura CALDATETIME specificata in una struttura SYSTEMTIME.
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: ConvertCalDateTimeToSystemTime (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 9c317a31904e2d1b0b2110f6b2dc367ac3e2e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312874"
---
# <a name="convertcaldatetimetosystemtime-function"></a><span data-ttu-id="775ad-104">ConvertCalDateTimeToSystemTime (funzione)</span><span class="sxs-lookup"><span data-stu-id="775ad-104">ConvertCalDateTimeToSystemTime function</span></span>

<span data-ttu-id="775ad-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="775ad-105">Deprecated.</span></span> <span data-ttu-id="775ad-106">Converte una struttura [**CALDATETIME**](caldatetime.md) specificata in una struttura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="775ad-106">Converts a specified [**CALDATETIME**](caldatetime.md) structure to a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="775ad-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="775ad-107">Syntax</span></span>


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a><span data-ttu-id="775ad-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="775ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="775ad-109">*lpCalDateTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="775ad-109">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="775ad-110">Puntatore alla struttura [**CALDATETIME**](caldatetime.md) da convertire.</span><span class="sxs-lookup"><span data-stu-id="775ad-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="775ad-111">*lpSysTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="775ad-111">*lpSysTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="775ad-112">Puntatore alla struttura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) equivalente.</span><span class="sxs-lookup"><span data-stu-id="775ad-112">Pointer to the equivalent [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="775ad-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="775ad-113">Return value</span></span>

<span data-ttu-id="775ad-114">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="775ad-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="775ad-115">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="775ad-115">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="775ad-116">\_Data di errore non \_ compresa nell' \_ \_ intervallo.</span><span class="sxs-lookup"><span data-stu-id="775ad-116">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="775ad-117">La data specificata non è compresa nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="775ad-117">The specified date was out of range.</span></span>
-   <span data-ttu-id="775ad-118">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="775ad-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="775ad-119">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="775ad-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="775ad-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="775ad-120">Remarks</span></span>

<span data-ttu-id="775ad-121">A questa funzione non è associato un file di intestazione o un file di libreria.</span><span class="sxs-lookup"><span data-stu-id="775ad-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="775ad-122">L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Kernel32.dll) per ottenere un handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="775ad-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="775ad-123">Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con l'handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.</span><span class="sxs-lookup"><span data-stu-id="775ad-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="775ad-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="775ad-124">Requirements</span></span>



| <span data-ttu-id="775ad-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="775ad-125">Requirement</span></span> | <span data-ttu-id="775ad-126">Valore</span><span class="sxs-lookup"><span data-stu-id="775ad-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="775ad-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="775ad-127">Minimum supported client</span></span><br/> | <span data-ttu-id="775ad-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="775ad-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="775ad-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="775ad-129">Minimum supported server</span></span><br/> | <span data-ttu-id="775ad-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="775ad-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="775ad-131">DLL</span><span class="sxs-lookup"><span data-stu-id="775ad-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="775ad-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="775ad-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="775ad-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="775ad-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="775ad-134">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="775ad-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="775ad-135">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="775ad-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="775ad-136">Recupero di informazioni su data e ora</span><span class="sxs-lookup"><span data-stu-id="775ad-136">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
