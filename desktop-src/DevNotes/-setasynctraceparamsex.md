---
description: Completa la configurazione di un buffer di traccia con campi facoltativi per le tracce di tipo sprintf.
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: SetAsyncTraceParamsEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326837"
---
# <a name="setasynctraceparamsex-function"></a><span data-ttu-id="a529a-103">SetAsyncTraceParamsEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="a529a-103">SetAsyncTraceParamsEx function</span></span>

<span data-ttu-id="a529a-104">Completa la configurazione di un buffer di traccia con campi facoltativi per le tracce di tipo **sprintf**.</span><span class="sxs-lookup"><span data-stu-id="a529a-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="a529a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a529a-105">Syntax</span></span>


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a><span data-ttu-id="a529a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a529a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a529a-107">*pszModule*</span><span class="sxs-lookup"><span data-stu-id="a529a-107">*pszModule*</span></span> 
</dt> <dd>

<span data-ttu-id="a529a-108">Nome del modulo associato alla traccia.</span><span class="sxs-lookup"><span data-stu-id="a529a-108">The name of the module that is associated with the trace.</span></span>

</dd> <dt>

<span data-ttu-id="a529a-109">*pszFile*</span><span class="sxs-lookup"><span data-stu-id="a529a-109">*pszFile*</span></span> 
</dt> <dd>

<span data-ttu-id="a529a-110">Nome del file di origine che contiene l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="a529a-110">The name of the source file that contains the exception.</span></span>

</dd> <dt>

<span data-ttu-id="a529a-111">*lLine*</span><span class="sxs-lookup"><span data-stu-id="a529a-111">*lLine*</span></span> 
</dt> <dd>

<span data-ttu-id="a529a-112">Numero di riga dell'eccezione nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="a529a-112">The line number of the exception in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="a529a-113">*pszFunction*</span><span class="sxs-lookup"><span data-stu-id="a529a-113">*pszFunction*</span></span> 
</dt> <dd>

<span data-ttu-id="a529a-114">Nome della funzione dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="a529a-114">The function name of the exception.</span></span>

</dd> <dt>

<span data-ttu-id="a529a-115">*dwTraceMask*</span><span class="sxs-lookup"><span data-stu-id="a529a-115">*dwTraceMask*</span></span> 
</dt> <dd>

<span data-ttu-id="a529a-116">Costante di un flag di traccia che rappresenta uno dei tipi di traccia disponibili.</span><span class="sxs-lookup"><span data-stu-id="a529a-116">A trace flag constant that represents one of the available trace types.</span></span> <span data-ttu-id="a529a-117">Questo parametro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a529a-117">This parameter can be any of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a529a-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**Errore irreversibile \_ \_Maschera di traccia** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a529a-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL\_TRACE\_MASK** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="a529a-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Errore \_ \_Maschera di traccia** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="a529a-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERROR\_TRACE\_MASK** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="a529a-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Esegui debug \_ \_Maschera di traccia** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="a529a-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG\_TRACE\_MASK** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="a529a-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**Stato \_ di \_Maschera di traccia** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="a529a-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE\_TRACE\_MASK** (0x00000008)</span></span>
</dt> <dt>

<span data-ttu-id="a529a-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>Funzione **\_ \_Maschera di traccia** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="a529a-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT\_TRACE\_MASK** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="a529a-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Messaggio \_ di \_Maschera di traccia** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="a529a-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE\_TRACE\_MASK** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="a529a-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Tutto \_ \_Maschera di traccia** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="a529a-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL\_TRACE\_MASK** (0xFFFFFFFF)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a529a-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a529a-125">Return value</span></span>

<span data-ttu-id="a529a-126">Questa funzione restituisce 1 se la funzione ha esito positivo; in caso contrario, restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="a529a-126">This function returns 1 if the function succeeds; otherwise, it returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="a529a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="a529a-127">Remarks</span></span>

<span data-ttu-id="a529a-128">Exstrace.dll è un componente facoltativo che viene installato con il Simple Mail Transfer Protocol (SMTP) e il protocollo NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="a529a-128">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="a529a-129">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a529a-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a529a-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a529a-130">Requirements</span></span>



| <span data-ttu-id="a529a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a529a-131">Requirement</span></span> | <span data-ttu-id="a529a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a529a-132">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a529a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a529a-133">DLL</span></span><br/> | <dl> <span data-ttu-id="a529a-134"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a529a-134"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
