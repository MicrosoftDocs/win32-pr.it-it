---
description: Descrive le statistiche che è possibile recuperare da un codec Windows media.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Recupero delle statistiche di codifica (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa718a27894ea3e91faa953cb7b23e6c92b57c93d4b0fc0cf2c15b6995f28b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449161"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a>Recupero delle statistiche di codifica (Microsoft Media Foundation)

Le informazioni su ciò che accade in una sessione di codifica sono in genere immediatamente disponibili sotto forma di codici di errore restituiti durante l'elaborazione dei campioni. Tuttavia, esistono alcune statistiche che è possibile recuperare dal codec sui vari aspetti della codifica.

## <a name="video-frame-information"></a>Informazioni sui fotogrammi video

Alcune statistiche video che è possibile recuperare si occupano del numero di fotogrammi elaborati dal codificatore. Sono disponibili tre proprietà del numero di fotogramma che è possibile leggere dal codificatore video:

-   [MFPKEY \_ TOTALFRAMES è](mfpkey-totalframesproperty.md) il numero di frame elaborati tramite il flusso di input del DMO.
-   [MFPKEY \_ CODEDFRAMES è](mfpkey-codedframesproperty.md) il numero di frame codificati. Sottraendo questo valore dal numero totale di frame passati, è possibile determinare il numero di fotogrammi eliminati.
-   [MFPKEY \_ ZEROBYTEFRAMES è](mfpkey-zerobyteframesproperty.md) il numero di frame non codificati perché il contenuto duplicato è già incluso. Questo valore non viene sottratto dal numero di frame codificati segnalati dal DMO.

È possibile leggere le proprietà dei fotogrammi video in qualsiasi momento durante la codifica. Ciò può essere utile per determinare se le impostazioni di codifica sono appropriate per il contenuto. Se esiste una grande differenza tra frame totali e frame codificati, il contenuto compresso potrebbe non soddisfare i requisiti di qualità. È possibile leggere i valori finali dopo aver completato la codifica.

## <a name="vbr-buffer-statistics"></a>Statistiche buffer VBR

A seconda della modalità di codifica usata, alcune o tutte le impostazioni del buffer possono essere determinate durante la codifica (ad esempio, la velocità in bit della qualità basata sulla codifica vbR non è nota fino a quando il contenuto non viene codificato). Esistono quattro proprietà del buffer VBR che è possibile ottenere usando il **metodo IPropertyBag::Read:**

-   [MFPKEY \_ RAVG](mfpkey-ravgproperty.md) è la velocità in bit media del contenuto VBR.
-   [MFPKEY \_ BAVG è](mfpkey-bavgproperty.md) la finestra del buffer per la velocità in bit media.
-   [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) è la velocità in bit massima del contenuto VBR.
-   [MFPKEY \_ BMAX è](mfpkey-bmaxproperty.md) la finestra di picco del buffer.

Dopo aver iniziato a elaborare gli esempi, è consigliabile non leggere alcuna proprietà VBR fino a quando non è stata completata la codifica del flusso. In questo caso, il codificatore interpreta la richiesta come un segnale che indica che la codifica è completa. L'esempio successivo che si elabora viene considerato come una nuova sessione di codifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



