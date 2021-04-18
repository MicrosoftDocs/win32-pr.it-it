---
description: Extended Linguistic Services (ELS) viene implementato come una libreria a collegamento dinamico (DLL) che fornisce un'ampia gamma di funzionalità di supporto linguistico per il testo specificato dall'applicazione.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: Informazioni sui servizi linguistici estesi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314312"
---
# <a name="about-extended-linguistic-services"></a>Informazioni sui servizi linguistici estesi

Extended Linguistic Services (ELS) viene implementato come una libreria a collegamento dinamico (DLL) che fornisce un'ampia gamma di funzionalità di supporto linguistico per il testo specificato dall'applicazione. La tecnologia include i plug-in e la piattaforma ELS per diversi tipi di servizi linguistici predefiniti accessibili all'applicazione tramite la piattaforma.

> [!Note]  
> Il modulo ELS viene installato automaticamente con Windows 7 e versioni successive.

 

## <a name="els-platform"></a>Piattaforma ELS

La piattaforma ELS è l'interfaccia tra l'applicazione e i servizi ELS. Offre un modo semplice per implementare diversi tipi di funzionalità linguistiche tramite la stessa API, che consente all'applicazione di accedere a servizi specifici e di utilizzarli. Per altre informazioni sull'API, vedere informazioni di [riferimento su servizi linguistici estesi.](extended-linguistic-services-reference.md)

> [!Note]  
> Quando l'applicazione chiama una delle funzioni dell'API ELS, la piattaforma alloca memoria e risorse in base alle esigenze per la comunicazione con i servizi. L'applicazione è responsabile della richiamata della piattaforma per liberare queste risorse.

 

La piattaforma viene eseguita all'interno dello spazio di memoria virtuale dell'applicazione e tutta la memoria allocata fa parte di questo spazio. Pertanto, l'applicazione deve solo collegarsi alla DLL del componente ELS (Elscore.dll) collegandosi a Elscore. lib o caricando in modo dinamico Elscore.dll.

## <a name="els-services"></a>Servizi ELS

Per Windows 7 e versioni successive, la piattaforma ELS supporta solo i servizi predefiniti seguenti.

-   [Rilevamento lingua Microsoft](microsoft-language-detection.md)
-   [Rilevamento script Microsoft](microsoft-script-detection.md)
-   [Servizi di traslitterazione](transliteration-services.md)

> [!Note]  
> Le versioni future di ELS supporteranno i servizi aggiuntivi forniti da Microsoft o dai provider di servizi.

 

Ogni servizio è associato a una categoria di servizi che descrive le operazioni del servizio. La categoria è rappresentata da una stringa non localizzabile. Viene utilizzato dalle applicazioni per enumerare i servizi disponibili. Le categorie di servizi correnti sono:

-   "Rilevamento lingua"
-   "Rilevamento script"
-   Translitterazione

La piattaforma usa i metadati del servizio per enumerare i servizi richiesti dall'applicazione. Proprietà quali l'identificatore univoco globale (GUID) del servizio, i linguaggi e gli script di input e output supportati e la categoria del servizio possono essere usati dall'applicazione per enumerare i servizi ELS desiderati.

Ogni servizio ELS viene implementato come plug-in supportato da una DLL che può essere installata nel sistema operativo in modo che la piattaforma ELS possa rilevare e usarla. I servizi possono esporre i propri sottoservizi, se necessario.

## <a name="main-els-operations"></a>Operazioni ELS principali

Questa sezione descrive le operazioni principali supportate dalla piattaforma ELS. La piattaforma supporta le modalità di chiamata sincrona e asincrona. La modalità di chiamata asincrona utilizza un pool di thread dell'applicazione per pianificare i thread per l'elaborazione delle richieste.

> [!Note]  
> Poiché la piattaforma supporta una modalità asincrona, i servizi ELS non devono implementare questo tipo di funzionalità autonomamente.

 

### <a name="service-enumeration"></a>Enumerazione del servizio

La piattaforma ELS carica e gestisce tutti i servizi ELS, rendendo trasparente l'operazione per l'applicazione. L'applicazione enumera i servizi disponibili chiamando [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices). Per istruzioni sulla programmazione, vedere [enumerazione e liberazione dei servizi](enumerating-and-freeing-services.md).

> [!Note]  
> Per motivi di prestazioni, è consigliabile che l'applicazione enumera i servizi disponibili una sola volta. La piattaforma ELS verifica nuovamente i servizi nell'enumerazione successiva per assicurarsi che i risultati dell'enumerazione siano sempre aggiornati.

 

### <a name="text-recognition"></a>Riconoscimento del testo

Dopo l'enumerazione del servizio, l'applicazione chiama la funzione [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) per usare un particolare servizio ELS per eseguire il mapping di qualsiasi intervallo di testo di testo di input al testo di output. Un esempio di riconoscimento del testo è l'uso di un servizio di rilevamento della lingua che riceve un segmento di testo e rileva il linguaggio più probabile.

Dopo che il servizio ha riconosciuto il testo, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) restituisce con una struttura del [**\_ \_ contenitore delle proprietà di mapping**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) popolata con le proprietà e i dati di output generati dal servizio. Per evitare perdite di memoria, l'applicazione deve liberare il contenitore delle proprietà chiamando [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) per ogni volta che [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) restituisce \_ OK. In genere l'applicazione esegue questa operazione quando viene completata utilizzando i dati di output o quando i dati di output non sono più rilevanti perché l'area di input del testo è stata modificata, ad esempio, modificata o eliminata. Quando viene rilasciato il contenitore delle proprietà, **MappingFreePropertyBag** restituisce.

Per la [richiesta di riconoscimento](requesting-text-recognition.md)del testo sono disponibili istruzioni di programmazione per il riconoscimento del testo.

### <a name="service-termination"></a>Terminazione del servizio

Quando l'applicazione non richiede più servizi ELS, chiama [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) prima di terminare. Per altre informazioni, vedere [enumerazione e liberazione dei servizi](enumerating-and-freeing-services.md).

### <a name="versioning"></a>Controllo delle versioni

Le versioni future di ELS consentiranno l'aggiornamento dei servizi ELS. L'applicazione sarà in grado di controllare i numeri di versione della struttura di [**\_ \_ informazioni sul servizio di mapping**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) per rilevare eventuali modifiche nei servizi.

> [!Note]  
> L'applicazione ELS non deve supporre che diverse versioni dello stesso servizio possano recuperare esattamente gli stessi risultati.

 

 

 



