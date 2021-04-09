---
description: Descrive le statistiche che è possibile recuperare da un codec Windows Media.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Recupero delle statistiche di codifica (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749218"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a>Recupero delle statistiche di codifica (Microsoft Media Foundation)

Le informazioni su ciò che accade in una sessione di codifica sono in genere immediatamente disponibili sotto forma di codici di errore restituiti durante l'elaborazione degli esempi. Tuttavia, esistono alcune statistiche che è possibile recuperare dal codec sui vari aspetti della codifica.

## <a name="video-frame-information"></a>Informazioni sul frame video

Alcune statistiche video che è possibile recuperare riguardano il numero di frame elaborati dal codificatore. Sono disponibili tre proprietà del numero di frame che è possibile leggere dal codificatore video:

-   [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) è il numero di frame elaborati tramite il flusso di input di DMO.
-   [MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md) è il numero di frame codificati. Sottraendo questo valore dal numero totale di frame passati, è possibile determinare il numero di frame eliminati.
-   [MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) è il numero di frame non codificati perché sono già stati inclusi contenuti duplicati. Questo valore non viene sottratto dal numero di fotogrammi codificati restituiti da DMO.

È possibile leggere le proprietà del fotogramma video in qualsiasi momento durante la codifica. Questo può essere utile per determinare se le impostazioni di codifica sono appropriate per il contenuto. Se c'è una grande differenza tra i frame totali e i frame codificati, il contenuto compresso potrebbe non soddisfare i requisiti di qualità. È possibile leggere i valori finali dopo aver completato la codifica.

## <a name="vbr-buffer-statistics"></a>Statistiche buffer VBR

A seconda della modalità di codifica utilizzata, alcune o tutte le impostazioni del buffer possono essere determinate durante la codifica (ad esempio, la velocità in bit di VBR basata sulla qualità non è nota fino a quando non viene codificato il contenuto). Sono disponibili quattro proprietà del buffer VBR che è possibile ottenere usando il metodo **IPropertyBag:: Read** :

-   [MFPKEY \_ RAVG](mfpkey-ravgproperty.md) è la velocità in bit media del contenuto VBR.
-   [MFPKEY \_ BAVG](mfpkey-bavgproperty.md) è la finestra del buffer per la velocità in bit media.
-   [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) è la velocità in bit massima del contenuto VBR.
-   [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) è la finestra del buffer di picco.

Dopo aver iniziato l'elaborazione degli esempi, è consigliabile non leggere alcuna proprietà VBR fino a quando non si termina la codifica del flusso. In tal caso, il codificatore interpreta la richiesta come segnale del completamento della codifica. Il seguente esempio elaborato viene considerato come una nuova sessione di codifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



