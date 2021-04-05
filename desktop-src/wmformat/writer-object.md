---
title: Oggetto writer
description: Oggetto writer
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- Windows Media Format SDK, oggetti writer
- ASF (Advanced Systems Format), oggetti writer
- ASF (Advanced Systems Format), oggetti writer
- oggetti, oggetti writer
- oggetti writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d4783a8330ac1f0f16bc2ca2de4e843cbacc06
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724124"
---
# <a name="writer-object"></a>Oggetto writer

L'oggetto writer viene utilizzato per scrivere file multimediali digitali utilizzando la struttura di file ASF (Advanced Systems Format). Il processo di scrittura di un file multimediale digitale comporta molti passaggi interni al writer, che coordina la compressione, la creazione di pacchetti e il multiplexing.

L'oggetto writer include interfacce per l'output su file o una rete, supporta un'interfaccia di callback e può creare uno o più oggetti proprietà supporti di input.

L'oggetto writer viene creato dalla funzione [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), che imposta un puntatore a un'interfaccia **IWMWriter** . Le altre interfacce dell'oggetto writer possono essere ottenute chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate dall'oggetto writer.



| Interfaccia                                          | Descrizione                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | Fornisce metodi per generare chiavi [*DRM*](wmformat-glossary.md) .                                                                                                |
| [**IWMDRMWriter2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | Configura l'oggetto writer per la scrittura di un file contenente un flusso pre-crittografato conforme al protocollo Windows Media DRM 10 per i dispositivi di rete.                                                    |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | Gestisce la specifica e il recupero delle informazioni di intestazione, ad esempio metadati, [*marcatori*](wmformat-glossary.md)e così via.                                                           |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | Gestisce l'enumerazione tramite le informazioni sui codec disponibili. Eredita tutti i metodi di **IWMHeaderInfo**.                                                                                            |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | Gestisce l'enumerazione tramite le informazioni sui codec disponibili. Eredita tutti i metodi di **IWMHeaderInfo** e **IWMHeaderInfo2**.                                                                     |
| [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | Consente di accedere alle informazioni sui sistemi di filigrana presenti nel sistema.                                                                                                                          |
| [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | Avvia e arresta la scrittura dei file ASF; sono inclusi i metodi per l'allocazione di buffer, l'impostazione e il recupero di proprietà di input, l'impostazione di profili e i nomi dei file di output e lo sblocco del writer.         |
| [**IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | Aggiunge, ottiene e rimuove gli oggetti sink specificati; Recupera le statistiche, il numero di sink e l'ora di clock a cui il writer sta lavorando; ed esegue altre funzioni avanzate.                                |
| [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | Fornisce alcune funzionalità avanzate, in particolare per la gestione di video deinterlacciati. Eredita tutti i metodi di **IWMWriterAdvanced**.                                                                 |
| [**IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | Fornisce funzionalità aggiuntive del writer, inclusa la possibilità di ottenere statistiche dettagliate del writer. Eredita tutti i metodi di **IWMWriterAdvanced** e **IWMWriterAdvanced2**.                       |
| [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | Gestisce alcune funzionalità di scrittura avanzate relative agli esempi di visualizzazione. Per verificare che il processo di codifica/decodifica funzioni correttamente, è possibile visualizzare l'output, in genere da un codificatore. |
| [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | Gestisce i passaggi di pre-elaborazione effettuati dal writer. I passaggi di pre-elaborazione vengono usati per migliorare la qualità dell'output codificato.                                                                                  |



 

L'interfaccia di callback seguente deve essere implementata dall'applicazione per tenere traccia dello stato di avanzamento della visualizzazione.



| Interfaccia                                                      | Descrizione                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | Consente di gestire il modo in cui vengono ricevuti gli esempi non compressi dall'oggetto writer per visualizzare in anteprima le attività del codec. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




