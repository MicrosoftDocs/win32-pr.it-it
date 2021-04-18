---
description: Accesso alle proprietà dell'oggetto servizio
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Accesso alle proprietà dell'oggetto servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306656"
---
# <a name="accessing-service-object-properties"></a>Accesso alle proprietà dell'oggetto servizio

Un'applicazione può leggere e scrivere proprietà per un singolo oggetto in un servizio, per più oggetti identificati da identificatori di oggetto o per più oggetti dello stesso tipo. Nell'argomento [recupero delle proprietà dell'oggetto](retrieving-content-object-properties.md) vengono descritte le proprietà di lettura per un singolo oggetto in un servizio. Nell'argomento [scrittura delle proprietà dell'oggetto](writing-content-object-properties.md) viene descritta la scrittura delle proprietà per un singolo oggetto in un servizio.

Per una descrizione del recupero delle proprietà per più oggetti, vedere la sezione [attività avanzate](advanced-tasks.md) .

## <a name="when-to-use-service-property-definitions"></a>Quando utilizzare le definizioni delle proprietà del servizio

Le chiamate all'API WPD usate per il recupero e l'impostazione delle proprietà degli oggetti per un servizio sono le stesse chiamate per recuperare le proprietà dell'oggetto per un dispositivo (per un esempio, confrontare "recupero delle proprietà per un singolo oggetto"). La differenza principale consiste nel fatto che per eseguire query sulle proprietà degli oggetti viene utilizzato un set diverso di PROPERTYKEYs. Per WpdServiceApiSample, vengono usati PROPERTYKEYs del servizio del dispositivo (ad esempio, **pkey \_ GenericObj \_ Name**); per i WpdApiSample, vengono usati WPD PROPERTYKEYs, ad esempio il **\_ \_ nome dell'oggetto WPD**.

Il servizio Device PROPERTYKEYs è definito in BridgeDeviceServices. h (incluso in ogni file di intestazione del servizio) e rappresenta il set comune di PROPERTYKEYS usato dalle applicazioni di servizi per dispositivi e dall'implementazione del firmware nel dispositivo. In questo modo è possibile ottenere un set coerente di definizioni in tutto lo stack del dispositivo con una conversione minima, raggruppare PROPERTYKEYs in base al servizio e consentire la definizione più semplice dei nuovi servizi senza dover aggiornare lo schema di WPD.

Il set di PROPERTYKEYs usato dipende dalle esigenze dell'applicazione:

-   Se l'applicazione sta comunicando con il dispositivo chiamando [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), usare il PROPERTYKEYs definito in portabledevice. h. Un esempio di tale applicazione è WpdApiSample.
-   Se l'applicazione sta comunicando con servizi dispositivo chiamando [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), usare il PROPERTYKEYS definito in BridgeDeviceServices. h. Un esempio di tale applicazione è WpdServicesApiSample.
-   Se si sta scrivendo un'applicazione complessa che deve supportare un ibrido di servizi per dispositivi e del dispositivo (ciò significa che l'applicazione chiama sia **IPortableDevice:: Open** che **IPortableDeviceService:: Open**), è necessario usare il PROPERTYKEYs WPD quando si usa IPortableDevice e le interfacce derivate e il servizio del dispositivo PROPERTYKEYs quando si usano [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) e le interfacce derivate.

La maggior parte delle applicazioni WPD deve rientrare nella prima o nella seconda categoria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[Recupero delle proprietà dell'oggetto](retrieving-content-object-properties.md)
</dt> <dt>

[Scrittura delle proprietà di un oggetto](writing-content-object-properties.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



