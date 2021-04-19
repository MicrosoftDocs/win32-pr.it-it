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
# <a name="com-soap-service-overview"></a>Panoramica del servizio SOAP COM+

Uso del computer HTTP rivoluzionato consentendo agli utenti di usare un Web browser per semplificare l'accesso alle informazioni su un server remoto in rete. I servizi Web XML hanno ora rivoluzionato lo sviluppo di applicazioni consentendo alle applicazioni client di chiamare facilmente metodi remoti in una rete.

Spesso è utile che un'applicazione client sia in grado di chiamare un metodo implementato in un server remoto. In alcuni casi il metodo usa le informazioni volatili archiviate nel server remoto (ad esempio, un metodo che restituisce il prezzo corrente dello stock corrispondente a un simbolo del segno di spunta specificato). In altri casi, lo sviluppatore desidera avere la possibilità di aggiornare l'implementazione dei metodi senza dover ridistribuire tutte le applicazioni che lo usano.

Analogamente alle pagine Web, i servizi Web XML sono accessibili tramite un server Web, ad esempio IIS, tramite HTTP. Tuttavia, anziché le pagine Web codificate in HTML, questi pacchetti HTTP contengono i parametri di input e di output delle chiamate a un metodo implementato nel server, codificato in SOAP.

Per utilizzare un servizio Web XML, è necessario individuare l'URL in cui il servizio viene esposto e il nome del metodo che si desidera chiamare ed è necessario fornire i parametri di input al metodo. [Lo standard SOAP 1,1](https://www.w3.org/TR/SOAP/) fornisce l'esempio seguente di un pacchetto http che contiene una chiamata remota a un servizio Web XML all'indirizzo https://www.stockquoteserver.com/StockQuote , che restituisce il prezzo corrente dello stock corrispondente a un simbolo del segno di spunta specificato.

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

Come illustrato nell'esempio precedente, SOAP è un'istanza XML che può essere incorporata in una richiesta HTTP. Analogamente, il risultato viene restituito come pacchetto HTTP con un payload SOAP, come illustrato nell'esempio seguente.

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

Sebbene sia utile avere una certa conoscenza dell'infrastruttura sottostante ai servizi Web XML, COM+ semplifica la creazione e l'utilizzo di servizi Web XML che spesso non devono essere approfonditi a questo livello.

È possibile esporre i metodi nelle interfacce predefinite dei componenti COM configurati in qualsiasi applicazione COM+ come un servizio Web XML. Non sono necessarie particolari considerazioni di programmazione quando si scrivono i componenti, ad eccezione del fatto che i metodi che si desidera esporre devono trovarsi nell'interfaccia predefinita e il componente deve essere configurato (nel catalogo COM+ del server). Non è necessario scrivere codice per comunicare tramite un'interfaccia di rete o per analizzare SOAP. Per istruzioni dettagliate sull'utilizzo del servizio SOAP COM+ per la creazione di un servizio Web XML, vedere [creazione di servizi Web XML](creating-xml-web-services.md).

Quando si espone un'applicazione COM+ come servizio Web XML, le informazioni dettagliate sulla sintassi di tutti i metodi disponibili in un servizio Web XML vengono pubblicate automaticamente utilizzando il Web Services Description Language (WSDL). Queste informazioni vengono utilizzate dai client che utilizzano il servizio Web XML.

COM+ fornisce due modi per accedere e utilizzare un servizio Web XML remoto, come indicato di seguito:

-   La modalità WKO ( *well-known Object* ) può essere utilizzata per accedere a qualsiasi servizio Web XML che pubblica la sintassi utilizzando WSDL, anche se il servizio Web XML non è stato creato utilizzando com+ o anche Microsoft Windows.
-   La modalità *oggetto attivato dal client* (Cao) può essere utilizzata solo per accedere ai servizi Web XML creati esponendo applicazioni com+. La modalità CAO aumenta le prestazioni usando connessioni permanenti, una funzionalità non supportata dallo standard SOAP corrente.

Entrambi i metodi consentono alle applicazioni client di chiamare i metodi dei servizi Web XML in modalità remota in modo semplice, senza dover scrivere codice per comunicare tramite un'interfaccia di rete o l'analisi SOAP. Per informazioni dettagliate su come accedere ai servizi Web XML in entrambe le modalità, vedere [accesso ai servizi Web XML in modalità Cao](accessing-xml-web-services-in-cao-mode.md) e [accesso ai servizi Web XML in modalità WKO](accessing-xml-web-services-in-wko-mode.md).

> [!Note]  
> COM+ supporta solo la specifica SOAP-RPC, non la specifica SOAP-Document.

 

COM+ rende particolarmente semplice l'utilizzo di servizi Web XML, consentendo di utilizzare le applicazioni COM+ esistenti come servizi Web XML in modalità CAO in modo completamente trasparente. Se si [Esporta](exporting-a-soap-enabled-application.md) un'applicazione com+ che è stata esposta come servizio Web XML dal server, qualsiasi client che [Importa](importing-a-soap-enabled-application.md) l'applicazione può utilizzare in modo trasparente il servizio Web XML del server ogni volta che viene utilizzata l'applicazione importata. Questa funzionalità rende molto semplice la conversione di applicazioni COM+ esistenti in servizi Web XML e la distribuzione di tali servizi in una rete.

L'utilizzo dei servizi Web XML presenta diversi vantaggi esclusivi rispetto alle implementazioni alternative di RPC (Remote Procedure Call), incluse le seguenti:

-   SOAP è una vera implementazione RPC multipiattaforma, che aumenta l'interoperabilità.
-   I servizi Web XML supportano i metodi con parametri di input e di output.
-   I servizi Web XML vengono eseguiti su HTTP, che in genere possono penetrare firewall che potrebbero bloccare altre implementazioni RPC.
-   Quando un servizio Web XML viene implementato utilizzando COM+, lo sviluppatore non deve scrivere codice specializzato; si tratta di un enorme vantaggio rispetto ai meccanismi RPC alternativi.

> [!Note]  
> I servizi Web XML non supportano le chiamate transazionali asincrone o in modo trasparente. Utilizzare il servizio [componenti in coda com+](com--queued-components.md) quando è necessaria questa funzionalità.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni sulla sicurezza del servizio SOAP COM+](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



