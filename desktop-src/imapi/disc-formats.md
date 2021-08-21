---
title: Formati del disco
description: IMAPI supporta tre file system formati ISO 9660, Joliet e UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af71733ec2747ae227ac412a7b49f0faa73639cf1000f1332db5ec1d1d55db9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758604"
---
# <a name="disc-formats"></a>Formati del disco

IMAPI supporta tre file system formati: [ISO 9660,](#iso-9660) [Joliet](#joliet)e [UDF.](#universal-disk-format-udf)

## <a name="iso-9660"></a>ISO 9660

Il formato ISO 9660 è il formato standard file system dischi dati CD. Il formato viene riconosciuto in diversi sistemi operativi, tra cui MSDOS, Mac OS, UNIX e Windows sistema operativo. Il formato ISO 9660 è pubblicato da International Organization for Standardization (ISO).

Il formato inizia al settore 16 con l'intestazione del volume CD0001; segue il resto dell'intestazione. Anche altri formati derivati iniziano dal settore 16, ma usano un'altra stringa per l'intestazione del volume. Ad esempio, i dischi High Sierra usano la stringa CD-ROM0001 e il formato Compact Disc Interactive usa CD-I0001.

L'intestazione punta alle aree del disco che archiviano i nomi di file in formato ISO 9660. La convenzione di denominazione di file e directory è costituita da 8 caratteri, un punto e altri 3 caratteri. Si tratta della stessa convenzione di denominazione usata dal sistema operativo MSDOS.

Altre file system, per formati come Joliet e UDF, possono coesistere su un disco senza influire sulla leggibilità del formato ISO 9660. Dopo gli indici, un set di file di dati occupa il disco. Gli indici per ogni file system fanno riferimento in modo indipendente ai file di dati sul disco.

La specifica ISO 9660 definisce tre livelli di formato:

-   Il livello 1 definisce i nomi di file per l'uso del formato carattere 8.3.
-   Il livello 2 consente nomi di file più lunghi, come si può trovare nelle piattaforme DOS 6.xx, MacIntosh e UNIX.
-   Il livello 3 consente ai file audio e ai dati interleaved di migliorare le prestazioni di recupero (riproduzione). Questo livello rimuove anche il limite di 2 GB di file. Questo livello non **è supportato** dall'API Image Mastering.

I dischi DVD possono anche usare ISO 9660; Tuttavia, la funzione definita dall'file system è la versione più file system usata con i supporti DVD.

## <a name="joliet"></a>Joliet

Il formato Joliet è un derivato di ISO 9660. Questo formato scrive l'indice file system Joliet nell'immagine del disco oltre all'indice file system ISO 9660.

L'indice Joliet offre i miglioramenti seguenti all'file system seguente:

-   Riconosce nomi di file lunghi fino a 32 caratteri.
-   Distingue tra lettere maiuscole e minuscole nei nomi di file.
-   Supporta i caratteri Unicode nel nome file.

L'intestazione del formato Joliet inizia dal settore 17 del disco.

Poiché il formato Joliet mantiene il file system ISO 9660 su un disco, viene mantenuta la compatibilità con i dispositivi conformi a ISO 9660.

## <a name="universal-disk-format-udf"></a>Universal Disk Format (UDF)

Il formato UDF (Universal Disk Format) è un file system più recente sviluppato per supporti ottici dalla Optical Archiviazione Technology Association (OSTA). La funzione definita dall'utente è un formato portabile riconosciuto da diversi sistemi operativi. La funzione definita dall'utente sostituisce ISO 9660 come nuovo standard, in particolare con supporti di lettura/scrittura.

Di seguito sono riportate le funzionalità della funzione definita dall'utente:

-   Supporta supporti di dimensioni massime di 2 TB.
-   Supporta supporti flash, dischi IOMEGA REV e dischi CD-MRW.
-   Archivia file di lunghezza inferiore a 2 KB nel blocco File Entry.
-   Supporta file fino a 2 TB con nomi file fino a 255 caratteri.
-   Supporta un set completo di attributi di file adatti a vari sistemi operativi.
-   Supporta un formato bridge in cui i formati ISO 9660, Joliet e UDF risiedono tutti sullo stesso disco. Viene usato nelle applicazioni video, ad esempio DVD-Video, DVD+VR e DVD-VR.
-   Supporta flussi denominati e file "in tempo reale".

 

 




