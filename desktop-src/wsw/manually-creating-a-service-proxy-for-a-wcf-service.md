---
title: Creazione manuale di un proxy del servizio per un servizio WCF
description: Il modo più semplice per creare un proxy del servizio client per un servizio Windows Communication Foundation (WCF) è il livello del modello di servizio con lo strumento WsUtil, come descritto nell'argomento Creazione di un client.
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e061fda95298986ee6336dee0662d80c89a0a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298485"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a><span data-ttu-id="aa562-103">Creazione manuale di un proxy del servizio per un servizio WCF</span><span class="sxs-lookup"><span data-stu-id="aa562-103">Manually Creating a Service Proxy for a WCF Service</span></span>

<span data-ttu-id="aa562-104">Il modo più semplice per creare un proxy del servizio client per un servizio Windows Communication Foundation (WCF) è il livello del [modello di servizio](service-model-layer-overview.md) con lo strumento WsUtil, come descritto nell'argomento [creazione di un client](creating-a-client.md) .</span><span class="sxs-lookup"><span data-stu-id="aa562-104">The easiest way to create a client service proxy for a Windows Communication Foundation (WCF) service is at the [Service Model](service-model-layer-overview.md) layer with the WsUtil tool, as described in the [Creating a Client](creating-a-client.md) topic.</span></span> <span data-ttu-id="aa562-105">Tuttavia, se necessario, è anche possibile creare manualmente un proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="aa562-105">However, if necessary, you can also create a service proxy manually.</span></span> <span data-ttu-id="aa562-106">Questa API include una funzione [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) per la creazione del proxy del servizio, nonché strutture, enumerazioni e così via, per l'impostazione delle proprietà necessarie per interagire con WCF.</span><span class="sxs-lookup"><span data-stu-id="aa562-106">This API includes a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function for creating the service proxy as well as structures, enumerations, and so on for setting the properties necessary to interoperate with WCF.</span></span>

<span data-ttu-id="aa562-107">In WCF sono disponibili diverse associazioni standard, ciascuna destinata a uno scenario di utilizzo specifico.</span><span class="sxs-lookup"><span data-stu-id="aa562-107">WCF provides a number of standard bindings, each targeting a specific usage scenario.</span></span> <span data-ttu-id="aa562-108">Quale associazione il servizio a cui si sta provando a connettersi USA, a sua volta, determina quali proprietà del canale è necessario personalizzare per il proxy del servizio per comunicare con il servizio.</span><span class="sxs-lookup"><span data-stu-id="aa562-108">Which binding the service you are trying to connect to uses, in turn, determines which channel properties you need to customize for your service proxy to communicate with the service.</span></span>

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a><span data-ttu-id="aa562-109">Creazione di un proxy del servizio per WSHttpBinding di WCF</span><span class="sxs-lookup"><span data-stu-id="aa562-109">Creating a Service Proxy for WCF's WSHttpBinding</span></span>

<span data-ttu-id="aa562-110">WSHttpBinding è per lo scenario principale di servizi Web Internet.</span><span class="sxs-lookup"><span data-stu-id="aa562-110">WSHttpBinding is for the mainline Internet web services scenario.</span></span> <span data-ttu-id="aa562-111">Usa la versione più recente di SOAP 1,2 e WS-Addressing versione 1,0 e Abilita un'ampia gamma di impostazioni di sicurezza sui trasporti HTTP e HTTPS pubblici.</span><span class="sxs-lookup"><span data-stu-id="aa562-111">It uses the newer SOAP version 1.2 and WS-Addressing version 1.0 and enables a wide range of security settings over the public HTTP and HTTPS transports.</span></span> <span data-ttu-id="aa562-112">WWSAPI non dispone di un equivalente di WSHttpBinding (o di qualsiasi binding standard WCF), ma poiché la versione SOAP predefinita, la versione WS-Addressing e il formato di codifica corrispondono a quelli in WSHttpBinding, la creazione di un proxy del servizio per un servizio che utilizza WSHttpBinding è semplice.</span><span class="sxs-lookup"><span data-stu-id="aa562-112">WWSAPI does not have an equivalent of the WSHttpBinding (or any of the WCF standard bindings, for that matter), but since its default SOAP version, WS-Addressing version, and encoding format match those in WSHttpBinding, creating a service proxy for a service that uses the WSHttpBinding is straightforward.</span></span> <span data-ttu-id="aa562-113">Ad esempio, per creare un proxy del servizio per comunicare con un endpoint WSHttpBinding senza sicurezza, è possibile usare semplicemente codice come il frammento di codice seguente (dichiarazione di variabile e la creazione dell'heap e degli errori viene omessa).</span><span class="sxs-lookup"><span data-stu-id="aa562-113">For example, to create a service proxy to talk to a WSHttpBinding endpoint without security, you can simply use code like following snippet (variable declaration, and heap and error creation are omitted).</span></span> <span data-ttu-id="aa562-114">Si noti che nella chiamata alla funzione [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) non è specificata alcuna proprietà del canale o descrizione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="aa562-114">Notice that no channel properties or security description is specified in the call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span>


```C++
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        NULL, // channel properties
        0, // channel property count
        &proxy, 
        error);
```



<span data-ttu-id="aa562-115">La funzione crea il proxy del servizio e restituisce un puntatore al parametro *serviceProxy* (&proxy nella chiamata di funzione precedente).</span><span class="sxs-lookup"><span data-stu-id="aa562-115">The function creates the service proxy and returns a pointer to it in the *serviceProxy* parameter (&proxy in the function call above).</span></span>

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a><span data-ttu-id="aa562-116">Creazione di un proxy del servizio per BasicHttpBinding di WCF</span><span class="sxs-lookup"><span data-stu-id="aa562-116">Creating a Service Proxy for WCF's BasicHttpBinding</span></span>

<span data-ttu-id="aa562-117">Quando si crea manualmente un proxy del servizio per un servizio WCF che utilizza un'associazione BasicHttpBinding, tuttavia, è necessario impostare la versione SOAP e WS-Addressing proprietà del canale.</span><span class="sxs-lookup"><span data-stu-id="aa562-117">When you manually create a service proxy for a WCF service that uses a BasicHttpBinding binding, however, it is necessary to set the SOAP version and WS-Addressing properties of the channel.</span></span> <span data-ttu-id="aa562-118">Il motivo è che WWSAPI è il valore predefinito di SOAP versione 1,2 e WS-Addressing 1,0.</span><span class="sxs-lookup"><span data-stu-id="aa562-118">This is because WWSAPI defaults to SOAP version 1.2 and WS-Addressing 1.0.</span></span> <span data-ttu-id="aa562-119">BasicHttpBinding di WCF, d'altra parte, usa la versione 1,1 di SOAP e nessun WS-Addressing.</span><span class="sxs-lookup"><span data-stu-id="aa562-119">WCF's BasicHttpBinding, on the other hand, uses SOAP version 1.1 and no WS-Addressing.</span></span>

<span data-ttu-id="aa562-120">Per impostare le proprietà della versione SOAP e WS-Addrssing del canale, dichiarare una matrice di strutture di [**\_ \_ proprietà del canale WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) che contengano le proprietà del canale e le informazioni correlate.</span><span class="sxs-lookup"><span data-stu-id="aa562-120">To set the SOAP version and WS-Addrssing properties of the channel, declare an array of [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) structures to hold the channel properties and related information.</span></span>


```
WS_CHANNEL_PROPERTY channelProperties[4]; // Array to hold up to 4 channel properties

ULONG channelPropertyCount = 0; // Count of properties set
 
WS_ENVELOPE_VERSION soapVersion = WS_ENVELOPE_VERSION_SOAP_1_1; // Set required SOAP version
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ENVELOPE_VERSION; // Type of first channel property
channelProperties[channelPropertyCount].value = &soapVersion; // Address of the SOAP version value
channelProperties[channelPropertyCount].valueSize = sizeof(soapVersion); // Size of the value
channelPropertyCount++; // Increment property count
 
WS_ADDRESSING_VERSION addressingVersion = WS_ADDRESSING_VERSION_TRANSPORT; // Set required WS-Addressing value
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ADDRESSING_VERSION; // Type of second channel property
channelProperties[channelPropertyCount].value = &addressingVersion ; // Address of the WS-Addressing value
channelProperties[channelPropertyCount].valueSize = sizeof(addressingVersion ); // Size of the value
channelPropertyCount++; // Increment property count
 
// add more channel properties here

```



<span data-ttu-id="aa562-121">Passare quindi la matrice di proprietà del canale (channelProperties) e il numero di proprietà (channelPropertyCount) a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (o [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) se si lavora a livello di canale).</span><span class="sxs-lookup"><span data-stu-id="aa562-121">Then pass the array of channel properties (channelProperties) and the count of properties (channelPropertyCount) to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (or [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) if you are working at channel layer).</span></span>


```
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        channelProperties, // channel properties
        channelPropertyCount, // channel property count
        &proxy, 
        error);
```



<span data-ttu-id="aa562-122">La matrice dichiarata per conservare le proprietà viene copiata in **WsCreateServiceProxy** e, di conseguenza, è possibile liberare la memoria per la matrice di proprietà immediatamente dopo aver chiamato la funzione.</span><span class="sxs-lookup"><span data-stu-id="aa562-122">The array you declared to hold the properties is copied in **WsCreateServiceProxy**, and as a result, you can free the memory for the property array immediately after calling the function.</span></span> <span data-ttu-id="aa562-123">Inoltre, se si alloca la memoria dallo stack, ad esempio il frammento di codice precedente, è anche possibile restituire dalla funzione immediatamente dopo la chiamata.</span><span class="sxs-lookup"><span data-stu-id="aa562-123">Also, if you allocate the memory from the stack (like the code snippet above), you can also return from the function immediately after the call.</span></span>

## <a name="other-bindings"></a><span data-ttu-id="aa562-124">Altre associazioni</span><span class="sxs-lookup"><span data-stu-id="aa562-124">Other Bindings</span></span>

<span data-ttu-id="aa562-125">Inoltre, WWSAPI fornisce meccanismi per la creazione di proxy di servizio per comunicare con i servizi WCF utilizzando altre associazioni, ad esempio NetTcpBinding e WSFederationHttpBinding.</span><span class="sxs-lookup"><span data-stu-id="aa562-125">In addition, WWSAPI provides mechanisms for creating service proxies to communicate with WCF services using other bindings, such as NetTcpBinding and WSFederationHttpBinding.</span></span> <span data-ttu-id="aa562-126">Molti di questi binding richiedono l'impostazione di proprietà del canale aggiuntive, ad esempio i descrittori di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="aa562-126">Many of these binding require setting additional channel properties, such as security descriptors.</span></span> <span data-ttu-id="aa562-127">Per esempi che illustrano l'utilizzo di altre associazioni, vedere la sezione Esempi di [servizi Web Windows](windows-web-services-examples.md), in particolare gli esempi di livello del canale [TCP](tcp-channel-layer-examples.md), gli [esempi di livello del canale http](http-channel-layer-examples.md)e le sottosezioni degli esempi relativi al livello del canale di [sicurezza](security-channel-layer-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="aa562-127">For examples that illustrate using other bindings, see the [Windows Web Services Examples](windows-web-services-examples.md), section, in particular the [TCP Channel Layer Examples](tcp-channel-layer-examples.md), [HTTP Channel Layer Examples](http-channel-layer-examples.md), and [Security Channel Layer Examples](security-channel-layer-examples.md) subsections.</span></span>

 

 




