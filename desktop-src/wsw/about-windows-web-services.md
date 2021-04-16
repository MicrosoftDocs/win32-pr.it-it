---
title: Informazioni sui servizi Web Windows
description: L'API dei servizi Web Windows è un'API a più livelli e può essere illustrata come indicato di seguito.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104566429"
---
# <a name="about-windows-web-services"></a>Informazioni sui servizi Web Windows

L'API dei servizi Web Windows è un'API a più livelli e può essere illustrata come indicato di seguito

![Diagramma che mostra i livelli e le aree multilivello dell'API dei servizi Web Windows.](images/apistack.png)

WWSAPI è un'API a più livelli. Si prevede che la maggior parte degli sviluppatori sia destinata al modello del servizio, ovvero un modello di programmazione basato su metodo. Nel modello del servizio, l'host del servizio fornisce il modello di programmazione lato server, mentre il proxy del servizio fornisce il modello di programmazione lato client.

Ogni livello espone un set di API e tipi che possono essere usati con le API di tale livello.

## <a name="service-model"></a>Modello del servizio

Il livello di livello superiore denominato [modello di servizio](service-model-layer-overview.md) fornisce un modello di programmazione basato sul metodo ed è il modello più semplice da usare. Nel modello del servizio, l' [host del servizio](service-host.md) fornisce il modello di programmazione lato server, mentre il [proxy del servizio](service-proxy.md) fornisce il modello di programmazione lato client. Il [contesto](context.md) viene utilizzato all'interno del modello del servizio per passare uno stato pertinente disponibile all'operazione del servizio e/o al callback quando viene richiamato. Il [contratto di servizio](contract.md) e viene usato per specificare un contratto di servizio in un endpoint esposto nel servizio. I componenti e le operazioni seguenti fanno parte del livello di servizio:

-   [Host del servizio](service-host.md)
-   [Proxy servizio](service-proxy.md)
-   [Contesto](context.md)
-   [Contratto](contract.md)
-   [Metadati del servizio](service-metadata.md)

## <a name="channel-layer"></a>Livello del canale

Il modello di servizio si basa su un livello del canale, che offre la massima flessibilità, ma è più difficile da usare. I componenti e le operazioni seguenti fanno parte del livello del canale:

-   [Messaggio](message.md)
-   [Channel](channel.md)
-   [Listener](listener.md)
-   [Errori](faults.md)
-   [Url](url.md)
-   [Sicurezza](security-overview.md)
-   [Importazione di metadati](metadata-import.md)

## <a name="xml-layer"></a>Livello XML

Il livello del canale si basa a sua volta su un Framework XML leggero, che include la deserializzazione dei tipi di dati C. I componenti e le operazioni seguenti fanno parte del livello XML:

-   [Writer XML](xml-writer.md)
-   [Lettore XML](xml-reader.md)
-   [Buffer XML](xml-buffer.md)
-   [Serializzazione](serialization.md)
-   [Supporto del linguaggio XML](xml-language-support.md)

## <a name="common-to-all-layers"></a>Comune a tutti i livelli

Di seguito sono riportati gli argomenti che si applicano a uno dei tre livelli:

-   [Errori](errors.md)
-   [Modello asincrono](asynchronous-model.md)
-   [Thread safety](thread-safety.md)
-   [Traccia](tracing.md)
-   [Annullamento](cancellation.md)
-   [Utilità](utilities.md)
-   [Debug](debugging.md)
-   [Strumento compilatore wsutil](wsutil-compiler-tool.md)
-   [Heap](heap.md)

## <a name="examples"></a>Esempio

Per ulteriori informazioni sugli elementi API, vedere [riferimenti per servizi Web Windows](windows-web-services-reference.md). Per esempi relativi all'uso dell'API, vedere [uso di servizi Web Windows](using-windows-web-services.md).

 

 




