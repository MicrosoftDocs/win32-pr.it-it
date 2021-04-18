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
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a>Creazione manuale di un proxy del servizio per un servizio WCF

Il modo più semplice per creare un proxy del servizio client per un servizio Windows Communication Foundation (WCF) è il livello del [modello di servizio](service-model-layer-overview.md) con lo strumento WsUtil, come descritto nell'argomento [creazione di un client](creating-a-client.md) . Tuttavia, se necessario, è anche possibile creare manualmente un proxy del servizio. Questa API include una funzione [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) per la creazione del proxy del servizio, nonché strutture, enumerazioni e così via, per l'impostazione delle proprietà necessarie per interagire con WCF.

In WCF sono disponibili diverse associazioni standard, ciascuna destinata a uno scenario di utilizzo specifico. Quale associazione il servizio a cui si sta provando a connettersi USA, a sua volta, determina quali proprietà del canale è necessario personalizzare per il proxy del servizio per comunicare con il servizio.

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a>Creazione di un proxy del servizio per WSHttpBinding di WCF

WSHttpBinding è per lo scenario principale di servizi Web Internet. Usa la versione più recente di SOAP 1,2 e WS-Addressing versione 1,0 e Abilita un'ampia gamma di impostazioni di sicurezza sui trasporti HTTP e HTTPS pubblici. WWSAPI non dispone di un equivalente di WSHttpBinding (o di qualsiasi binding standard WCF), ma poiché la versione SOAP predefinita, la versione WS-Addressing e il formato di codifica corrispondono a quelli in WSHttpBinding, la creazione di un proxy del servizio per un servizio che utilizza WSHttpBinding è semplice. Ad esempio, per creare un proxy del servizio per comunicare con un endpoint WSHttpBinding senza sicurezza, è possibile usare semplicemente codice come il frammento di codice seguente (dichiarazione di variabile e la creazione dell'heap e degli errori viene omessa). Si noti che nella chiamata alla funzione [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) non è specificata alcuna proprietà del canale o descrizione della sicurezza.


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



La funzione crea il proxy del servizio e restituisce un puntatore al parametro *serviceProxy* (&proxy nella chiamata di funzione precedente).

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a>Creazione di un proxy del servizio per BasicHttpBinding di WCF

Quando si crea manualmente un proxy del servizio per un servizio WCF che utilizza un'associazione BasicHttpBinding, tuttavia, è necessario impostare la versione SOAP e WS-Addressing proprietà del canale. Il motivo è che WWSAPI è il valore predefinito di SOAP versione 1,2 e WS-Addressing 1,0. BasicHttpBinding di WCF, d'altra parte, usa la versione 1,1 di SOAP e nessun WS-Addressing.

Per impostare le proprietà della versione SOAP e WS-Addrssing del canale, dichiarare una matrice di strutture di [**\_ \_ proprietà del canale WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) che contengano le proprietà del canale e le informazioni correlate.


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



Passare quindi la matrice di proprietà del canale (channelProperties) e il numero di proprietà (channelPropertyCount) a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (o [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) se si lavora a livello di canale).


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



La matrice dichiarata per conservare le proprietà viene copiata in **WsCreateServiceProxy** e, di conseguenza, è possibile liberare la memoria per la matrice di proprietà immediatamente dopo aver chiamato la funzione. Inoltre, se si alloca la memoria dallo stack, ad esempio il frammento di codice precedente, è anche possibile restituire dalla funzione immediatamente dopo la chiamata.

## <a name="other-bindings"></a>Altre associazioni

Inoltre, WWSAPI fornisce meccanismi per la creazione di proxy di servizio per comunicare con i servizi WCF utilizzando altre associazioni, ad esempio NetTcpBinding e WSFederationHttpBinding. Molti di questi binding richiedono l'impostazione di proprietà del canale aggiuntive, ad esempio i descrittori di sicurezza. Per esempi che illustrano l'utilizzo di altre associazioni, vedere la sezione Esempi di [servizi Web Windows](windows-web-services-examples.md), in particolare gli esempi di livello del canale [TCP](tcp-channel-layer-examples.md), gli [esempi di livello del canale http](http-channel-layer-examples.md)e le sottosezioni degli esempi relativi al livello del canale di [sicurezza](security-channel-layer-examples.md) .

 

 




