---
description: Recupera l'elenco di set di CPU nel set predefinito del processo impostato da SetProcessDefaultCpuSets. Se per un determinato processo non è impostato alcun set di CPU predefinito, RequiredIdCount viene impostato su 0 e la funzione ha esito positivo.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: Funzione GetProcessDefaultCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: a5bd7c27b76efbbac923317837ac82b3a6700197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311988"
---
# <a name="getprocessdefaultcpusets-function"></a><span data-ttu-id="ac1d6-104">GetProcessDefaultCpuSets (funzione)</span><span class="sxs-lookup"><span data-stu-id="ac1d6-104">GetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="ac1d6-105">Recupera l'elenco di set di CPU nel set predefinito del processo impostato da [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md).</span><span class="sxs-lookup"><span data-stu-id="ac1d6-105">Retrieves the list of CPU Sets in the process default set that was set by [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md).</span></span> <span data-ttu-id="ac1d6-106">Se per un determinato processo non è impostato alcun set di CPU predefinito, **RequiredIdCount** viene impostato su 0 e la funzione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ac1d6-106">If no default CPU Sets are set for a given process, then the **RequiredIdCount** is set to 0 and the function succeeds.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1d6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac1d6-107">Syntax</span></span>


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="ac1d6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac1d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac1d6-109">*Processo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ac1d6-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1d6-110">Specifica un handle di processo per il processo su cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="ac1d6-110">Specifies a process handle for the process to query.</span></span> <span data-ttu-id="ac1d6-111">Questo handle deve avere il \_ diritto di \_ accesso alle informazioni limitato per le query di processo \_ .</span><span class="sxs-lookup"><span data-stu-id="ac1d6-111">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="ac1d6-112">Il valore restituito da [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) può anche essere specificato qui.</span><span class="sxs-lookup"><span data-stu-id="ac1d6-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="ac1d6-113">*CpuSetIds* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ac1d6-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1d6-114">Specifica un buffer facoltativo per recuperare l'elenco degli identificatori del set di CPU.</span><span class="sxs-lookup"><span data-stu-id="ac1d6-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="ac1d6-115">*CpuSetIdCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac1d6-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1d6-116">Specifica la capacità del buffer specificato in **CpuSetIds**.</span><span class="sxs-lookup"><span data-stu-id="ac1d6-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="ac1d6-117">Se il buffer è NULL, deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="ac1d6-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="ac1d6-118">*RequiredIdCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ac1d6-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1d6-119">Specifica la capacità necessaria del buffer per memorizzare l'intero elenco di set di CPU predefiniti del processo.</span><span class="sxs-lookup"><span data-stu-id="ac1d6-119">Specifies the required capacity of the buffer to hold the entire list of process default CPU Sets.</span></span> <span data-ttu-id="ac1d6-120">In esito positivo, specifica il numero di ID inseriti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="ac1d6-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac1d6-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac1d6-121">Return value</span></span>

<span data-ttu-id="ac1d6-122">Questa API restituisce TRUE in seguito all'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ac1d6-122">This API returns TRUE on success.</span></span> <span data-ttu-id="ac1d6-123">Se il buffer non è sufficientemente grande, l'API restituisce FALSE e il valore **GetLastError** è un errore di \_ buffer insufficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="ac1d6-123">If the buffer is not large enough the API returns FALSE, and the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="ac1d6-124">Questa API non può avere esito negativo se vengono passati parametri validi e il buffer restituito è sufficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="ac1d6-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac1d6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac1d6-125">Requirements</span></span>



| <span data-ttu-id="ac1d6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac1d6-126">Requirement</span></span> | <span data-ttu-id="ac1d6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ac1d6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1d6-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac1d6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ac1d6-129">App desktop di Windows 10 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ac1d6-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="ac1d6-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac1d6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ac1d6-131">App UWP per \[ app desktop di Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="ac1d6-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="ac1d6-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac1d6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac1d6-133"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac1d6-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="ac1d6-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="ac1d6-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac1d6-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac1d6-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="ac1d6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ac1d6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac1d6-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac1d6-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

