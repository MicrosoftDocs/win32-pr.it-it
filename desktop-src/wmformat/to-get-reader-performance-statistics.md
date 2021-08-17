---
title: Per ottenere statistiche sulle prestazioni del lettore
description: Per ottenere statistiche sulle prestazioni del lettore
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- Advanced Systems Format (ASF), statistiche sulle prestazioni del lettore
- ASF (Advanced Systems Format), statistiche sulle prestazioni del lettore
- Advanced Systems Format (ASF), lettori asincroni
- ASF (Advanced Systems Format),lettori asincroni
- Advanced Systems Format (ASF), statistiche sulle prestazioni
- ASF (Advanced Systems Format), statistiche sulle prestazioni
- lettori asincroni, statistiche sulle prestazioni
- prestazioni, statistiche lettore
- prestazioni, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2397e575d67a699c4f211d872b53632e728fc2240b396d7475c8bb6b243fe445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084263"
---
# <a name="to-get-reader-performance-statistics"></a>Per ottenere statistiche sulle prestazioni del lettore

Quando si leggono i file in locale con il lettore asincrono, non è necessario controllare le prestazioni delle operazioni di lettura. Se tuttavia l'applicazione legge da un'origine di streaming, le statistiche sulle prestazioni possono essere molto importanti. L'applicazione può rispondere alle variazioni delle prestazioni di riproduzione per garantire la migliore esperienza possibile per l'utente finale.

Le informazioni sulle prestazioni che è possibile recuperare dal lettore includono le statistiche seguenti:

-   Larghezza di banda corrente della connessione.
-   Numero di pacchetti ricevuti dal server.
-   Numero di pacchetti persi recuperati.
-   Numero di pacchetti persi che non sono stati recuperati.
-   Percentuale del numero totale di pacchetti inviati ricevuti.

Per ottenere le statistiche sulle prestazioni del lettore, seguire questa procedura.

1.  Prima di avviare la riproduzione, creare una [**struttura WM \_ READER \_ STATISTICS.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) È necessario impostare il **membro cbSize** su sizeof(WM \_ READER \_ STATISTICS).
2.  Ottenere un puntatore [**all'interfaccia IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) dell'oggetto reader chiamando **IWMReader::QueryInterface.**
3.  Durante la riproduzione, effettuare spesso chiamate a [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) per monitorare le prestazioni. Passare la **struttura WM \_ READER \_ STATISTICS** con ogni chiamata ed esaminare i membri appropriati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




