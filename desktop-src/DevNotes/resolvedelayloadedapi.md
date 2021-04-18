---
description: Individua la funzione di destinazione dell'importazione specificata e sostituisce il puntatore a funzione nel thunk di importazione con la destinazione dell'implementazione della funzione.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: ResolveDelayLoadedAPI (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 019729cacb45cce87de2cc4015c661c494125108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329577"
---
# <a name="resolvedelayloadedapi-function"></a><span data-ttu-id="3dd2e-103">ResolveDelayLoadedAPI (funzione)</span><span class="sxs-lookup"><span data-stu-id="3dd2e-103">ResolveDelayLoadedAPI function</span></span>

<span data-ttu-id="3dd2e-104">Individua la funzione di destinazione dell'importazione specificata e sostituisce il puntatore a funzione nel thunk di importazione con la destinazione dell'implementazione della funzione.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-104">Locates the target function of the specified import and replaces the function pointer in the import thunk with the target of the function implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd2e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3dd2e-105">Syntax</span></span>


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="3dd2e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3dd2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dd2e-107">*ParentModuleBase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dd2e-107">*ParentModuleBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd2e-108">Indirizzo della base del modulo che importa una funzione a caricamento ritardato.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-108">The address of the base of the module importing a delay-loaded function.</span></span>

</dd> <dt>

<span data-ttu-id="3dd2e-109">*DelayloadDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dd2e-109">*DelayloadDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd2e-110">Descrittore per il modulo da caricare.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-110">The descriptor for the module to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="3dd2e-111">*FailureDllHook* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3dd2e-111">*FailureDllHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd2e-112">Indirizzo dell'hook di errore.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-112">The address of the failure hook.</span></span> <span data-ttu-id="3dd2e-113">Vedere [**DelayLoadFailureHook**](delayloadfailurehook.md).</span><span class="sxs-lookup"><span data-stu-id="3dd2e-113">See [**DelayLoadFailureHook**](delayloadfailurehook.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd2e-114">*FailureSystemHook* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3dd2e-114">*FailureSystemHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd2e-115">Indirizzo dell'hook di errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-115">The address of the system failure hook.</span></span>

</dd> <dt>

<span data-ttu-id="3dd2e-116">*ThunkAddress* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3dd2e-116">*ThunkAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd2e-117">Dati del thunk per la funzione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-117">The thunk data for the target function.</span></span> <span data-ttu-id="3dd2e-118">Utilizzato per trovare la voce della tabella dei nomi specifica della funzione.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-118">Used to find the specific name table entry of the function.</span></span>

</dd> <dt>

<span data-ttu-id="3dd2e-119">*Flag*</span><span class="sxs-lookup"><span data-stu-id="3dd2e-119">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="3dd2e-120">Riservati deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-120">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dd2e-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3dd2e-121">Return value</span></span>

<span data-ttu-id="3dd2e-122">Indirizzo dell'importazione o dello stub dell'errore.</span><span class="sxs-lookup"><span data-stu-id="3dd2e-122">The address of the import, or the failure stub for it.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd2e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3dd2e-123">Requirements</span></span>



| <span data-ttu-id="3dd2e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dd2e-124">Requirement</span></span> | <span data-ttu-id="3dd2e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3dd2e-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd2e-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="3dd2e-126">Library</span></span><br/> | <dl> <span data-ttu-id="3dd2e-127"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dd2e-127"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3dd2e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3dd2e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="3dd2e-129"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dd2e-129"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd2e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3dd2e-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="3dd2e-131">[Supporto del linker per le DLL di Delay-Loaded](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="3dd2e-131">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




