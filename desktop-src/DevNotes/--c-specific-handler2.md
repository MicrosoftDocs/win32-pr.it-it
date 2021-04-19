---
description: Chiamato dal compilatore per implementare estensioni di gestione delle eccezioni strutturate.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: Funzione __C_specific_handler (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326686"
---
# <a name="__c_specific_handler-function"></a><span data-ttu-id="2c01d-103">\_\_\_Funzione del gestore specifico di C \_</span><span class="sxs-lookup"><span data-stu-id="2c01d-103">\_\_C\_specific\_handler function</span></span>

<span data-ttu-id="2c01d-104">Chiamato dal compilatore per implementare estensioni di gestione delle eccezioni strutturate.</span><span class="sxs-lookup"><span data-stu-id="2c01d-104">Called by the compiler to implement structured exception handling extensions.</span></span>

<span data-ttu-id="2c01d-105">L'indirizzo relativo del gestore specifico del linguaggio è presente nelle informazioni di rimozione \_ ogni volta che Flags Unw \_ flag \_ EHANDLER o Unw \_ flag \_ UHANDLER sono impostati.</span><span class="sxs-lookup"><span data-stu-id="2c01d-105">The relative address of the language specific handler is present in the UNWIND\_INFO whenever flags UNW\_FLAG\_EHANDLER or UNW\_FLAG\_UHANDLER are set.</span></span> <span data-ttu-id="2c01d-106">Il gestore specifico del linguaggio viene chiamato come parte della ricerca di un gestore di eccezioni o come parte di una rimozione.</span><span class="sxs-lookup"><span data-stu-id="2c01d-106">The language specific handler is called as part of the search for an exception handler or as part of an unwind.</span></span> <span data-ttu-id="2c01d-107">Per ulteriori informazioni, vedere [gestore specifico del linguaggio](/cpp/build/language-specific-handler).</span><span class="sxs-lookup"><span data-stu-id="2c01d-107">For more information see [Language Specific Handler](/cpp/build/language-specific-handler).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c01d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c01d-108">Syntax</span></span>


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a><span data-ttu-id="2c01d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c01d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c01d-110">*ExceptionRecord* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c01d-110">*ExceptionRecord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c01d-111">Fornisce un puntatore a un record di eccezione, che ha la definizione Win64 standard.</span><span class="sxs-lookup"><span data-stu-id="2c01d-111">Supplies a pointer to an exception record, which has the standard Win64 definition.</span></span>

</dd> <dt>

<span data-ttu-id="2c01d-112">*EstablisherFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c01d-112">*EstablisherFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c01d-113">Indirizzo della base dell'allocazione dello stack fisso per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="2c01d-113">The address of the base of the fixed stack allocation for this function.</span></span>

</dd> <dt>

<span data-ttu-id="2c01d-114">*ContextRecord* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2c01d-114">*ContextRecord* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c01d-115">Punta al contesto dell'eccezione nel momento in cui è stata generata l'eccezione (nel caso del gestore di eccezioni) o nel contesto di rimozione corrente (nel caso del gestore di terminazione).</span><span class="sxs-lookup"><span data-stu-id="2c01d-115">Points to the exception context at the time the exception was raised (in the exception handler case) or the current "unwind" context (in the termination handler case).</span></span>

</dd> <dt>

<span data-ttu-id="2c01d-116">*DispatcherContext* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2c01d-116">*DispatcherContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c01d-117">Punta al contesto del dispatcher per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="2c01d-117">Points to the dispatcher context for this function.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c01d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c01d-118">Requirements</span></span>



| <span data-ttu-id="2c01d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c01d-119">Requirement</span></span> | <span data-ttu-id="2c01d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2c01d-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c01d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c01d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2c01d-122"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c01d-122"><dt>Wdm.h</dt></span></span> </dl>        |
| <span data-ttu-id="2c01d-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="2c01d-123">Library</span></span><br/> | <dl> <span data-ttu-id="2c01d-124"><dt>NtosKrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c01d-124"><dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="2c01d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2c01d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c01d-126"><dt>Ntoskrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c01d-126"><dt>Ntoskrnl.exe</dt></span></span> </dl> |



 

