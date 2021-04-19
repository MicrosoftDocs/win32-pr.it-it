---
description: Uso del computer HTTP rivoluzionato consentendo agli utenti di usare un Web browser per semplificare l'accesso alle informazioni su un server remoto in rete.
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Panoramica del servizio SOAP COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93ce7d80753f306777d3ac0b77dc46dc4e08d22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304839"
---
# <a name="com-soap-service-overview"></a><span data-ttu-id="06efc-103">Panoramica del servizio SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="06efc-103">COM+ SOAP Service Overview</span></span>

<span data-ttu-id="06efc-104">Uso del computer HTTP rivoluzionato consentendo agli utenti di usare un Web browser per semplificare l'accesso alle informazioni su un server remoto in rete.</span><span class="sxs-lookup"><span data-stu-id="06efc-104">HTTP revolutionized computer use by allowing people to use a Web browser for easy access to information on a remote server over a network.</span></span> <span data-ttu-id="06efc-105">I servizi Web XML hanno ora rivoluzionato lo sviluppo di applicazioni consentendo alle applicazioni client di chiamare facilmente metodi remoti in una rete.</span><span class="sxs-lookup"><span data-stu-id="06efc-105">XML web services have now revolutionized application development by allowing client applications to easily call remote methods over a network.</span></span>

<span data-ttu-id="06efc-106">Spesso è utile che un'applicazione client sia in grado di chiamare un metodo implementato in un server remoto.</span><span class="sxs-lookup"><span data-stu-id="06efc-106">It is often useful for a client application to be able to call a method implemented on a remote server.</span></span> <span data-ttu-id="06efc-107">In alcuni casi il metodo usa le informazioni volatili archiviate nel server remoto (ad esempio, un metodo che restituisce il prezzo corrente dello stock corrispondente a un simbolo del segno di spunta specificato).</span><span class="sxs-lookup"><span data-stu-id="06efc-107">Sometimes the method makes use of volatile information stored on the remote server (for example, a method that returns the current price of the stock corresponding to a given ticker symbol).</span></span> <span data-ttu-id="06efc-108">In altri casi, lo sviluppatore desidera avere la possibilità di aggiornare l'implementazione dei metodi senza dover ridistribuire tutte le applicazioni che lo usano.</span><span class="sxs-lookup"><span data-stu-id="06efc-108">At other times, the developer wants the ability to upgrade the methods implementation without having to redeploy all the applications that use it.</span></span>

<span data-ttu-id="06efc-109">Analogamente alle pagine Web, i servizi Web XML sono accessibili tramite un server Web, ad esempio IIS, tramite HTTP.</span><span class="sxs-lookup"><span data-stu-id="06efc-109">Like webpages, XML web services are accessed via a web server, such as IIS, using HTTP.</span></span> <span data-ttu-id="06efc-110">Tuttavia, anziché le pagine Web codificate in HTML, questi pacchetti HTTP contengono i parametri di input e di output delle chiamate a un metodo implementato nel server, codificato in SOAP.</span><span class="sxs-lookup"><span data-stu-id="06efc-110">However, instead of webpages encoded in HTML, these HTTP packets contain the input and output parameters of calls to a method implemented on the server, encoded in SOAP.</span></span>

<span data-ttu-id="06efc-111">Per utilizzare un servizio Web XML, è necessario individuare l'URL in cui il servizio viene esposto e il nome del metodo che si desidera chiamare ed è necessario fornire i parametri di input al metodo.</span><span class="sxs-lookup"><span data-stu-id="06efc-111">To use an XML web service, you need to know the URL where the service is exposed and the name of the method you want to call, and you must provide the input parameters to the method.</span></span> <span data-ttu-id="06efc-112">[Lo standard SOAP 1,1](https://www.w3.org/TR/SOAP/) fornisce l'esempio seguente di un pacchetto http che contiene una chiamata remota a un servizio Web XML all'indirizzo https://www.stockquoteserver.com/StockQuote , che restituisce il prezzo corrente dello stock corrispondente a un simbolo del segno di spunta specificato.</span><span class="sxs-lookup"><span data-stu-id="06efc-112">[The SOAP 1.1 standard](https://www.w3.org/TR/SOAP/) provides the following example of an HTTP packet containing a remote call to an XML web service at https://www.stockquoteserver.com/StockQuote, which returns the current price of the stock corresponding to a given ticker symbol.</span></span>

``` syntax
POST /StockQuote HTTP/1.1
Host: www.stockquoteserver.com
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn
SOAPAction: "Some-URI"

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding/">
<SOAP-ENV:Body>
<m:GetLastTradePrice xmlns:m="Some-URI">
<symbol>DIS</symbol>
</m:GetLastTradePrice>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="06efc-113">Come illustrato nell'esempio precedente, SOAP è un'istanza XML che può essere incorporata in una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="06efc-113">As the preceding example illustrates, SOAP is an XML instance that can be embedded in an HTTP request.</span></span> <span data-ttu-id="06efc-114">Analogamente, il risultato viene restituito come pacchetto HTTP con un payload SOAP, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="06efc-114">Similarly, the result is returned as an HTTP packet with a SOAP payload, as shown in the following example.</span></span>

``` syntax
HTTP/1.1 200 OK
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding//">
<SOAP-ENV:Body>
<m:GetLastTradePriceResponse xmlns:m="Some-URI">
<Price>34.5</Price>
</m:GetLastTradePriceResponse>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="06efc-115">Sebbene sia utile avere una certa conoscenza dell'infrastruttura sottostante ai servizi Web XML, COM+ semplifica la creazione e l'utilizzo di servizi Web XML che spesso non devono essere approfonditi a questo livello.</span><span class="sxs-lookup"><span data-stu-id="06efc-115">While it is helpful to have some understanding of the infrastructure that underlies XML web services, COM+ makes it so easy to create and use XML web services that you won't often have to delve to this level.</span></span>

<span data-ttu-id="06efc-116">È possibile esporre i metodi nelle interfacce predefinite dei componenti COM configurati in qualsiasi applicazione COM+ come un servizio Web XML.</span><span class="sxs-lookup"><span data-stu-id="06efc-116">You can expose the methods in the default interfaces of the configured COM components in any COM+ application as an XML web service.</span></span> <span data-ttu-id="06efc-117">Non sono necessarie particolari considerazioni di programmazione quando si scrivono i componenti, ad eccezione del fatto che i metodi che si desidera esporre devono trovarsi nell'interfaccia predefinita e il componente deve essere configurato (nel catalogo COM+ del server).</span><span class="sxs-lookup"><span data-stu-id="06efc-117">No special programming considerations are necessary when writing the components, except that the methods you want to expose must be in the default interface and the component must be configured (in your server's COM+ catalog).</span></span> <span data-ttu-id="06efc-118">Non è necessario scrivere codice per comunicare tramite un'interfaccia di rete o per analizzare SOAP.</span><span class="sxs-lookup"><span data-stu-id="06efc-118">You need not write code to communicate via a network interface or to parse SOAP.</span></span> <span data-ttu-id="06efc-119">Per istruzioni dettagliate sull'utilizzo del servizio SOAP COM+ per la creazione di un servizio Web XML, vedere [creazione di servizi Web XML](creating-xml-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="06efc-119">For detailed instructions about using the COM+ SOAP service to create an XML web service, see [Creating XML Web Services](creating-xml-web-services.md).</span></span>

<span data-ttu-id="06efc-120">Quando si espone un'applicazione COM+ come servizio Web XML, le informazioni dettagliate sulla sintassi di tutti i metodi disponibili in un servizio Web XML vengono pubblicate automaticamente utilizzando il Web Services Description Language (WSDL).</span><span class="sxs-lookup"><span data-stu-id="06efc-120">When you expose a COM+ application as an XML web service, detailed information about the syntax of all the methods available from an XML web service is published automatically, using the Web Services Description Language (WSDL).</span></span> <span data-ttu-id="06efc-121">Queste informazioni vengono utilizzate dai client che utilizzano il servizio Web XML.</span><span class="sxs-lookup"><span data-stu-id="06efc-121">This information is used by clients that use your XML web service.</span></span>

<span data-ttu-id="06efc-122">COM+ fornisce due modi per accedere e utilizzare un servizio Web XML remoto, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="06efc-122">COM+ provides two ways for you to access and use a remote XML web service, as follows:</span></span>

-   <span data-ttu-id="06efc-123">La modalità WKO ( *well-known Object* ) può essere utilizzata per accedere a qualsiasi servizio Web XML che pubblica la sintassi utilizzando WSDL, anche se il servizio Web XML non è stato creato utilizzando com+ o anche Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="06efc-123">The *well-known object* (WKO) mode can be used to access any XML web service that publishes its syntax using WSDL, even if that XML web service was not created using COM+ or even Microsoft Windows.</span></span>
-   <span data-ttu-id="06efc-124">La modalità *oggetto attivato dal client* (Cao) può essere utilizzata solo per accedere ai servizi Web XML creati esponendo applicazioni com+.</span><span class="sxs-lookup"><span data-stu-id="06efc-124">The *client-activated object* (CAO) mode can be used only to access XML web services created by exposing COM+ applications.</span></span> <span data-ttu-id="06efc-125">La modalità CAO aumenta le prestazioni usando connessioni permanenti, una funzionalità non supportata dallo standard SOAP corrente.</span><span class="sxs-lookup"><span data-stu-id="06efc-125">CAO mode increases performance by using persistent connections, a feature not supported by the current SOAP standard.</span></span>

<span data-ttu-id="06efc-126">Entrambi i metodi consentono alle applicazioni client di chiamare i metodi dei servizi Web XML in modalità remota in modo semplice, senza dover scrivere codice per comunicare tramite un'interfaccia di rete o l'analisi SOAP.</span><span class="sxs-lookup"><span data-stu-id="06efc-126">Both methods allow client applications to call the methods of XML web services remotely in a straightforward fashion, without having to write code to communicate via a network interface or parse SOAP.</span></span> <span data-ttu-id="06efc-127">Per informazioni dettagliate su come accedere ai servizi Web XML in entrambe le modalità, vedere [accesso ai servizi Web XML in modalità Cao](accessing-xml-web-services-in-cao-mode.md) e [accesso ai servizi Web XML in modalità WKO](accessing-xml-web-services-in-wko-mode.md).</span><span class="sxs-lookup"><span data-stu-id="06efc-127">For details about how to access XML web services in either mode, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md) and [Accessing XML Web Services in WKO Mode](accessing-xml-web-services-in-wko-mode.md).</span></span>

> [!Note]  
> <span data-ttu-id="06efc-128">COM+ supporta solo la specifica SOAP-RPC, non la specifica SOAP-Document.</span><span class="sxs-lookup"><span data-stu-id="06efc-128">COM+ supports only the SOAP-RPC specification, not the SOAP-Document specification.</span></span>

 

<span data-ttu-id="06efc-129">COM+ rende particolarmente semplice l'utilizzo di servizi Web XML, consentendo di utilizzare le applicazioni COM+ esistenti come servizi Web XML in modalità CAO in modo completamente trasparente.</span><span class="sxs-lookup"><span data-stu-id="06efc-129">COM+ makes using XML web services especially easy by allowing you to use existing COM+ applications as XML web services in CAO mode in a completely transparent fashion.</span></span> <span data-ttu-id="06efc-130">Se si [Esporta](exporting-a-soap-enabled-application.md) un'applicazione com+ che è stata esposta come servizio Web XML dal server, qualsiasi client che [Importa](importing-a-soap-enabled-application.md) l'applicazione può utilizzare in modo trasparente il servizio Web XML del server ogni volta che viene utilizzata l'applicazione importata.</span><span class="sxs-lookup"><span data-stu-id="06efc-130">If you [export](exporting-a-soap-enabled-application.md) a COM+ application that has been exposed as an XML web service from your server, any client that [imports](importing-a-soap-enabled-application.md) the application can transparently use the server's XML web service whenever the imported application is used.</span></span> <span data-ttu-id="06efc-131">Questa funzionalità rende molto semplice la conversione di applicazioni COM+ esistenti in servizi Web XML e la distribuzione di tali servizi in una rete.</span><span class="sxs-lookup"><span data-stu-id="06efc-131">This facility makes the conversion of existing COM+ applications to XML web services and the deployment of those services over a network very easy.</span></span>

<span data-ttu-id="06efc-132">L'utilizzo dei servizi Web XML presenta diversi vantaggi esclusivi rispetto alle implementazioni alternative di RPC (Remote Procedure Call), incluse le seguenti:</span><span class="sxs-lookup"><span data-stu-id="06efc-132">Using XML web services has several unique advantages over alternative implementations of remote procedure calls (RPC), including the following:</span></span>

-   <span data-ttu-id="06efc-133">SOAP è una vera implementazione RPC multipiattaforma, che aumenta l'interoperabilità.</span><span class="sxs-lookup"><span data-stu-id="06efc-133">SOAP is a true cross-platform RPC implementation, which increases interoperability.</span></span>
-   <span data-ttu-id="06efc-134">I servizi Web XML supportano i metodi con parametri di input e di output.</span><span class="sxs-lookup"><span data-stu-id="06efc-134">XML web services support methods with both input and output parameters.</span></span>
-   <span data-ttu-id="06efc-135">I servizi Web XML vengono eseguiti su HTTP, che in genere possono penetrare firewall che potrebbero bloccare altre implementazioni RPC.</span><span class="sxs-lookup"><span data-stu-id="06efc-135">XML web services run over HTTP, which can usually penetrate firewalls that might block other RPC implementations.</span></span>
-   <span data-ttu-id="06efc-136">Quando un servizio Web XML viene implementato utilizzando COM+, lo sviluppatore non deve scrivere codice specializzato; si tratta di un enorme vantaggio rispetto ai meccanismi RPC alternativi.</span><span class="sxs-lookup"><span data-stu-id="06efc-136">When an XML web service is implemented using COM+, the developer does not have to write any specialized code; this is a tremendous advantage over alternative RPC mechanisms.</span></span>

> [!Note]  
> <span data-ttu-id="06efc-137">I servizi Web XML non supportano le chiamate transazionali asincrone o in modo trasparente.</span><span class="sxs-lookup"><span data-stu-id="06efc-137">XML web services do not support asynchronous or transparently transactional calls.</span></span> <span data-ttu-id="06efc-138">Utilizzare il servizio [componenti in coda com+](com--queued-components.md) quando è necessaria questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="06efc-138">Use the [COM+ Queued Components](com--queued-components.md) service when you require this functionality.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="06efc-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06efc-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06efc-140">Considerazioni sulla sicurezza del servizio SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="06efc-140">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



