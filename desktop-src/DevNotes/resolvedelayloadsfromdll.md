---
description: Invia il lavoro di risoluzione delle importazioni a caricamento ritardato dal file binario padre a un file binario di destinazione.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: ResolveDelayLoadsFromDll (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: a0fb517de7384a964c21c9e1a0a3e695a0d6e6cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332710"
---
# <a name="resolvedelayloadsfromdll-function"></a><span data-ttu-id="d107e-103">ResolveDelayLoadsFromDll (funzione)</span><span class="sxs-lookup"><span data-stu-id="d107e-103">ResolveDelayLoadsFromDll function</span></span>

<span data-ttu-id="d107e-104">Invia il lavoro di risoluzione delle importazioni a caricamento ritardato dal file binario padre a un file binario di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d107e-104">Forwards the work in resolving delay-loaded imports from the parent binary to a target binary.</span></span>

## <a name="syntax"></a><span data-ttu-id="d107e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d107e-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="d107e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d107e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d107e-107">*ParentBase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d107e-107">*ParentBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d107e-108">Indirizzo di base del modulo che ritarda il caricamento di un altro file binario.</span><span class="sxs-lookup"><span data-stu-id="d107e-108">The base address of the module that delay loads another binary.</span></span>

</dd> <dt>

<span data-ttu-id="d107e-109">*TargetDllName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d107e-109">*TargetDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d107e-110">Nome della DLL di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d107e-110">The name of the target DLL.</span></span>

</dd> <dt>

<span data-ttu-id="d107e-111">*Flag*</span><span class="sxs-lookup"><span data-stu-id="d107e-111">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="d107e-112">Riservati deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="d107e-112">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d107e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d107e-113">Return value</span></span>

<span data-ttu-id="d107e-114">Indirizzo del descrittore di caricamento ritardato, se trovato. in caso contrario, **null**.</span><span class="sxs-lookup"><span data-stu-id="d107e-114">The address of the delay-load descriptor, if it is found; otherwise, **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d107e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d107e-115">Requirements</span></span>



| <span data-ttu-id="d107e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d107e-116">Requirement</span></span> | <span data-ttu-id="d107e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d107e-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d107e-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="d107e-118">Library</span></span><br/> | <dl> <span data-ttu-id="d107e-119"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d107e-119"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d107e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d107e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="d107e-121"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d107e-121"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d107e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d107e-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="d107e-123">[Supporto del linker per le DLL di Delay-Loaded](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="d107e-123">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




