---
title: attributo ncalrpc
description: La parola chiave ncalrpc identifica la comunicazione interprocesso locale come famiglia di protocolli per l'endpoint. Questa parola chiave è uno dei nomi di famiglia di protocollo validi che devono essere usati con l'attributo \ endpoint \.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- attributo MIDL di ncalrpc
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f20ae9e347303288868eeb16758736047fecc1b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963049"
---
# <a name="ncalrpc-attribute"></a><span data-ttu-id="31be8-105">attributo ncalrpc</span><span class="sxs-lookup"><span data-stu-id="31be8-105">ncalrpc attribute</span></span>

<span data-ttu-id="31be8-106">La parola chiave **ncalrpc** identifica la comunicazione interprocesso locale come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="31be8-106">The **ncalrpc** keyword identifies local interprocess communication as the protocol family for the endpoint.</span></span> <span data-ttu-id="31be8-107">Questa parola chiave è uno dei nomi di famiglia di protocollo validi che devono essere utilizzati con l' **\[** [](endpoint.md) **\]** attributo endpoint.</span><span class="sxs-lookup"><span data-stu-id="31be8-107">This keyword is one of the valid protocol family names that must be used with the **\[**[**endpoint**](endpoint.md)**\]** attribute.</span></span>

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="31be8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="31be8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31be8-109">*nome porta*</span><span class="sxs-lookup"><span data-stu-id="31be8-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="31be8-110">Stringa di caratteri che specifica la porta di comunicazione (un'applicazione, un servizio o un'istanza di un servizio) che un client utilizza per eseguire chiamate interprocesso a un server.</span><span class="sxs-lookup"><span data-stu-id="31be8-110">A character string that specifies the communication port (an application, a service, or an instance of a service) that a client uses to make interprocess calls to a server.</span></span> <span data-ttu-id="31be8-111">La stringa può contenere un massimo di 53 caratteri e non deve contenere una barra rovesciata ( \) caratteri.</span><span class="sxs-lookup"><span data-stu-id="31be8-111">The string can contain up to 53 characters and should not contain any backslash (\) characters.</span></span> <span data-ttu-id="31be8-112">Il nome del computer non deve essere utilizzato con la parola chiave **ncalrpc** .</span><span class="sxs-lookup"><span data-stu-id="31be8-112">The computer name must not be used with the **ncalrpc** keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31be8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="31be8-113">Remarks</span></span>

<span data-ttu-id="31be8-114">La sintassi della stringa di porta di comunicazione interprocesso locale, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="31be8-114">The syntax of the local interprocess-communication port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="31be8-115">Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="31be8-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="31be8-116">Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="31be8-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="31be8-117">Esempi</span><span class="sxs-lookup"><span data-stu-id="31be8-117">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="31be8-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="31be8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31be8-119">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="31be8-119">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="31be8-120">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="31be8-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="31be8-121">**ncacn \_ in \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="31be8-121">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="31be8-122">**ncacn \_ DNET \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="31be8-122">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="31be8-123">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="31be8-123">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="31be8-124">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="31be8-124">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="31be8-125">**\_SPX ncacn**</span><span class="sxs-lookup"><span data-stu-id="31be8-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="31be8-126">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="31be8-126">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="31be8-127">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="31be8-127">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="31be8-128">**\_NP ncacn**</span><span class="sxs-lookup"><span data-stu-id="31be8-128">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="31be8-129">**ncacn \_ le reti virtuali \_ spp**</span><span class="sxs-lookup"><span data-stu-id="31be8-129">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="31be8-130">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="31be8-130">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="31be8-131">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="31be8-131">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="31be8-132">Associazione stringa</span><span class="sxs-lookup"><span data-stu-id="31be8-132">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 