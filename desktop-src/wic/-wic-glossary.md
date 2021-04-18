---
description: Definisce i termini utilizzati in WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Glossario componenti Windows Imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314472"
---
# <a name="windows-imaging-component-glossary"></a>Glossario componenti Windows Imaging

## <a name="b"></a>B

<dl> <dt>

**profondità bit**
</dt> <dd>

Numero di valori dei colori che possono essere assegnati a un singolo pixel in un'immagine. La profondità del colore può variare da 1 bit (nero e bianco) a 32 bit (oltre 16,7 milioni colori). Vedere anche: profondità colore

</dd> <dt>

**bit per pixel (BPP)**
</dt> <dd>

Numero di bit che rappresentano il valore del colore di ogni pixel in un'immagine digitalizzata. Vedere anche: BPP

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Clipper**
</dt> <dd>

Oggetto IWICBitmapClipper.

</dd> <dt>

**codec**
</dt> <dd>

Un filtro che comprime (codifica) o decomprime (Decodifica) un flusso di dati.

</dd> <dt>

**contesto colori**
</dt> <dd>

Astrazione per un profilo colori. Il profilo può essere caricato da un file (ad esempio, "sRGB Color Space Profile. ICM") o da un buffer di memoria ottenuto leggendo. Le informazioni sul contesto dei colori sono definite dall'interfaccia IWICColorContext per WIC e vengono recuperate con il metodo GetColorContext.

</dd> <dt>

**trasformazione colore**
</dt> <dd>

Mapping dei colori dal contesto del colore di origine al contesto del colore di destinazione in un formato pixel di output specificato.

</dd> <dt>

**Modello colori CYMK**
</dt> <dd>

Spazio dei colori multidimensionali costituito dalle intensità cyan, magenta, Yellow e Black che compongono un determinato colore.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**decodificatore**
</dt> <dd>

Vedere: codec

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Encoder**
</dt> <dd>

Vedere: codec

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**Lossless**
</dt> <dd>

Tipo di compressione che garantisce che i dati originali possano essere recuperati esattamente, senza perdita di qualità dell'immagine.

</dd> <dt>

**con perdita**
</dt> <dd>

Processo per la compressione dei dati in cui le informazioni ritenute non necessarie vengono rimosse e non possono essere recuperate durante la decompressione. Usato in genere con dati audio e visivi in cui è accettabile una lieve riduzione della qualità.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**Apartment a thread multipli (MTA)**
</dt> <dd>

Forma di multithreading supportata da Component Object Model (COM). In un modello di Apartment a thread multipli tutti i thread del processo che sono stati inizializzati come a thread libero si trovano in un unico Apartment.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**formato pixel nativo**
</dt> <dd>

Uno dei formati pixel forniti da WIC, in cui viene descritto il layout della memoria di ogni pixel in una bitmap.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**tavolozza**
</dt> <dd>

Set di colori utilizzati da un oggetto o da un'applicazione.

</dd> <dt>

**criteri per i metadati delle foto**
</dt> <dd>

Criteri di Windows per la lettura, la scrittura e la rimozione dei metadati delle immagini.

</dd> <dt>

**formato a pixel**
</dt> <dd>

Dimensioni e disposizione dei componenti colore pixel in memoria. Viene specificato in base al numero totale di bit utilizzati per pixel e al numero di bit utilizzati per archiviare i componenti rosso, verde, blu e alfa del colore. Ad esempio, il formato pixel RGB24 utilizza 24 bit per archiviare un colore pixel, con otto bit ciascuno per rosso, verde e blu. Il formato pixel ARGB32 utilizza 32 bit, con 24 bit di informazioni sui colori e 8 bit di informazioni sul canale alfa.

</dd> <dt>

**decodifica progressiva**
</dt> <dd>

Processo per la decodifica delle immagini codificate con informazioni sui diversi livelli di decodifica.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**flusso**
</dt> <dd>

Si riferisce a un'interfaccia COM IStream che può essere usata per leggere o scrivere in sequenza i dati in file, memoria o percorsi di rete.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**curva tono**
</dt> <dd>

Grafico utilizzato nella fotografia digitale che Visualizza l'intervallo tonale dell'immagine.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Windows Imaging Component (WIC)**
</dt> <dd>

Piattaforma estendibile che fornisce un'API di basso livello per le immagini digitali.

</dd> </dl>

 

 



