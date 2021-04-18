---
description: Deprecato. Regola una data in base a un numero di anni, mesi, settimane o giorni specificato.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: AdjustCalendarDate (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: ce2f61fd7d7d6354130873b5b2b2376c856e3958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306619"
---
# <a name="adjustcalendardate-function"></a><span data-ttu-id="2c171-104">AdjustCalendarDate (funzione)</span><span class="sxs-lookup"><span data-stu-id="2c171-104">AdjustCalendarDate function</span></span>

<span data-ttu-id="2c171-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="2c171-105">Deprecated.</span></span> <span data-ttu-id="2c171-106">Regola una data in base a un numero di anni, mesi, settimane o giorni specificato.</span><span class="sxs-lookup"><span data-stu-id="2c171-106">Adjusts a date by a specified number of years, months, weeks, or days.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c171-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c171-107">Syntax</span></span>


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a><span data-ttu-id="2c171-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c171-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c171-109">*lpCalDateTime* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2c171-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c171-110">Puntatore a una struttura [**CALDATETIME**](caldatetime.md) che contiene le informazioni sulla data e sul calendario da regolare.</span><span class="sxs-lookup"><span data-stu-id="2c171-110">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to adjust.</span></span>

</dd> <dt>

<span data-ttu-id="2c171-111">*Calunit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c171-111">*calUnit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c171-112">Valore di enumerazione [**\_ DATEUNIT CALDATETIME**](caldatetime-dateunit.md) che indica l'unità di data, ad esempio DayUnit.</span><span class="sxs-lookup"><span data-stu-id="2c171-112">The [**CALDATETIME\_DATEUNIT**](caldatetime-dateunit.md) enumeration value indicating the date unit, for example, DayUnit.</span></span>

</dd> <dt>

<span data-ttu-id="2c171-113">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="2c171-113">*amount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c171-114">Valore in base al quale modificare la data specificata.</span><span class="sxs-lookup"><span data-stu-id="2c171-114">The amount by which to adjust the specified date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c171-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c171-115">Return value</span></span>

<span data-ttu-id="2c171-116">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2c171-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="2c171-117">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c171-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="2c171-118">\_Data di errore non \_ compresa nell' \_ \_ intervallo.</span><span class="sxs-lookup"><span data-stu-id="2c171-118">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="2c171-119">La data specificata non è compresa nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="2c171-119">The specified date was out of range.</span></span>
-   <span data-ttu-id="2c171-120">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="2c171-120">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="2c171-121">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="2c171-121">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c171-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c171-122">Remarks</span></span>

<span data-ttu-id="2c171-123">A questa funzione non è associato un file di intestazione o un file di libreria.</span><span class="sxs-lookup"><span data-stu-id="2c171-123">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="2c171-124">L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Kernel32.dll) per ottenere un handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="2c171-124">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="2c171-125">Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con l'handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.</span><span class="sxs-lookup"><span data-stu-id="2c171-125">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c171-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c171-126">Requirements</span></span>



| <span data-ttu-id="2c171-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c171-127">Requirement</span></span> | <span data-ttu-id="2c171-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2c171-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c171-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c171-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2c171-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c171-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2c171-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c171-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2c171-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2c171-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c171-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2c171-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c171-134"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c171-134"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c171-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c171-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c171-136">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="2c171-136">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="2c171-137">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="2c171-137">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="2c171-138">NLS: esempio di API basate su nome</span><span class="sxs-lookup"><span data-stu-id="2c171-138">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
