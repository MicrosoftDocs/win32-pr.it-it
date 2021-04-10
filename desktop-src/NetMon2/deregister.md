---
description: La funzione Deregister Export libera le risorse utilizzate per creare il database delle proprietà del protocollo. La DLL del parser deve implementare l'annullamento della registrazione.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Annullare la registrazione della funzione di callback (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227383"
---
# <a name="deregister-callback-function"></a><span data-ttu-id="a3bda-104">Annullare la registrazione della funzione di callback</span><span class="sxs-lookup"><span data-stu-id="a3bda-104">Deregister callback function</span></span>

<span data-ttu-id="a3bda-105">La funzione **deregister** Export libera le risorse utilizzate per creare il database delle [*Proprietà*](p.md)del protocollo.</span><span class="sxs-lookup"><span data-stu-id="a3bda-105">The **Deregister** export function frees the resources used to create the protocol [*property database*](p.md).</span></span> <span data-ttu-id="a3bda-106">La DLL del parser deve implementare l' **annullamento della registrazione**.</span><span class="sxs-lookup"><span data-stu-id="a3bda-106">The parser DLL must implement **Deregister**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3bda-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3bda-107">Syntax</span></span>


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="a3bda-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3bda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3bda-109">*hProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3bda-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3bda-110">Handle del protocollo per un database specifico.</span><span class="sxs-lookup"><span data-stu-id="a3bda-110">Handle of the protocol for a specific database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3bda-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3bda-111">Return value</span></span>

<span data-ttu-id="a3bda-112">No.</span><span class="sxs-lookup"><span data-stu-id="a3bda-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3bda-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a3bda-113">Remarks</span></span>

<span data-ttu-id="a3bda-114">Network Monitor chiama la funzionalità di **annullamento della registrazione** dopo il passaggio di tutte le informazioni di acquisizione alla DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="a3bda-114">Network Monitor calls **Deregister** after passing all the capture information to the parser DLL.</span></span> <span data-ttu-id="a3bda-115">La DLL del parser deve implementare una funzione di **annullamento della registrazione** per ogni protocollo supportato dal parser.</span><span class="sxs-lookup"><span data-stu-id="a3bda-115">The parser DLL must implement a **Deregister** function for each protocol that the parser supports.</span></span>

<span data-ttu-id="a3bda-116">Quando si implementa la funzione di **annullamento della registrazione**, è necessario che la dll del parser chiami la funzione [DestroyPropertyDatabase](destroypropertydatabase.md) per rilasciare le risorse del [*database della proprietà*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="a3bda-116">When implementing **Deregister**, the parser DLL must call the [DestroyPropertyDatabase](destroypropertydatabase.md) function to release the [*property database*](p.md) resources.</span></span>



| <span data-ttu-id="a3bda-117">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="a3bda-117">For information on</span></span>                                        | <span data-ttu-id="a3bda-118">Vedere</span><span class="sxs-lookup"><span data-stu-id="a3bda-118">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="a3bda-119">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="a3bda-119">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="a3bda-120">Parser</span><span class="sxs-lookup"><span data-stu-id="a3bda-120">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="a3bda-121">I punti di ingresso inclusi nella DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="a3bda-121">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="a3bda-122">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="a3bda-122">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="a3bda-123">Come implementare la **Deregistrazione**  è incluso un esempio.</span><span class="sxs-lookup"><span data-stu-id="a3bda-123">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="a3bda-124">Implementazione della deregistrazione</span><span class="sxs-lookup"><span data-stu-id="a3bda-124">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="a3bda-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3bda-125">Requirements</span></span>



| <span data-ttu-id="a3bda-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3bda-126">Requirement</span></span> | <span data-ttu-id="a3bda-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a3bda-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a3bda-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3bda-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a3bda-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3bda-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a3bda-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3bda-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a3bda-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3bda-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a3bda-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3bda-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3bda-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3bda-133"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3bda-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3bda-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3bda-135">DestroyPropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="a3bda-135">DestroyPropertyDatabase</span></span>](destroypropertydatabase.md)
</dt> </dl>

 

 




