---
title: Indirizzo endpoint
description: Un indirizzo endpoint rappresenta l'indirizzo di un servizio sulla rete.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Servizi Web per l'indirizzo endpoint per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104565182"
---
# <a name="endpoint-address"></a><span data-ttu-id="0dc19-106">Indirizzo endpoint</span><span class="sxs-lookup"><span data-stu-id="0dc19-106">Endpoint Address</span></span>

<span data-ttu-id="0dc19-107">Un indirizzo endpoint rappresenta l'indirizzo di un servizio sulla rete.</span><span class="sxs-lookup"><span data-stu-id="0dc19-107">An endpoint address represents the address of a service on the network.</span></span> <span data-ttu-id="0dc19-108">Quando si apre un [canale](channel.md), chiamando la funzione [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) , è necessario fornire l'indirizzo dell'endpoint del servizio con cui comunicare, oltre a specificare il canale che si vuole aprire.</span><span class="sxs-lookup"><span data-stu-id="0dc19-108">When you open a [channel](channel.md), by calling the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) function, you need to provide the endpoint address of the service you which to communicate with, as well as specifying the channel you wish to open.</span></span>


<span data-ttu-id="0dc19-109">Un indirizzo endpoint è costituito da:</span><span class="sxs-lookup"><span data-stu-id="0dc19-109">An endpoint address consists of:</span></span>

-   <span data-ttu-id="0dc19-110">un [URL](url.md)</span><span class="sxs-lookup"><span data-stu-id="0dc19-110">a [URL](url.md)</span></span>
-   <span data-ttu-id="0dc19-111">un set di intestazioni (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="0dc19-111">a set of headers (optional)</span></span>
-   <span data-ttu-id="0dc19-112">un set di estensioni (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="0dc19-112">a set of extensions (optional)</span></span>
-   <span data-ttu-id="0dc19-113">[identità](endpoint-identity.md) facoltativa che rappresenta l'identità di sicurezza del servizio.</span><span class="sxs-lookup"><span data-stu-id="0dc19-113">an optional [identity](endpoint-identity.md) representing the security identity of the service.</span></span>

<span data-ttu-id="0dc19-114">Quando un messaggio viene risolto, l'URL diventa l'intestazione "to" del messaggio.</span><span class="sxs-lookup"><span data-stu-id="0dc19-114">When a message is addressed, the URL becomes the "To" header of the message.</span></span> <span data-ttu-id="0dc19-115">Al messaggio vengono aggiunte anche tutte le intestazioni che fanno parte dell'indirizzo endpoint.</span><span class="sxs-lookup"><span data-stu-id="0dc19-115">Any headers that are part of the endpoint address are also added to the message.</span></span>

![Diagramma che mostra le intestazioni degli indirizzi endpoint aggiunti a un messaggio.](images/endpointaddress.png)

<span data-ttu-id="0dc19-117">I canali indirizzano automaticamente tutti i messaggi inviati, usando la struttura di [**\_ \_ indirizzi dell'endpoint WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) passata a [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span><span class="sxs-lookup"><span data-stu-id="0dc19-117">Channels automatically address any messages that are sent, using the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure that was passed to the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span></span> <span data-ttu-id="0dc19-118">È anche possibile usare la funzione [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) per eseguire l'override di questo comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="0dc19-118">You can also use the [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) function to override this default behavior.</span></span>

<span data-ttu-id="0dc19-119">Quando [**l' \_ \_ Indirizzo WS endpoint**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) viene passato come parametro, le funzioni [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) e [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) creano una copia del parametro **dell' \_ \_ indirizzo dell'endpoint WS** in memoria e la relativa dimensione è limitata a 65536 byte.</span><span class="sxs-lookup"><span data-stu-id="0dc19-119">When [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) is passed as a parameter, the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) and [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) functions create a copy of the **WS\_ENDPOINT\_ADDRESS** parameter in memory and its size is limited by 65536 bytes.</span></span> <span data-ttu-id="0dc19-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) non presenta questa limitazione perché non richiede la creazione di una copia del parametro dell' **\_ \_ indirizzo dell'endpoint WS** .</span><span class="sxs-lookup"><span data-stu-id="0dc19-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) does not have this limitation because it does not require creating a copy of the **WS\_ENDPOINT\_ADDRESS** parameter.</span></span>

<span data-ttu-id="0dc19-121">Le estensioni specificate nel campo **estensioni** di [**WS \_ endpoint \_ Address**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) non vengono utilizzate per indirizzare il messaggio, ma sono invece un meccanismo di estendibilità che può essere utilizzato per fornire informazioni aggiuntive (ad esempio, i metadati) sul servizio.</span><span class="sxs-lookup"><span data-stu-id="0dc19-121">The extensions specified in the **extensions** field of [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) are not used for addressing the message but instead are an extensibility mechanism that can be used to provide additional information (for example, metadata) about the service.</span></span> <span data-ttu-id="0dc19-122">Le estensioni comuni possono essere lette con la funzione [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) .</span><span class="sxs-lookup"><span data-stu-id="0dc19-122">Common extensions can be read with the [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) function.</span></span>

<span data-ttu-id="0dc19-123">Il campo Identity facoltativo dell'indirizzo endpoint può includere, ad esempio, il nome DNS del computer in cui è in esecuzione il servizio o l'UPN dell'account di Windows con cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="0dc19-123">The optional identity field of the endpoint address can include, for example, the DNS name of the machine on which the service is running, or the UPN of the Windows account under which the service is running.</span></span> <span data-ttu-id="0dc19-124">Il campo Identity non viene utilizzato per indirizzare il messaggio, ma può essere utilizzato per ottenere un token di sicurezza per il servizio (ad esempio, per ottenere un ticket Kerberos per l'UPN di destinazione) e per verificare l'identità delle risposte al servizio (ad esempio, un'identità DNS utilizzata per i controlli nome sul certificato del servizio restituito durante SSL).</span><span class="sxs-lookup"><span data-stu-id="0dc19-124">The identity field is not used in addressing the message, but may be used for obtaining a security token for the service (for example, for obtaining a Kerberos ticket to the target UPN) and for verifying the identity of the service replies (for example, a DNS identity used for name checks on the service certificate returned during SSL).</span></span>

<span data-ttu-id="0dc19-125">Gli indirizzi endpoint possono essere letti e scritti usando la [serializzazione](serialization.md) con il valore di enumerazione del **\_ \_ \_ tipo di indirizzo endpoint WS** da [**WS \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span><span class="sxs-lookup"><span data-stu-id="0dc19-125">Endpoint addresses can be read and written using [serialization](serialization.md) with the **WS\_ENDPOINT\_ADDRESS\_TYPE** enumeration value from [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="0dc19-126">Nota per serializzare un indirizzo endpoint, è necessario essere a conoscenza della versione della specifica utilizzata per le intestazioni di indirizzamento, come specificato nell'enumerazione della [**\_ \_ versione WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .</span><span class="sxs-lookup"><span data-stu-id="0dc19-126">Note in order to serialize an endpoint address, you must know the version of the specification used for the addressing headers, as specified in the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) enumeration.</span></span>

 

 




