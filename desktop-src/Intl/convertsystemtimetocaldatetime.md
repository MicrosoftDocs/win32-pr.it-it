---
description: Deprecato. Converte una struttura SYSTEMTIME specificata in una struttura CALDATETIME.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: ConvertSystemTimeToCalDateTime (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 738899c7307797f0edeade93f7e4e706919be900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312875"
---
# <a name="convertsystemtimetocaldatetime-function"></a><span data-ttu-id="bb21f-104">ConvertSystemTimeToCalDateTime (funzione)</span><span class="sxs-lookup"><span data-stu-id="bb21f-104">ConvertSystemTimeToCalDateTime function</span></span>

<span data-ttu-id="bb21f-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="bb21f-105">Deprecated.</span></span> <span data-ttu-id="bb21f-106">Converte una struttura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) specificata in una struttura [**CALDATETIME**](caldatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="bb21f-106">Converts a specified [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to a [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb21f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb21f-107">Syntax</span></span>


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a><span data-ttu-id="bb21f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb21f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb21f-109">*lpSysTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb21f-109">*lpSysTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb21f-110">Puntatore alla struttura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) da convertire.</span><span class="sxs-lookup"><span data-stu-id="bb21f-110">Pointer to the [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="bb21f-111">*CALID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb21f-111">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb21f-112">Identificatore del [Calendario](calendar-identifiers.md) di sistema da utilizzare nella conversione.</span><span class="sxs-lookup"><span data-stu-id="bb21f-112">The system [calendar identifier](calendar-identifiers.md) to use in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="bb21f-113">*lpCalDateTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bb21f-113">*lpCalDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb21f-114">Puntatore alla struttura [**CALDATETIME**](caldatetime.md) equivalente.</span><span class="sxs-lookup"><span data-stu-id="bb21f-114">Pointer to the equivalent [**CALDATETIME**](caldatetime.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb21f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb21f-115">Return value</span></span>

<span data-ttu-id="bb21f-116">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bb21f-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="bb21f-117">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb21f-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="bb21f-118">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="bb21f-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="bb21f-119">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="bb21f-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb21f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb21f-120">Remarks</span></span>

<span data-ttu-id="bb21f-121">La data meno recente supportata da questa funzione è il 1 gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="bb21f-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="bb21f-122">A questa funzione non è associato un file di intestazione o un file di libreria.</span><span class="sxs-lookup"><span data-stu-id="bb21f-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="bb21f-123">L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Kernel32.dll) per ottenere un handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="bb21f-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="bb21f-124">Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con l'handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.</span><span class="sxs-lookup"><span data-stu-id="bb21f-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb21f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb21f-125">Requirements</span></span>



| <span data-ttu-id="bb21f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb21f-126">Requirement</span></span> | <span data-ttu-id="bb21f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="bb21f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb21f-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb21f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bb21f-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb21f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bb21f-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb21f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bb21f-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bb21f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb21f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bb21f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb21f-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb21f-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb21f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb21f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb21f-135">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="bb21f-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="bb21f-136">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="bb21f-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="bb21f-137">Recupero di informazioni su data e ora</span><span class="sxs-lookup"><span data-stu-id="bb21f-137">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
