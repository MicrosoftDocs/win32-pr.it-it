---
description: HTTP ha rivoluzionato l'uso del computer consentendo agli utenti di usare un Web browser per un facile accesso alle informazioni su un server remoto tramite una rete.
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Cenni preliminari sul servizio SOAP COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68501d80596d8547715cb1694fe77a17a3ab4b6955ad1e1acd596f249be5f231
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096871"
---
# <a name="com-soap-service-overview"></a>Cenni preliminari sul servizio SOAP COM+

HTTP ha rivoluzionato l'uso del computer consentendo agli utenti di usare un Web browser per un facile accesso alle informazioni su un server remoto tramite una rete. I servizi Web XML hanno ora rivoluzionato lo sviluppo di applicazioni consentendo alle applicazioni client di chiamare facilmente metodi remoti in rete.

Spesso è utile che un'applicazione client sia in grado di chiamare un metodo implementato in un server remoto. In alcuni casi il metodo usa informazioni volatili archiviate nel server remoto, ad esempio un metodo che restituisce il prezzo corrente del titolo corrispondente a un simbolo ticker specificato. In altri casi, lo sviluppatore vuole la possibilità di aggiornare l'implementazione dei metodi senza dover ridistribuire tutte le applicazioni che la usano.

Analogamente alle pagine Web, i servizi Web XML sono accessibili tramite un server Web, ad esempio IIS, tramite HTTP. Tuttavia, anziché le pagine Web codificate in HTML, questi pacchetti HTTP contengono i parametri di input e output delle chiamate a un metodo implementato nel server, codificati in SOAP.

Per usare un servizio Web XML, è necessario conoscere l'URL in cui è esposto il servizio e il nome del metodo da chiamare ed è necessario fornire i parametri di input al metodo . [Lo standard SOAP 1.1](https://www.w3.org/TR/SOAP/) fornisce l'esempio seguente di un pacchetto HTTP contenente una chiamata remota a un servizio Web XML in , che restituisce il prezzo corrente del titolo corrispondente a un simbolo https://www.stockquoteserver.com/StockQuote ticker specificato.

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

Sebbene sia utile conoscere l'infrastruttura alla base dei servizi Web XML, COM+ semplifica la creazione e l'uso di servizi Web XML che spesso non è necessario approfondire a questo livello.

È possibile esporre i metodi nelle interfacce predefinite dei componenti COM configurati in qualsiasi applicazione COM+ come servizio Web XML. Non sono necessarie considerazioni di programmazione speciali quando si scrivono i componenti, ad eccezione del fatto che i metodi da esporre devono essere nell'interfaccia predefinita e il componente deve essere configurato (nel catalogo COM+ del server). Non è necessario scrivere codice per comunicare tramite un'interfaccia di rete o per analizzare SOAP. Per istruzioni dettagliate sull'uso del servizio SOAP COM+ per creare un servizio Web XML, vedere [Creazione di servizi Web XML](creating-xml-web-services.md).

Quando si espone un'applicazione COM+ come servizio Web XML, le informazioni dettagliate sulla sintassi di tutti i metodi disponibili da un servizio Web XML vengono pubblicate automaticamente usando Web Services Description Language (WSDL). Queste informazioni vengono usate dai client che usano il servizio Web XML.

COM+ offre due modi per accedere e usare un servizio Web XML remoto, come indicato di seguito:

-   La modalità WKO *(Well-Known Object)* può essere usata per accedere a qualsiasi servizio Web XML che pubblica la sintassi tramite WSDL, anche se tale servizio Web XML non è stato creato usando COM+ o microsoft Windows.
-   La *modalità CAO (Client-Activated Object)* può essere usata solo per accedere ai servizi Web XML creati esponendo applicazioni COM+. La modalità CAO aumenta le prestazioni usando connessioni permanenti, una funzionalità non supportata dallo standard SOAP corrente.

Entrambi i metodi consentono alle applicazioni client di chiamare i metodi dei servizi Web XML in modalità remota in modo semplice, senza dover scrivere codice per comunicare tramite un'interfaccia di rete o analizzare SOAP. Per informazioni dettagliate su come accedere ai servizi Web XML in entrambe le modalità, vedere Accesso ai servizi [Web XML in modalità CAO](accessing-xml-web-services-in-cao-mode.md) e Accesso ai servizi Web XML in modalità [WKO](accessing-xml-web-services-in-wko-mode.md).

> [!Note]  
> COM+ supporta solo la specifica SOAP-RPC, non SOAP-Document specifica.

 

COM+ semplifica particolarmente l'uso dei servizi Web XML consentendo di usare le applicazioni COM+ esistenti come servizi Web XML in modalità CAO in modo completamente trasparente. Se [](exporting-a-soap-enabled-application.md) si esporta un'applicazione COM+ esposta come servizio Web XML [](importing-a-soap-enabled-application.md) dal server, qualsiasi client che importa l'applicazione può usare in modo trasparente il servizio Web XML del server ogni volta che viene usata l'applicazione importata. Questa funzionalità semplifica la conversione di applicazioni COM+ esistenti in servizi Web XML e la distribuzione di tali servizi in rete.

L'uso dei servizi Web XML offre diversi vantaggi univoci rispetto alle implementazioni alternative di chiamate di procedura remota (RPC), tra cui:

-   SOAP è una vera implementazione RPC multipiattaforma, che aumenta l'interoperabilità.
-   I servizi Web XML supportano metodi con parametri di input e di output.
-   I servizi Web XML vengono eseguiti su HTTP, che in genere può penetrare i firewall che potrebbero bloccare altre implementazioni RPC.
-   Quando un servizio Web XML viene implementato tramite COM+, lo sviluppatore non deve scrivere codice specializzato. si tratta di un enorme vantaggio rispetto ai meccanismi RPC alternativi.

> [!Note]  
> I servizi Web XML non supportano chiamate asincrone o transazionali in modo trasparente. Usare il [servizio Componenti in coda COM+](com--queued-components.md) quando è necessaria questa funzionalità.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni sulla sicurezza dei servizi SOAP COM+](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



