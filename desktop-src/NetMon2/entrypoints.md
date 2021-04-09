---
description: La struttura ENTRYPOINTS definisce i punti di ingresso alle funzioni di esportazione utilizzate da Network Monitor per il funzionamento del parser.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: Struttura ENTRYPOINTS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966484"
---
# <a name="entrypoints-structure"></a><span data-ttu-id="27fff-103">Struttura ENTRYPOINTS</span><span class="sxs-lookup"><span data-stu-id="27fff-103">ENTRYPOINTS structure</span></span>

<span data-ttu-id="27fff-104">La struttura **ENTRYPOINTS** definisce i punti di ingresso alle funzioni di esportazione utilizzate da Network Monitor per il funzionamento del parser.</span><span class="sxs-lookup"><span data-stu-id="27fff-104">The **ENTRYPOINTS** structure defines the entry points to the export functions that Network Monitor uses to operate the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="27fff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27fff-105">Syntax</span></span>


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a><span data-ttu-id="27fff-106">Members</span><span class="sxs-lookup"><span data-stu-id="27fff-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="27fff-107">**Registra**</span><span class="sxs-lookup"><span data-stu-id="27fff-107">**Register**</span></span>
</dt> <dd>

<span data-ttu-id="27fff-108">Puntatore all'implementazione della funzione dell' [*esperto di registrazione*](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="27fff-108">Pointer to the implementation of the [*Register expert*](register-expert.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="27fff-109">**Annullamento registrazione**</span><span class="sxs-lookup"><span data-stu-id="27fff-109">**Deregister**</span></span>
</dt> <dd>

<span data-ttu-id="27fff-110">Puntatore all'implementazione della funzione di [**annullamento della registrazione**](deregister.md) .</span><span class="sxs-lookup"><span data-stu-id="27fff-110">Pointer to the implementation of the [**Deregister**](deregister.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="27fff-111">**RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="27fff-111">**RecognizeFrame**</span></span>
</dt> <dd>

<span data-ttu-id="27fff-112">Puntatore all'implementazione della funzione di esportazione [**RecognizeFrame**](recognizeframe.md) .</span><span class="sxs-lookup"><span data-stu-id="27fff-112">Pointer to the implementation of the [**RecognizeFrame**](recognizeframe.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="27fff-113">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="27fff-113">**AttachProperties**</span></span>
</dt> <dd>

<span data-ttu-id="27fff-114">Puntatore all'implementazione della funzione di esportazione [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="27fff-114">Pointer to the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="27fff-115">**FormatProperties**</span><span class="sxs-lookup"><span data-stu-id="27fff-115">**FormatProperties**</span></span>
</dt> <dd>

<span data-ttu-id="27fff-116">Puntatore all'implementazione della funzione di esportazione [**FormatProperties**](formatproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="27fff-116">Pointer to the implementation of the [**FormatProperties**](formatproperties.md) export function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27fff-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="27fff-117">Remarks</span></span>

<span data-ttu-id="27fff-118">La funzione **CreateProtocol** usa la struttura **ENTRYPOINTS** per fornire i puntatori a Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="27fff-118">The **CreateProtocol** function uses the **ENTRYPOINTS** structure to provide pointers to Network Monitor.</span></span> <span data-ttu-id="27fff-119">I puntatori devono essere specificati nell'ordine identificato nella sezione membri precedenti.</span><span class="sxs-lookup"><span data-stu-id="27fff-119">The pointers must be specified in the order identified in the previous Members section.</span></span>

<span data-ttu-id="27fff-120">Non è necessario implementare la funzione [**FormatProperties**](formatproperties.md) se Network Monitor non visualizza mai i dati del protocollo.</span><span class="sxs-lookup"><span data-stu-id="27fff-120">The [**FormatProperties**](formatproperties.md) function does not need to be implemented if Network Monitor will never display the protocol data.</span></span> <span data-ttu-id="27fff-121">Ad esempio, non è necessario implementare **FormatProperties** se un'applicazione di esportazione usa l'output del parser e Network Monitor non Visualizza l'output.</span><span class="sxs-lookup"><span data-stu-id="27fff-121">For example, **FormatProperties** does not need to be implemented if an export application uses the output from the parser, and Network Monitor does not display the output.</span></span>



| <span data-ttu-id="27fff-122">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="27fff-122">For information on</span></span>                                        | <span data-ttu-id="27fff-123">Vedere</span><span class="sxs-lookup"><span data-stu-id="27fff-123">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="27fff-124">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="27fff-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="27fff-125">Parser</span><span class="sxs-lookup"><span data-stu-id="27fff-125">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="27fff-126">Come implementare **DllMain**  include un esempio.</span><span class="sxs-lookup"><span data-stu-id="27fff-126">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="27fff-127">Implementazione di DllMain</span><span class="sxs-lookup"><span data-stu-id="27fff-127">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="27fff-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27fff-128">Requirements</span></span>



| <span data-ttu-id="27fff-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="27fff-129">Requirement</span></span> | <span data-ttu-id="27fff-130">Valore</span><span class="sxs-lookup"><span data-stu-id="27fff-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="27fff-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27fff-131">Minimum supported client</span></span><br/> | <span data-ttu-id="27fff-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27fff-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="27fff-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27fff-133">Minimum supported server</span></span><br/> | <span data-ttu-id="27fff-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27fff-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="27fff-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27fff-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="27fff-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="27fff-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27fff-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27fff-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27fff-138">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="27fff-138">AttachProperties</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="27fff-139">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="27fff-139">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="27fff-140">Annullamento registrazione</span><span class="sxs-lookup"><span data-stu-id="27fff-140">Deregister</span></span>](deregister.md)
</dt> <dt>

[<span data-ttu-id="27fff-141">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="27fff-141">FormatProperties</span></span>](formatproperties.md)
</dt> <dt>

[<span data-ttu-id="27fff-142">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="27fff-142">RecognizeFrame</span></span>](recognizeframe.md)
</dt> <dt>

[<span data-ttu-id="27fff-143">Registra</span><span class="sxs-lookup"><span data-stu-id="27fff-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




