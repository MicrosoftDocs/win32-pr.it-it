---
title: attributo endpoint
description: L'attributo \ endpoint \ specifica una porta o porte note (endpoint di comunicazione) sui quali i server dell'interfaccia restano in ascolto delle chiamate.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- attributo dell'endpoint MIDL
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872362"
---
# <a name="endpoint-attribute"></a><span data-ttu-id="e4358-104">attributo endpoint</span><span class="sxs-lookup"><span data-stu-id="e4358-104">endpoint attribute</span></span>

<span data-ttu-id="e4358-105">L'attributo **\[ endpoint \]** specifica una porta o porte note (endpoint di comunicazione) sui quali i server dell'interfaccia restano in ascolto delle chiamate.</span><span class="sxs-lookup"><span data-stu-id="e4358-105">The **\[endpoint\]** attribute specifies a well-known port or ports (communication endpoints) on which servers of the interface listen for calls.</span></span>

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a><span data-ttu-id="e4358-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4358-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4358-107">*sequenza di protocolli*</span><span class="sxs-lookup"><span data-stu-id="e4358-107">*protocol-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="e4358-108">Specifica una stringa di caratteri che rappresenta una combinazione valida di un protocollo RPC (ad esempio "ncacn"), un protocollo di trasporto (ad esempio "TCP") e un protocollo di rete (ad esempio "IP").</span><span class="sxs-lookup"><span data-stu-id="e4358-108">Specifies a character string that represents a valid combination of an RPC protocol (such as "ncacn"), a transport protocol (such as "tcp"), and a network protocol (such as "ip").</span></span> <span data-ttu-id="e4358-109">Per un elenco di sequenze di protocollo valide, vedere [costanti di sequenza del protocollo](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="e4358-109">For a list of valid protocol sequences, see [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

</dd> <dt>

<span data-ttu-id="e4358-110">*Porta endpoint*</span><span class="sxs-lookup"><span data-stu-id="e4358-110">*endpoint-port*</span></span> 
</dt> <dd>

<span data-ttu-id="e4358-111">Specifica una stringa che rappresenta la designazione dell'endpoint per la famiglia di protocolli specificata.</span><span class="sxs-lookup"><span data-stu-id="e4358-111">Specifies a string that represents the endpoint designation for the specified protocol family.</span></span> <span data-ttu-id="e4358-112">La sintassi della stringa di porta è specifica per ogni sequenza di protocollo.</span><span class="sxs-lookup"><span data-stu-id="e4358-112">The syntax of the port string is specific to each protocol sequence.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4358-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4358-113">Remarks</span></span>

<span data-ttu-id="e4358-114">L'attributo **\[ endpoint \]** specifica una famiglia di trasporto, ad esempio il protocollo orientato alla connessione TCP/IP, un protocollo NetBIOS orientato alla connessione o il protocollo orientato alla connessione named pipe.</span><span class="sxs-lookup"><span data-stu-id="e4358-114">The **\[endpoint\]** attribute specifies a transport family such as the TCP/IP connection-oriented protocol, a NetBIOS connection-oriented protocol, or the named-pipe connection-oriented protocol.</span></span> <span data-ttu-id="e4358-115">L'utilizzo dell'attributo **\[ endpoint \]** è coerente con altri metodi per l'aggiunta di un endpoint e non fornisce servizi aggiuntivi o speciali per l'endpoint. fornisce semplicemente un collegamento per chiamare l'API.</span><span class="sxs-lookup"><span data-stu-id="e4358-115">Use of the **\[endpoint\]** attribute is consistent with other methods for adding an endpoint, and does not provide additional or special services for the endpoint; it simply provides a shortcut for calling the API.</span></span>

> [!Note]  
> <span data-ttu-id="e4358-116">Specifica di un endpoint in. La definizione dell'interfaccia IDL non limita l'accesso all'interfaccia all'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="e4358-116">Specifying an endpoint in the .IDL interface definition does not restrict access to the interface to the specified endpoint.</span></span> <span data-ttu-id="e4358-117">Aggiunta di un endpoint a. La definizione dell'interfaccia IDL consente la chiamata dell'interfaccia tramite qualsiasi endpoint in tale processo e consente l'utilizzo dell'endpoint per chiamare altre interfacce nel processo.</span><span class="sxs-lookup"><span data-stu-id="e4358-117">Adding an endpoint to the .IDL interface definition allows the interface to be called through any endpoint in that process, and allows the endpoint to be used to call other interfaces in that process.</span></span>

 

<span data-ttu-id="e4358-118">Il valore della *sequenza di protocollo* determina i valori validi per la *porta dell'endpoint*.</span><span class="sxs-lookup"><span data-stu-id="e4358-118">The *protocol-sequence* value determines the valid values for the *endpoint-port*.</span></span> <span data-ttu-id="e4358-119">Il compilatore MIDL controlla solo la sintassi generale per la voce di *Porta endpoint* .</span><span class="sxs-lookup"><span data-stu-id="e4358-119">The MIDL compiler checks only general syntax for the *endpoint-port* entry.</span></span> <span data-ttu-id="e4358-120">Gli errori di specifica della porta vengono segnalati dalle librerie di Runtime.</span><span class="sxs-lookup"><span data-stu-id="e4358-120">Port specification errors are reported by the run-time libraries.</span></span> <span data-ttu-id="e4358-121">Per informazioni sui valori consentiti per ogni sequenza di protocollo, vedere [costanti di sequenza del protocollo](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="e4358-121">For information about the allowed values for each protocol sequence, see the [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

<span data-ttu-id="e4358-122">Le sequenze di protocollo seguenti specificate da DCE non sono supportate dal compilatore MIDL fornito con Microsoft RPC: **ncacn \_ OSI \_ DNA** e **ncadg \_ DDS**.</span><span class="sxs-lookup"><span data-stu-id="e4358-122">The following protocol sequences specified by DCE are not supported by the MIDL compiler provided with Microsoft RPC: **ncacn\_osi\_dna** and **ncadg\_dds**.</span></span>

<span data-ttu-id="e4358-123">Assicurarsi di racchiudere tra virgolette la barra rovesciata negli endpoint.</span><span class="sxs-lookup"><span data-stu-id="e4358-123">Make sure that you correctly quote backslash characters in endpoints.</span></span> <span data-ttu-id="e4358-124">Questo errore si verifica in genere quando l'endpoint è un named pipe.</span><span class="sxs-lookup"><span data-stu-id="e4358-124">This error commonly occurs when the endpoint is a named pipe.</span></span>

<span data-ttu-id="e4358-125">Le informazioni sull'endpoint specificate nel file IDL vengono utilizzate dalle funzioni di runtime RPC [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) e [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).</span><span class="sxs-lookup"><span data-stu-id="e4358-125">Endpoint information specified in the IDL file is used by the RPC run-time functions [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) and [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).</span></span>

## <a name="examples"></a><span data-ttu-id="e4358-126">Esempi</span><span class="sxs-lookup"><span data-stu-id="e4358-126">Examples</span></span>

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a><span data-ttu-id="e4358-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e4358-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4358-128">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="e4358-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e4358-129">**RpcServerUseAllProtseqsIf**</span><span class="sxs-lookup"><span data-stu-id="e4358-129">**RpcServerUseAllProtseqsIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[<span data-ttu-id="e4358-130">**RpcServerUseProtseqIf**</span><span class="sxs-lookup"><span data-stu-id="e4358-130">**RpcServerUseProtseqIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 