---
title: Formati di disco
description: IMAPi supporta tre formati file system ISO 9660, Joliet e UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330087"
---
# <a name="disc-formats"></a>Formati di disco

IMAPi supporta tre formati di file system: [ISO 9660](#iso-9660), [Joliet](#joliet)e [UDF](#universal-disk-format-udf).

## <a name="iso-9660"></a>ISO 9660

Il formato ISO 9660 è il file system standard originale per i dischi di dati CD. Il formato è riconosciuto su diversi sistemi operativi, tra cui MSDOS, il Mac OS, UNIX e il sistema operativo Windows. Il formato ISO 9660 è pubblicato dal organizzazione internazionale per la standardizzazione (ISO).

Il formato inizia in corrispondenza del settore 16 con l'intestazione del volume, CD0001; il resto dell'intestazione segue. Anche altri formati derivati iniziano nel settore 16, ma usano un'altra stringa per l'intestazione del volume. Ad esempio, i dischi High Sierra usano la stringa CD-ROM0001 e Compact Disc Interactive Format USA CD-I0001.

L'intestazione punta alle aree del disco in cui sono archiviati i nomi dei file in formato ISO 9660. La convenzione di denominazione di file e directory è costituita da 8 caratteri, un punto e altri 3 caratteri. Si tratta della stessa convenzione di denominazione utilizzata dal sistema operativo MSDOS.

Intestazioni file system aggiuntive, per formati come Joliet e UDF, possono coesistere in un disco senza influire sulla leggibilità del formato ISO 9660. Dopo gli indici, un set di file di dati occupa il disco. Gli indici per ogni file system i file di dati di riferimento in modo indipendente nel disco.

La specifica ISO 9660 definisce tre livelli del formato:

-   Il livello 1 definisce i nomi di file per l'utilizzo del formato carattere 8,3.
-   Il livello 2 consente nomi di file più lunghi, come si trova nelle piattaforme DOS 6. XX, MacIntosh e UNIX.
-   Il livello 3 consente ai file di dati e audio con interfoliazione di migliorare le prestazioni di recupero (riproduzione). Questo livello consente inoltre di rimuovere il limite di file da 2 GB. Questo livello **non** è supportato dall'API per la creazione di immagini master.

I dischi DVD possono anche usare ISO 9660; Tuttavia, la file system UDF è la file system più prevalente utilizzata con supporti DVD.

## <a name="joliet"></a>Joliet

Il formato Joliet è un derivato di ISO 9660. Questo formato scrive l'indice Joliet file system nell'immagine del disco, oltre all'indice file system ISO 9660.

L'indice Joliet fornisce i miglioramenti seguenti all'indice file system:

-   Riconosce i nomi di file lunghi fino a 32 caratteri.
-   Distingue le lettere maiuscole e minuscole nei nomi dei file.
-   Supporta i caratteri Unicode nel nome file.

L'intestazione del formato Joliet inizia al settore 17 del disco.

Poiché il formato Joliet conserva la file system ISO 9660 su un disco, viene mantenuta la compatibilità con i dispositivi conformi a ISO 9660.

## <a name="universal-disk-format-udf"></a>Universal Disk Format (UDF)

Il formato UDF (Universal Disk Format) è un file system più recente sviluppato per supporti ottici da Optical Storage Technology Association (OSTA). UDF è un formato portatile riconosciuto da diversi sistemi operativi. La funzione UDF sostituisce ISO 9660 come nuovo standard, soprattutto con i supporti di lettura/scrittura.

Le funzionalità di UDF includono quanto segue:

-   Supporta supporti fino a 2 TB di dimensioni.
-   Supporta Flash Media, dischi Iomega REV e dischi CD-MRW.
-   Archivia i file di lunghezza inferiore a 2 KB nel blocco di immissione file.
-   Supporta file fino a 2 TB con nomi di file di lunghezza pari a 255 caratteri.
-   Supporta un set completo di attributi di file adatti a diversi sistemi operativi.
-   Supporta un formato Bridge in cui tutti i formati ISO 9660, Joliet e UDF si trovano nello stesso disco. Questa operazione viene usata nelle applicazioni video, ad esempio DVD-video, DVD + VR e DVD-VR.
-   Supporta i flussi denominati e i file in tempo reale.

 

 




