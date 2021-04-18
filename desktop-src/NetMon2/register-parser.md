---
description: La funzione Register Export deve essere implementata in tutte le dll del parser. L'implementazione di Register crea e compila un database delle proprietà per un protocollo. Network Monitor utilizza il database per determinare le proprietà supportate dal protocollo.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Funzione Register parser callback (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: bc49cc083cf6ba46594473a041d9a1ad138efa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310495"
---
# <a name="register-parser-callback-function"></a><span data-ttu-id="6ae2f-105">Funzione di callback Register parser</span><span class="sxs-lookup"><span data-stu-id="6ae2f-105">Register Parser callback function</span></span>

<span data-ttu-id="6ae2f-106">La funzione **Register** Export deve essere implementata in tutte le dll del parser.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-106">The **Register** export function must be implemented in all parser DLLs.</span></span> <span data-ttu-id="6ae2f-107">L'implementazione di **Register** crea e compila un [*database delle proprietà*](p.md) per un protocollo.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-107">The implementation of **Register** creates and fills-in a [*property database*](p.md) for a protocol.</span></span> <span data-ttu-id="6ae2f-108">Network Monitor utilizza il database per determinare le proprietà supportate dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-108">Network Monitor uses the database to determine which properties the protocol supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae2f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ae2f-109">Syntax</span></span>


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="6ae2f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ae2f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae2f-111">*hProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ae2f-111">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae2f-112">Handle del protocollo fornito da Network Monitor quando si chiama **Register**.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-112">The handle of the protocol that Network Monitor provides when calling **Register**.</span></span> <span data-ttu-id="6ae2f-113">L'handle *hProtocol* è necessario quando si chiamano le funzioni di supporto di esportazione.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-113">The *hProtocol* handle is needed when calling export helper functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae2f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ae2f-114">Return value</span></span>

<span data-ttu-id="6ae2f-115">No.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-115">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ae2f-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="6ae2f-116">Remarks</span></span>

<span data-ttu-id="6ae2f-117">Network Monitor inizia a chiamare la funzione **Register** non appena viene caricata un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-117">Network Monitor starts calling the **Register** function as soon as a capture is loaded.</span></span> <span data-ttu-id="6ae2f-118">Network Monitor chiama la funzione **Register** per ogni protocollo che può identificare.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-118">Network Monitor calls the **Register** function for each protocol it can identify.</span></span> <span data-ttu-id="6ae2f-119">La funzione [CreateProtocol](createprotocol.md) passa un puntatore alla funzione **Register** .</span><span class="sxs-lookup"><span data-stu-id="6ae2f-119">The [CreateProtocol](createprotocol.md) function passes a pointer to the **Register** function.</span></span>

<span data-ttu-id="6ae2f-120">L'implementazione del **Registro** include le chiamate alle funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-120">The implementation of **Register** includes calls to the following functions.</span></span>

-   <span data-ttu-id="6ae2f-121">Una chiamata alle funzioni [CreatePropertyDatabase](createpropertydatabase.md) e [AddProperty](/previous-versions/bb251873(v=msdn.10)) per creare un database di tutte le proprietà supportate dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-121">A call to the [CreatePropertyDatabase](createpropertydatabase.md) and [AddProperty](/previous-versions/bb251873(v=msdn.10)) functions to create a database of all the properties that the protocol supports.</span></span>
-   <span data-ttu-id="6ae2f-122">Una chiamata alla funzione [CreateHandoffTable](createhandofftable.md) è obbligatoria se il protocollo usa un [*set di continuità*](h.md).</span><span class="sxs-lookup"><span data-stu-id="6ae2f-122">A call to the [CreateHandoffTable](createhandofftable.md) function is required if the protocol uses a [*handoff set*](h.md).</span></span>

<span data-ttu-id="6ae2f-123">Se la DLL del parser contiene più parser e il parser è in grado di rilevare più di un protocollo, è necessario implementare una funzione **Register** per ogni protocollo.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-123">If the parser DLL contains multiple parsers, and the parser can detect more than one protocol, you must implement a **Register** function for each protocol.</span></span>



| <span data-ttu-id="6ae2f-124">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="6ae2f-124">For Information on</span></span>                                        | <span data-ttu-id="6ae2f-125">Vedere</span><span class="sxs-lookup"><span data-stu-id="6ae2f-125">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="6ae2f-126">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-126">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="6ae2f-127">Parser</span><span class="sxs-lookup"><span data-stu-id="6ae2f-127">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="6ae2f-128">I punti di ingresso inclusi nella DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-128">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="6ae2f-129">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="6ae2f-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="6ae2f-130">Come implementare il **Registro**  è incluso un esempio.</span><span class="sxs-lookup"><span data-stu-id="6ae2f-130">How to implement **Register**  includes an example.</span></span>       | [<span data-ttu-id="6ae2f-131">Implementazione del registro</span><span class="sxs-lookup"><span data-stu-id="6ae2f-131">Implementing Register</span></span>](implementing-register.md)     |



 

## <a name="requirements"></a><span data-ttu-id="6ae2f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ae2f-132">Requirements</span></span>



| <span data-ttu-id="6ae2f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ae2f-133">Requirement</span></span> | <span data-ttu-id="6ae2f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="6ae2f-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae2f-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ae2f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae2f-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ae2f-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6ae2f-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ae2f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae2f-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ae2f-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6ae2f-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ae2f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ae2f-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ae2f-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ae2f-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ae2f-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="6ae2f-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6ae2f-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="6ae2f-143">CreateHandoffTable</span><span class="sxs-lookup"><span data-stu-id="6ae2f-143">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> <dt>

[<span data-ttu-id="6ae2f-144">CreatePropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="6ae2f-144">CreatePropertyDatabase</span></span>](createpropertydatabase.md)
</dt> <dt>

[<span data-ttu-id="6ae2f-145">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="6ae2f-145">CreateProtocol</span></span>](createprotocol.md)
</dt> </dl>

 

