---
title: Broadcast (attributo)
description: La parola chiave \ broadcast \ specifica che le chiamate a procedure remote devono essere inviate a tutti i server in una rete locale.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- attributo broadcast MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334431"
---
# <a name="broadcast-attribute"></a><span data-ttu-id="b2cb2-104">Broadcast (attributo)</span><span class="sxs-lookup"><span data-stu-id="b2cb2-104">broadcast attribute</span></span>

<span data-ttu-id="b2cb2-105">La parola chiave **\[ broadcast \]** indica che le chiamate a procedure remote devono essere inviate a tutti i server in una rete locale.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-105">The keyword **\[broadcast\]** specifies that remote procedure calls be sent to all servers on a local network.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="b2cb2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2cb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2cb2-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b2cb2-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b2cb2-108">Specifica un elenco di zero o più attributi IDL che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="b2cb2-109">Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="b2cb2-110">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="b2cb2-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b2cb2-111">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="b2cb2-112">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="b2cb2-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b2cb2-113">Specifica gli attributi aggiuntivi da applicare alla funzione.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-113">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="b2cb2-114">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-114">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="b2cb2-115">*returnType*</span><span class="sxs-lookup"><span data-stu-id="b2cb2-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="b2cb2-116">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="b2cb2-117">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="b2cb2-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b2cb2-118">Specifica il nome della funzione a cui verrà applicato l'attributo **\[ broadcast \]** .</span><span class="sxs-lookup"><span data-stu-id="b2cb2-118">Specifies the name of the function to which the **\[broadcast\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="b2cb2-119">*params*</span><span class="sxs-lookup"><span data-stu-id="b2cb2-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="b2cb2-120">Elenco dei parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2cb2-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2cb2-121">Remarks</span></span>

<span data-ttu-id="b2cb2-122">La parola chiave **\[ broadcast \]** specifica che la routine viene sempre trasmessa a tutti i server nella rete, anziché essere recapitata a un server specifico. Il client riceve l'output dalla prima risposta per restituire correttamente, mentre le risposte successive vengono scartate.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-122">The **\[broadcast\]** keyword specifies that the routine is always broadcasted to all the servers on the network, rather than being delivered to one particular server.The client receives output from the first reply to return successfully, while subsequent replies are discarded.</span></span>

<span data-ttu-id="b2cb2-123">Un'operazione con l'attributo **\[ broadcast \]** è implicitamente un'operazione [**\[ idempotente \]**](idempotent.md) .</span><span class="sxs-lookup"><span data-stu-id="b2cb2-123">An operation with the **\[broadcast\]** attribute is implicitly an [**\[idempotent\]**](idempotent.md) operation.</span></span> <span data-ttu-id="b2cb2-124">Tuttavia, l'attributo **\[ broadcast \]** specifica proprietà aggiuntive che non sono disponibili nelle funzioni con l'attributo **\[ idempotente \]** .</span><span class="sxs-lookup"><span data-stu-id="b2cb2-124">However, the **\[broadcast\]** attribute specifies additional properties that functions with the **\[idempotent\]** attribute don't have.</span></span> <span data-ttu-id="b2cb2-125">In particolare, le funzioni che usano l'attributo **\[ broadcast \]** specificano che la routine può essere chiamata più volte come risultato di una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-125">Specifically, functions using the **\[broadcast\]** attribute specify that the routine can be called multiple times as the result of one remote procedure call.</span></span> <span data-ttu-id="b2cb2-126">Allo stesso tempo, possono essere inviati a più server.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-126">At the same time, they can be sent to multiple servers.</span></span> <span data-ttu-id="b2cb2-127">Questa operazione è diversa dall'attributo **\[ idempotente \]** , che specifica solo che è possibile ritentare una chiamata se non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-127">This is different from the **\[idempotent\]** attribute, which specifies only that a call can be retried if it is not completed.</span></span>

<span data-ttu-id="b2cb2-128">Se una procedura remota trasmette la chiamata a tutti gli host in una rete locale, deve usare la sequenza di protocollo [**\_ IPX**](ncadg-ipx.md) [**ncadg \_ \_**](ncadg-ip-udp.md) o ncadg.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-128">If a remote procedure broadcasts its call to all hosts on a local network, it must use either the [**ncadg\_ip\_udp**](ncadg-ip-udp.md) or the [**ncadg\_ipx**](ncadg-ipx.md) protocol sequence.</span></span> <span data-ttu-id="b2cb2-129">Si noti che la dimensione di un pacchetto di **\[ broadcast \]** è determinata dal servizio datagramma in uso.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-129">Note that the size of a **\[broadcast\]** packet is determined by the datagram service in use.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2cb2-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2cb2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2cb2-131">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-131">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="b2cb2-132">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="b2cb2-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b2cb2-133">**Forse**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-133">**maybe**</span></span>](maybe.md)
</dt> <dt>

[<span data-ttu-id="b2cb2-134">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-134">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="b2cb2-135">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-135">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> </dl>

 

 




