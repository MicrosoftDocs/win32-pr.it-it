---
description: La funzione DestroyPropertyDatabase rilascia le risorse usate per creare il database delle proprietà del protocollo.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: Funzione DestroyPropertyDatabase (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968391"
---
# <a name="destroypropertydatabase-function"></a><span data-ttu-id="4ec3b-103">DestroyPropertyDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="4ec3b-103">DestroyPropertyDatabase function</span></span>

<span data-ttu-id="4ec3b-104">La funzione **DestroyPropertyDatabase** rilascia le risorse usate per creare il [*database delle proprietà*](p.md)del protocollo.</span><span class="sxs-lookup"><span data-stu-id="4ec3b-104">The **DestroyPropertyDatabase** function releases the resources used to create the protocol [*property database*](p.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec3b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ec3b-105">Syntax</span></span>


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="4ec3b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ec3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ec3b-107">*hProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ec3b-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec3b-108">Handle per il database delle proprietà da eliminare definitivamente.</span><span class="sxs-lookup"><span data-stu-id="4ec3b-108">Handle to the property database to be destroyed.</span></span> <span data-ttu-id="4ec3b-109">L'handle viene passato alla DLL del parser quando Network Monitor chiama la funzione di [annullamento della registrazione](deregister.md) .</span><span class="sxs-lookup"><span data-stu-id="4ec3b-109">The handle is passed to the parser DLL when Network Monitor calls the [Deregister](deregister.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ec3b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ec3b-110">Return value</span></span>

<span data-ttu-id="4ec3b-111">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4ec3b-111">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4ec3b-112">Se la funzione ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="4ec3b-112">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="4ec3b-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4ec3b-113">Return code</span></span>                                                                                              | <span data-ttu-id="4ec3b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ec3b-114">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="4ec3b-115"><dt>**\_errore interno \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="4ec3b-115"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="4ec3b-116">An internal error occurred.</span><span class="sxs-lookup"><span data-stu-id="4ec3b-116">An internal error occurred.</span></span> <br/>    |
| <dl> <span data-ttu-id="4ec3b-117"><dt>**\_HPROTOCOL NMERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ec3b-117"><dt>**NMERR\_INVALID\_HPROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="4ec3b-118">Handle non valido in *hProtocol*.</span><span class="sxs-lookup"><span data-stu-id="4ec3b-118">Invalid handle in *hProtocol*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="4ec3b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ec3b-119">Remarks</span></span>

<span data-ttu-id="4ec3b-120">La funzione **DestroyPropertyDatabase** deve essere chiamata solo quando si implementa la funzione di esportazione di [annullamento della registrazione](deregister.md) per il protocollo.</span><span class="sxs-lookup"><span data-stu-id="4ec3b-120">The **DestroyPropertyDatabase** function should be called only when implementing the [Deregister](deregister.md) export function for the protocol.</span></span> <span data-ttu-id="4ec3b-121">Per le dll del parser che supportano più protocolli, viene chiamata la funzione **DestroyPropertyDatabase** per ogni implementazione di **deregister**.</span><span class="sxs-lookup"><span data-stu-id="4ec3b-121">For parser DLLs that support multiple protocols, the **DestroyPropertyDatabase** function is called for each implementation of **Deregister**.</span></span>



| <span data-ttu-id="4ec3b-122">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="4ec3b-122">For information on</span></span>                                        | <span data-ttu-id="4ec3b-123">Vedere</span><span class="sxs-lookup"><span data-stu-id="4ec3b-123">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="4ec3b-124">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="4ec3b-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="4ec3b-125">Parser</span><span class="sxs-lookup"><span data-stu-id="4ec3b-125">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="4ec3b-126">I punti di ingresso inclusi nella DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="4ec3b-126">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="4ec3b-127">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="4ec3b-127">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="4ec3b-128">Come implementare la **Deregistrazione**  è incluso un esempio.</span><span class="sxs-lookup"><span data-stu-id="4ec3b-128">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="4ec3b-129">Implementazione della deregistrazione</span><span class="sxs-lookup"><span data-stu-id="4ec3b-129">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="4ec3b-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ec3b-130">Requirements</span></span>



| <span data-ttu-id="4ec3b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ec3b-131">Requirement</span></span> | <span data-ttu-id="4ec3b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4ec3b-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec3b-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ec3b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec3b-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ec3b-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4ec3b-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ec3b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec3b-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ec3b-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4ec3b-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ec3b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ec3b-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ec3b-138"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4ec3b-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="4ec3b-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="4ec3b-140"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ec3b-140"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="4ec3b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4ec3b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ec3b-142"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ec3b-142"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ec3b-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ec3b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec3b-144">Annullamento registrazione</span><span class="sxs-lookup"><span data-stu-id="4ec3b-144">Deregister</span></span>](deregister.md)
</dt> </dl>

 

 




