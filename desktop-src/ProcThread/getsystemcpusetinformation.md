---
description: Consente a un'applicazione di eseguire una query sui set di CPU disponibili nel sistema e il relativo stato corrente.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: Funzione GetSystemCpuSetInformation (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d8ce490e3377e45a81b24523504d06941755de49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231521"
---
# <a name="getsystemcpusetinformation-function"></a><span data-ttu-id="61da8-103">GetSystemCpuSetInformation (funzione)</span><span class="sxs-lookup"><span data-stu-id="61da8-103">GetSystemCpuSetInformation function</span></span>

<span data-ttu-id="61da8-104">Consente a un'applicazione di eseguire una query sui set di CPU disponibili nel sistema e il relativo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="61da8-104">Allows an application to query the available CPU Sets on the system, and their current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="61da8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61da8-105">Syntax</span></span>


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a><span data-ttu-id="61da8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="61da8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61da8-107">*Informazioni* \[ su out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="61da8-107">*Information* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61da8-108">Puntatore a una struttura [**di \_ \_ \_ informazioni del set di CPU di sistema**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) che riceve i dati del set di CPU.</span><span class="sxs-lookup"><span data-stu-id="61da8-108">A pointer to a [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure that receives the CPU Set data.</span></span> <span data-ttu-id="61da8-109">Passare NULL con una lunghezza del buffer di 0 per determinare le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="61da8-109">Pass NULL with a buffer length of 0 to determine the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="61da8-110">*BufferLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61da8-110">*BufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61da8-111">Lunghezza, in byte, del buffer di output passato come argomento Information.</span><span class="sxs-lookup"><span data-stu-id="61da8-111">The length, in bytes, of the output buffer passed as the Information argument.</span></span>

</dd> <dt>

<span data-ttu-id="61da8-112">*ReturnedLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="61da8-112">*ReturnedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61da8-113">Lunghezza, in byte, dei dati validi nel buffer di output se il buffer è sufficientemente grande o la dimensione richiesta del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="61da8-113">The length, in bytes, of the valid data in the output buffer if the buffer is large enough, or the required size of the output buffer.</span></span> <span data-ttu-id="61da8-114">Se non sono presenti set di CPU, questo valore sarà 0.</span><span class="sxs-lookup"><span data-stu-id="61da8-114">If no CPU Sets exist, this value will be 0.</span></span>

</dd> <dt>

<span data-ttu-id="61da8-115">*Processo* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="61da8-115">*Process* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61da8-116">Handle facoltativo per un processo.</span><span class="sxs-lookup"><span data-stu-id="61da8-116">An optional handle to a process.</span></span> <span data-ttu-id="61da8-117">Questo processo viene utilizzato per determinare il valore del flag **AllocatedToTargetProcess** nella struttura delle informazioni del set di CPU del sistema \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="61da8-117">This process is used to determine the value of the **AllocatedToTargetProcess** flag in the SYSTEM\_CPU\_SET\_INFORMATION structure.</span></span> <span data-ttu-id="61da8-118">Se un set di CPU viene allocato al processo specificato, il flag viene impostato.</span><span class="sxs-lookup"><span data-stu-id="61da8-118">If a CPU Set is allocated to the specified process, the flag is set.</span></span> <span data-ttu-id="61da8-119">In caso contrario, è chiaro.</span><span class="sxs-lookup"><span data-stu-id="61da8-119">Otherwise, it is clear.</span></span> <span data-ttu-id="61da8-120">Questo handle deve avere il \_ diritto di \_ accesso alle informazioni limitato per le query di processo \_ .</span><span class="sxs-lookup"><span data-stu-id="61da8-120">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="61da8-121">Il valore restituito da [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) può anche essere specificato qui.</span><span class="sxs-lookup"><span data-stu-id="61da8-121">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) may also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="61da8-122">*Flag*</span><span class="sxs-lookup"><span data-stu-id="61da8-122">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="61da8-123">Riservato, deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="61da8-123">Reserved, must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61da8-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61da8-124">Return value</span></span>

<span data-ttu-id="61da8-125">Se l'API ha esito positivo, restituisce TRUE.</span><span class="sxs-lookup"><span data-stu-id="61da8-125">If the API succeeds it returns TRUE.</span></span> <span data-ttu-id="61da8-126">Se ha esito negativo, il motivo dell'errore è disponibile tramite **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="61da8-126">If it fails, the error reason is available through **GetLastError**.</span></span> <span data-ttu-id="61da8-127">Se il buffer delle informazioni è NULL o non è sufficientemente grande, viene restituito l'errore del codice di errore \_ insufficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="61da8-127">If the Information buffer was NULL or not large enough, the error code ERROR\_INSUFFICIENT\_BUFFER is returned.</span></span> <span data-ttu-id="61da8-128">Questa API non può avere esito negativo se vengono passati parametri validi e un buffer sufficientemente grande da conservare tutti i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="61da8-128">This API cannot fail when passed valid parameters and a buffer that is large enough to hold all of the return data.</span></span>

## <a name="requirements"></a><span data-ttu-id="61da8-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61da8-129">Requirements</span></span>



| <span data-ttu-id="61da8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="61da8-130">Requirement</span></span> | <span data-ttu-id="61da8-131">Valore</span><span class="sxs-lookup"><span data-stu-id="61da8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="61da8-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61da8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="61da8-133">App desktop di Windows 10 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="61da8-133">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="61da8-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61da8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="61da8-135">App UWP per \[ app desktop di Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="61da8-135">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="61da8-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61da8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="61da8-137"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="61da8-137"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="61da8-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="61da8-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="61da8-139"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="61da8-139"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="61da8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="61da8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61da8-141"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61da8-141"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

