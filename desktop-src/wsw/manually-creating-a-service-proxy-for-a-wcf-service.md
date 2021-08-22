---
title: Creazione manuale di un proxy del servizio per un servizio WCF
description: Il modo più semplice per creare un proxy del servizio client per un servizio Windows Communication Foundation (WCF) è a livello di modello di servizio con lo strumento WsUtil, come descritto nell'argomento Creazione di un client.
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33133ae48dee89e72871712d445453e237116f6f1fa08cf66a76381ea8d3d424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927251"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a>Creazione manuale di un proxy del servizio per un servizio WCF

Il modo più semplice per creare un proxy del servizio client per un [](service-model-layer-overview.md) servizio Windows Communication Foundation (WCF) è al livello del modello di servizio con lo strumento WsUtil, come descritto nell'argomento Creazione di [un client.](creating-a-client.md) Se necessario, tuttavia, è anche possibile creare manualmente un proxy del servizio. Questa API include una [**funzione WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) per la creazione del proxy del servizio, nonché strutture, enumerazioni e così via per l'impostazione delle proprietà necessarie per l'interoperabilità con WCF.

WCF fornisce una serie di associazioni standard, ognuna delle quali ha come destinazione uno scenario di utilizzo specifico. L'associazione del servizio a cui si sta tentando di connettersi usa, a sua volta, determina le proprietà del canale che è necessario personalizzare per il proxy del servizio per comunicare con il servizio.

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a>Creazione di un proxy del servizio per WSHttpBinding di WCF

WSHttpBinding è per lo scenario principale dei servizi Web Internet. Usa le versioni soap 1.2 e WS-Addressing 1.0 più nuove e abilita un'ampia gamma di impostazioni di sicurezza sui trasporti HTTP e HTTPS pubblici. WWSAPI non ha un equivalente di WSHttpBinding (o di qualsiasi associazione standard WCF, in questo caso), ma poiché la versione SOAP predefinita, la versione WS-Addressing e il formato di codifica corrispondono a quelli in WSHttpBinding, la creazione di un proxy del servizio per un servizio che usa WSHttpBinding è semplice. Ad esempio, per creare un proxy del servizio per la conversazione con un endpoint WSHttpBinding senza sicurezza, è sufficiente usare codice come il frammento seguente (dichiarazione di variabile e creazione di heap ed errori vengono omessi). Si noti che nella chiamata alla funzione [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) non è specificata alcuna proprietà del canale o descrizione della sicurezza.


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



La funzione crea il proxy del servizio e restituisce un puntatore al proxy nel parametro *serviceProxy* (&proxy nella chiamata di funzione precedente).

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a>Creazione di un proxy del servizio per BasicHttpBinding di WCF

Quando si crea manualmente un proxy del servizio per un servizio WCF che utilizza un'associazione BasicHttpBinding, tuttavia, è necessario impostare la versione SOAP e WS-Addressing proprietà del canale. Ciò è dovuto al fatto che per impostazione predefinita WWSAPI è SOAP versione 1.2 e WS-Addressing 1.0. BasicHttpBinding di WCF, d'altra parte, usa SOAP versione 1.1 e nessun WS-Addressing.

Per impostare la versione SOAP e WS-Addrssing proprietà del canale, dichiarare una matrice di strutture [**\_ \_ WS CHANNEL PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) per contenere le proprietà del canale e le informazioni correlate.


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



Passare quindi la matrice di proprietà del canale (channelProperties) e il conteggio delle proprietà (channelPropertyCount) a [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (o [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) se si lavora a livello di canale).


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



La matrice dichiarata per contenere le proprietà viene copiata in **WsCreateServiceProxy** e, di conseguenza, è possibile liberare la memoria per la matrice di proprietà immediatamente dopo aver chiamato la funzione . Inoltre, se si alloca la memoria dallo stack (come il frammento di codice precedente), è anche possibile restituire dalla funzione immediatamente dopo la chiamata.

## <a name="other-bindings"></a>Altre associazioni

INOLTRE, WWSAPI fornisce meccanismi per la creazione di proxy del servizio per comunicare con i servizi WCF usando altre associazioni, ad esempio NetTcpBinding e WSFederationHttpBinding. Molte di queste associazioni richiedono l'impostazione di proprietà del canale aggiuntive, ad esempio descrittori di sicurezza. Per esempi che illustrano l'uso di altre associazioni, vedere la sezione Windows Web Services Examples , in particolare le sottosezioni [Tcp Channel Layer](tcp-channel-layer-examples.md) [Examples](windows-web-services-examples.md), HTTP Channel [Layer Examples](http-channel-layer-examples.md)e Security Channel Layer [Examples.](security-channel-layer-examples.md)

 

 




