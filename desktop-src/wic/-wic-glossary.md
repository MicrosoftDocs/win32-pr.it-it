---
description: Definisce i termini usati in WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Windows Glossario dei componenti di creazione dell'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c851b4a0be5d5f90a5ff0cc030d68cc1010a0259c316811a7ca1c3b92c383b7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668192"
---
# <a name="windows-imaging-component-glossary"></a>Windows Glossario dei componenti di creazione dell'immagine

## <a name="b"></a>B

<dl> <dt>

**profondità in bit**
</dt> <dd>

Numero di valori di colore che possono essere assegnati a un singolo pixel in un'immagine. La profondità del colore può variare da 1 bit (bianco e nero) a 32 bit (oltre 16,7 milioni di colori). Vedere anche: Profondità colore

</dd> <dt>

**bit per pixel (bpp)**
</dt> <dd>

Numero di bit che rappresentano il valore del colore di ogni pixel in un'immagine digitalizzata. Vedere anche:BPP

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Clipper**
</dt> <dd>

Oggetto IWICBitmapClipper.

</dd> <dt>

**Codec**
</dt> <dd>

Filtro che comprime (codifica) o decomprime (decodifica) un flusso di dati.

</dd> <dt>

**contesto dei colori**
</dt> <dd>

Astrazione per un profilo colori. Il profilo può essere caricato da un file (ad esempio. "sRGB Color Space Profile.icm") o da un buffer di memoria ottenuto tramite la lettura. Le informazioni sul contesto del colore sono definite dall'interfaccia IWICColorContext per WIC e vengono recuperate con il metodo GetColorContext.

</dd> <dt>

**trasformazione dei colori**
</dt> <dd>

Mapping dei colori dal contesto del colore di origine al contesto del colore di destinazione in un formato pixel di output specificato.

</dd> <dt>

**Modello a colori CYMK**
</dt> <dd>

Spazio colori multidimensionale costituito dalle intensità ciano, magenta, giallo e nero che costituiscono un determinato colore.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Decoder**
</dt> <dd>

Vedere Altro termine: codec

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Encoder**
</dt> <dd>

Vedere Altro termine: codec

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**Lossless**
</dt> <dd>

Tipo di compressione che garantisce che i dati originali possano essere recuperati esattamente, senza perdita di qualità dell'immagine.

</dd> <dt>

**Lossy**
</dt> <dd>

Processo di compressione dei dati in cui le informazioni ritenute non necessarie vengono rimosse e non possono essere recuperate in caso di decompressione. Usato in genere con dati audio e visivi in cui è accettabile una lieve riduzione della qualità.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**apartment multithreading (MTA)**
</dt> <dd>

Forma di multithreading supportata da Component Object Model (COM). In un modello di apartment multithreading tutti i thread del processo inizializzati come a thread libero risiedono in un singolo apartment.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**formato pixel nativo**
</dt> <dd>

Uno dei formati pixel forniti da WIC, in cui viene descritto il layout di memoria di ogni pixel in una bitmap.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**Tavolozza**
</dt> <dd>

Set di colori utilizzati da un oggetto o un'applicazione.

</dd> <dt>

**criteri dei metadati delle foto**
</dt> <dd>

Criteri di Windows per la lettura, la scrittura e la rimozione dei metadati dell'immagine.

</dd> <dt>

**formato a pixel**
</dt> <dd>

Dimensioni e disposizione dei componenti di colore pixel in memoria. Viene specificato dal numero totale di bit usati per pixel e dal numero di bit usati per archiviare i componenti rosso, verde, blu e alfa del colore. Ad esempio, il formato pixel RGB24 usa 24 bit per archiviare un colore pixel, con otto bit ciascuno per rosso, verde e blu. Il formato pixel ARGB32 usa 32 bit, con 24 bit di informazioni sul colore e 8 bit di informazioni sul canale alfa.

</dd> <dt>

**decodifica progressiva**
</dt> <dd>

Processo di decodifica delle immagini codificate con informazioni sui diversi livelli di decodifica.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Flusso**
</dt> <dd>

Fa riferimento a un'interfaccia COM IStream che può essere usata per leggere o scrivere dati in sequenza in file, memoria o percorsi di rete.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**curva tono**
</dt> <dd>

Grafico usato nella fotografia digitale che visualizza l'intervallo tonale dell'immagine.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Windows Imaging Component (WIC)**
</dt> <dd>

Una piattaforma estendibile che fornisce API di basso livello per le immagini digitali.

</dd> </dl>

 

 



