---
title: Attributo ncalrpc
description: La parola chiave ncalrpc identifica la comunicazione interprocesso locale come famiglia di protocolli per l'endpoint. Questa parola chiave è uno dei nomi di famiglia di protocolli validi che devono essere usati con l'attributo \ endpoint\.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- Attributo ncalrpc MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5d22b572eb9ad2f2e46b029ec242b48d5cd684
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386880"
---
# <a name="ncalrpc-attribute"></a><span data-ttu-id="06418-105">Attributo ncalrpc</span><span class="sxs-lookup"><span data-stu-id="06418-105">ncalrpc attribute</span></span>

<span data-ttu-id="06418-106">La **parola chiave ncalrpc** identifica la comunicazione interprocesso locale come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="06418-106">The **ncalrpc** keyword identifies local interprocess communication as the protocol family for the endpoint.</span></span> <span data-ttu-id="06418-107">Questa parola chiave è uno dei nomi di famiglia di protocolli validi che devono essere usati con **\[** [**l'attributo endpoint.**](endpoint.md) **\]**</span><span class="sxs-lookup"><span data-stu-id="06418-107">This keyword is one of the valid protocol family names that must be used with the **\[**[**endpoint**](endpoint.md)**\]** attribute.</span></span>

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="06418-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="06418-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06418-109">*port-name*</span><span class="sxs-lookup"><span data-stu-id="06418-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="06418-110">Stringa di caratteri che specifica la porta di comunicazione (un'applicazione, un servizio o un'istanza di un servizio) utilizzata da un client per effettuare chiamate interprocesso a un server.</span><span class="sxs-lookup"><span data-stu-id="06418-110">A character string that specifies the communication port (an application, a service, or an instance of a service) that a client uses to make interprocess calls to a server.</span></span> <span data-ttu-id="06418-111">La stringa può contenere fino a 53 caratteri e non deve contenere alcuna barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="06418-111">The string can contain up to 53 characters and should not contain any backslash (\\) characters.</span></span> <span data-ttu-id="06418-112">Il nome del computer non deve essere usato con la **parola chiave ncalrpc.**</span><span class="sxs-lookup"><span data-stu-id="06418-112">The computer name must not be used with the **ncalrpc** keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06418-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="06418-113">Remarks</span></span>

<span data-ttu-id="06418-114">La sintassi della stringa di porta interprocess-communication locale, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="06418-114">The syntax of the local interprocess-communication port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="06418-115">Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="06418-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="06418-116">Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="06418-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="06418-117">Esempi</span><span class="sxs-lookup"><span data-stu-id="06418-117">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="06418-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="06418-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06418-119">**Endpoint**</span><span class="sxs-lookup"><span data-stu-id="06418-119">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="06418-120">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="06418-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="06418-121">**ncacn \_ in \_ dsp**</span><span class="sxs-lookup"><span data-stu-id="06418-121">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="06418-122">**ncacn \_ dnet \_ nsp**</span><span class="sxs-lookup"><span data-stu-id="06418-122">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="06418-123">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="06418-123">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="06418-124">**ncacn \_ nb \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="06418-124">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="06418-125">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="06418-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="06418-126">**ncacn \_ nb \_ nb**</span><span class="sxs-lookup"><span data-stu-id="06418-126">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="06418-127">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="06418-127">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="06418-128">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="06418-128">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="06418-129">**ncacn \_ vns \_ spp**</span><span class="sxs-lookup"><span data-stu-id="06418-129">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="06418-130">**ncadg \_ ip \_ udp**</span><span class="sxs-lookup"><span data-stu-id="06418-130">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="06418-131">**ncadg \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="06418-131">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="06418-132">Associazione di stringhe</span><span class="sxs-lookup"><span data-stu-id="06418-132">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 