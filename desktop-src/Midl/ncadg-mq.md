---
title: attributo ncadg_mq
description: La \_ parola chiave ncadg mq identifica Microsoft Message Queuing Services (MSMQ) come protocollo di trasporto per l'endpoint. Questo protocollo è obsoleto e non deve essere utilizzato nelle nuove applicazioni.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- attributo ncadg_mq MIDL
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0acc433b55ba9f3c6d8919bef9b8db470bc0f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956413"
---
# <a name="ncadg_mq-attribute"></a><span data-ttu-id="021bf-105">ncadg \_ mq-attributo</span><span class="sxs-lookup"><span data-stu-id="021bf-105">ncadg\_mq attribute</span></span>

<span data-ttu-id="021bf-106">La parola chiave **ncadg \_ mq** identifica Microsoft Message QUEUING Services (MSMQ) come protocollo di trasporto per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="021bf-106">The **ncadg\_mq** keyword identifies Microsoft Message Queuing Services (MSMQ) as the transport protocol for the endpoint.</span></span> <span data-ttu-id="021bf-107">Questo protocollo è obsoleto e non deve essere utilizzato nelle nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="021bf-107">This protocol is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a><span data-ttu-id="021bf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="021bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="021bf-109">*nome server*</span><span class="sxs-lookup"><span data-stu-id="021bf-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="021bf-110">Specifica il nome del server, o host, del computer.</span><span class="sxs-lookup"><span data-stu-id="021bf-110">Specifies the name of the server, or host, computer.</span></span> <span data-ttu-id="021bf-111">Il nome è una stringa di caratteri e può essere un nome di dominio completo.</span><span class="sxs-lookup"><span data-stu-id="021bf-111">The name is a character string and may be a fully qualified domain name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="021bf-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="021bf-112">Remarks</span></span>

<span data-ttu-id="021bf-113">Per usare il protocollo di trasporto **ncadg \_ mq** , i componenti MSMQ devono essere completamente installati e i sistemi client e server devono essere raggiungibili tramite i protocolli mq.</span><span class="sxs-lookup"><span data-stu-id="021bf-113">In order to use the **ncadg\_mq** transport protocol, the MSMQ components must be fully installed and the client and server systems must be reachable through the MQ protocols.</span></span>

<span data-ttu-id="021bf-114">Il protocollo **ncadg \_ mq** non supporta endpoint dinamici o chiamate [**broadcast**](broadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="021bf-114">The **ncadg\_mq** protocol does not support dynamic endpoints or [**broadcast**](broadcast.md) calls.</span></span> <span data-ttu-id="021bf-115">Come per gli altri protocolli di datagramma, **ncadg \_ mq** non supporta i callback. le funzioni che usano l'attributo di [**callback**](callback.md) avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="021bf-115">As with other datagram protocols, **ncadg\_mq** does not support callbacks; any functions using the [**callback**](callback.md) attribute will fail.</span></span>

> [!Note]  
> <span data-ttu-id="021bf-116">Questa famiglia di protocolli non è supportata in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="021bf-116">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="021bf-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="021bf-117">Examples</span></span>

<span data-ttu-id="021bf-118">La sintassi del protocollo Message-Queue è definita indipendentemente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="021bf-118">The syntax of the message-queue protocol is defined independently of the IDL specification.</span></span> <span data-ttu-id="021bf-119">Il compilatore MIDL esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="021bf-119">The MIDL compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="021bf-120">È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="021bf-120">Some errors may be reported at run time rather than during compilation.</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="021bf-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="021bf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="021bf-122">**trasmissione**</span><span class="sxs-lookup"><span data-stu-id="021bf-122">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="021bf-123">**callback**</span><span class="sxs-lookup"><span data-stu-id="021bf-123">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="021bf-124">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="021bf-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="021bf-125">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="021bf-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="021bf-126">**Messaggio**</span><span class="sxs-lookup"><span data-stu-id="021bf-126">**message**</span></span>](message.md)
</dt> <dt>

[<span data-ttu-id="021bf-127">Accodamento messaggi RPC</span><span class="sxs-lookup"><span data-stu-id="021bf-127">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="021bf-128">Associazione stringa</span><span class="sxs-lookup"><span data-stu-id="021bf-128">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 