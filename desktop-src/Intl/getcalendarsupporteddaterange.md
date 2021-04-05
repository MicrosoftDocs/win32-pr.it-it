---
description: Deprecato. Ottiene l'intervallo di date supportato per un calendario specificato.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: GetCalendarSupportedDateRange (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 57b1175ef7bcf5b6b5d91af63682ca565bc0f1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967917"
---
# <a name="getcalendarsupporteddaterange-function"></a><span data-ttu-id="7ae41-104">GetCalendarSupportedDateRange (funzione)</span><span class="sxs-lookup"><span data-stu-id="7ae41-104">GetCalendarSupportedDateRange function</span></span>

<span data-ttu-id="7ae41-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7ae41-105">Deprecated.</span></span> <span data-ttu-id="7ae41-106">Ottiene l'intervallo di date supportato per un calendario specificato.</span><span class="sxs-lookup"><span data-stu-id="7ae41-106">Gets the supported date range for a specified calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae41-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ae41-107">Syntax</span></span>


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="7ae41-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ae41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ae41-109">*Calendario* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ae41-109">*Calendar* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae41-110">[Identificatore del calendario](calendar-identifiers.md) per il quale ottenere l'intervallo di date supportato.</span><span class="sxs-lookup"><span data-stu-id="7ae41-110">[Calendar identifier](calendar-identifiers.md) for which to get the supported date range.</span></span>

</dd> <dt>

<span data-ttu-id="7ae41-111">*lpCalMinDateTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ae41-111">*lpCalMinDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae41-112">Puntatore a una struttura [**CALDATETIME**](caldatetime.md) che definisce la data minima supportata.</span><span class="sxs-lookup"><span data-stu-id="7ae41-112">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the minimum supported date.</span></span>

</dd> <dt>

<span data-ttu-id="7ae41-113">*lpCalMaxDateTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ae41-113">*lpCalMaxDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae41-114">Puntatore a una struttura [**CALDATETIME**](caldatetime.md) che definisce la data massima supportata.</span><span class="sxs-lookup"><span data-stu-id="7ae41-114">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the maximum supported date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ae41-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ae41-115">Return value</span></span>

<span data-ttu-id="7ae41-116">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7ae41-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="7ae41-117">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ae41-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="7ae41-118">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="7ae41-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="7ae41-119">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="7ae41-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae41-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ae41-120">Remarks</span></span>

<span data-ttu-id="7ae41-121">La data meno recente supportata da questa funzione è il 1 gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="7ae41-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="7ae41-122">A questa funzione non è associato un file di intestazione o un file di libreria.</span><span class="sxs-lookup"><span data-stu-id="7ae41-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="7ae41-123">L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Kernel32.dll) per ottenere un handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="7ae41-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="7ae41-124">Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con l'handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.</span><span class="sxs-lookup"><span data-stu-id="7ae41-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae41-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ae41-125">Requirements</span></span>



| <span data-ttu-id="7ae41-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ae41-126">Requirement</span></span> | <span data-ttu-id="7ae41-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7ae41-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae41-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ae41-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7ae41-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ae41-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7ae41-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ae41-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7ae41-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ae41-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7ae41-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7ae41-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ae41-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ae41-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ae41-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ae41-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae41-135">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="7ae41-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="7ae41-136">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="7ae41-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="7ae41-137">NLS: esempio di API basate su nome</span><span class="sxs-lookup"><span data-stu-id="7ae41-137">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
