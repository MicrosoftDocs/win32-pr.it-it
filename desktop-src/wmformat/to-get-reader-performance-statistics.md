---
title: Per ottenere le statistiche sulle prestazioni del lettore
description: Per ottenere le statistiche sulle prestazioni del lettore
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- ASF (Advanced Systems Format), statistiche sulle prestazioni del lettore
- ASF (formato avanzato dei sistemi), statistiche sulle prestazioni del lettore
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- ASF (Advanced Systems Format), statistiche sulle prestazioni
- ASF (formato avanzato dei sistemi), statistiche sulle prestazioni
- lettori asincroni, statistiche sulle prestazioni
- prestazioni, statistiche del lettore
- prestazioni, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858002"
---
# <a name="to-get-reader-performance-statistics"></a>Per ottenere le statistiche sulle prestazioni del lettore

Quando si leggono i file localmente con il lettore asincrono, non è necessario verificare le prestazioni delle operazioni di lettura. Se l'applicazione sta leggendo da un'origine di flusso, tuttavia, le statistiche sulle prestazioni possono essere molto importanti. L'applicazione può rispondere alle modifiche nelle prestazioni di riproduzione per garantire la migliore esperienza utente finale.

Le informazioni sulle prestazioni che è possibile recuperare dal Reader includono le statistiche seguenti:

-   Larghezza di banda corrente della connessione.
-   Numero di pacchetti ricevuti dal server.
-   Numero di pacchetti persi recuperati.
-   Numero di pacchetti persi che non sono stati recuperati.
-   Percentuale del numero totale di pacchetti inviati ricevuti.

Per ottenere le statistiche sulle prestazioni del lettore, seguire questa procedura.

1.  Prima di iniziare la riproduzione, creare una struttura di [**\_ \_ statistiche di WM Reader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) . È necessario impostare il membro **cbSize** su sizeof (statistiche di WM \_ Reader \_ ).
2.  Ottenere un puntatore all'interfaccia [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.
3.  Durante la riproduzione, eseguire le chiamate a [**IWMReaderAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) di frequente per monitorare le prestazioni. Passare la struttura delle **\_ \_ statistiche di WM Reader** a ogni chiamata ed esaminare i membri appropriati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




