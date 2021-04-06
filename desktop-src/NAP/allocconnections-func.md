---
title: Funzione AllocConnections (NapUtil. h)
description: Alloca memoria per un numero specificato di strutture di connessione.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- NAP funzione AllocConnections
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e29521d2fea6eec3765a3a34210b896f1baa4db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743898"
---
# <a name="allocconnections-function"></a><span data-ttu-id="5bd4b-104">AllocConnections (funzione)</span><span class="sxs-lookup"><span data-stu-id="5bd4b-104">AllocConnections function</span></span>

> [!Note]  
> <span data-ttu-id="5bd4b-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="5bd4b-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5bd4b-106">La funzione **AllocConnections** alloca memoria per un numero specificato di strutture di [**connessione**](connections-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="5bd4b-106">The **AllocConnections** function allocates memory for a specified number of [**Connections**](connections-struct.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd4b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5bd4b-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a><span data-ttu-id="5bd4b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bd4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bd4b-109">*connessioni* \[ di in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-109">*connections* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd4b-110">Puntatore a una matrice di strutture di [**connessioni**](connections-struct.md) appena allocate.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-110">A pointer to an array of newly allocated [**Connections**](connections-struct.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="5bd4b-111">*connectionsCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-111">*connectionsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd4b-112">Numero di strutture da allocare alle *connessioni*.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-112">The number of structures to allocate to *connections*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bd4b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bd4b-113">Return value</span></span>



| <span data-ttu-id="5bd4b-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5bd4b-114">Return code</span></span>                                                                                   | <span data-ttu-id="5bd4b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bd4b-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5bd4b-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5bd4b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5bd4b-117">L'operazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="5bd4b-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5bd4b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5bd4b-119">È stato passato un argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="5bd4b-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="5bd4b-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5bd4b-121">Memoria virtuale insufficiente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-121">The system is out of virtual memory.</span></span> <span data-ttu-id="5bd4b-122">Operazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5bd4b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bd4b-123">Remarks</span></span>

<span data-ttu-id="5bd4b-124">Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="5bd4b-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="5bd4b-125">I parametri **in** vengono allocati e liberati dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="5bd4b-126">I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="5bd4b-127">I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="5bd4b-128">Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bd4b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bd4b-129">Requirements</span></span>



| <span data-ttu-id="5bd4b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bd4b-130">Requirement</span></span> | <span data-ttu-id="5bd4b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="5bd4b-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd4b-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bd4b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd4b-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5bd4b-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bd4b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd4b-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5bd4b-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bd4b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bd4b-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bd4b-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="5bd4b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5bd4b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bd4b-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bd4b-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bd4b-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bd4b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd4b-141">**FreeConnections**</span><span class="sxs-lookup"><span data-stu-id="5bd4b-141">**FreeConnections**</span></span>](freeconnections-func.md)
</dt> </dl>

 

 





