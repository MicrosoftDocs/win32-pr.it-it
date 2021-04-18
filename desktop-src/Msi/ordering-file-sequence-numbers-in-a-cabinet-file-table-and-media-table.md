---
description: La tabella file contiene un elenco completo di tutti i file di origine per l'installazione.
ms.assetid: 481fdc45-82db-4128-93de-388562f636e9
title: Ordinamento dei numeri di sequenza di file in un file CAB, una tabella file e una tabella multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07f9cd530d90fb0ef4d805b8ff2c96398cd97e55
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320793"
---
# <a name="ordering-file-sequence-numbers-in-a-cabinet-file-table-and-media-table"></a>Ordinamento dei numeri di sequenza di file in un file CAB, una tabella file e una tabella multimediale

La [tabella file](file-table.md) contiene un elenco completo di tutti i file di origine per l'installazione. I file possono essere archiviati nel supporto di origine come singoli file o compressi all'interno di [file CAB](cabinet-files.md). I numeri di sequenza nella colonna sequenza della tabella file, insieme al campo LastSequence della [tabella media](media-table.md), specificano sia l'ordine di installazione per i file che i supporti di origine in cui si trova ogni file. Ogni record della tabella media identifica il disco di origine contenente tutti i file con numeri di sequenza minori o uguali al valore indicato nella colonna LastSequence e maggiore del valore LastSequence del disco precedente.

Si supponga, ad esempio, che un file disponga di un numero di sequenza di 92 immesso nella colonna sequenza della tabella file. Per determinare in quale disco di origine si trova il file, il programma di installazione controlla il record della tabella dei supporti per la voce con il valore LastSequence più piccolo maggiore di 92. La colonna DiskID è la chiave primaria per la tabella dei supporti e questo campo identifica in modo univoco il disco nella tabella.

Il limite massimo per il numero di file che possono essere elencati nella tabella file di un pacchetto di Windows Installer è 32767 file. Per creare un pacchetto di Windows Installer contenente più file, vedere la pagina relativa alla [creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md).

Gli autori di pacchetti possono ridurre le dimensioni dei pacchetti di installazione comprimendo i file di origine e inserendoli nei file CAB. L'immagine del file di origine può essere compressa, non compressa o una combinazione di entrambi i tipi. Per ulteriori informazioni sulle origini compresse e non compresse, vedere [origini compresse e non compresse](compressed-and-uncompressed-sources.md). I file di origine compressi devono essere archiviati all'interno di un file CAB. I file compressi all'interno di un file CAB hanno i rispettivi numeri di sequenza interni. I valori dei numeri di sequenza interni non devono necessariamente corrispondere al valore dei numeri di sequenza nella tabella file. La sequenza dei file specificati nella tabella file, tuttavia, deve essere identica alla sequenza effettiva dei file all'interno dei file CAB. I numeri di sequenza dei file non compressi non devono essere univoci. Se, ad esempio, tutti i file sono decompressi e si trovano in un disco, tutti i file possono avere lo stesso numero di sequenza nella tabella file.

La tabella media descrive il set di dischi che costituiscono il supporto di origine per l'installazione. La prima voce nella tabella media deve avere sempre un valore 1 nel campo DiskID. I file devono essere organizzati nel supporto di origine in modo che tutti i file su disco 1 dispongano di numeri di sequenza della tabella file di dimensioni inferiori ai numeri di sequenza dei file sul disco 2 e tutti i numeri di sequenza sul disco 2 dovrebbero essere più piccoli rispetto al disco 3 e così via. Questo requisito si applica anche a un disco che contiene origini compresse e non compresse. Se, ad esempio, le origini supporti per l'installazione si trovano in due dischi di origine e se il disco 1 contiene sia file non compressi sia un file CAB, entrambi i file non compressi e i file nel file CAB devono avere numeri di sequenza inferiori al numero di sequenza di file più piccolo di qualsiasi file archiviato sul disco 2. Se tutti i file sul disco 1 sono compressi in un file CAB, è possibile creare la tabella dei supporti come illustrato nella tabella seguente.

[Tabella media](media-table.md) (parziale)



| DiskId | LastSequence | DiskPrompt | CAB   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          | mycab.cab | Disco 1      |
| 2      | 10           | 2          |           | Disco 2      |



 

Se alcuni file su disco 1 sono compressi in un file CAB e alcuni sono decompressi, è possibile creare la tabella media come indicato di seguito.

[Tabella media](media-table.md) (parziale)



| DiskId | LastSequence | DiskPrompt | CAB   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disco 1      |
| 2      | 10           | 1          | mycab.cab | Disco 1      |
| 3      | 15           | 2          |           | Disco 2      |



 

Si noti che la creazione nella tabella multimediale seguente non è corretta perché specifica alcuni numeri di sequenza del file su disco 2 di dimensioni inferiori rispetto ad alcuni file nel disco 1.

[Tabella supporti](media-table.md)



| DiskId | LastSequence | DiskPrompt | CAB   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disco 1      |
| 2      | 10           | 2          |           | Disco 2      |
| 3      | 15           | 1          | mycab.cab | Disco 1      |



 

I file di grandi dimensioni possono essere suddivisi tra due o più file CAB. Non possono essere presenti più di 15 file in un file CAB che si estende al file CAB successivo. Se, ad esempio, si dispone di tre file CAB, il primo file CAB può includere 15 file che si estendono al secondo file CAB e il secondo file CAB può includere 15 file che si estendono al terzo file CAB. Quando si aggiunge un record alla tabella file per un file su più file CAB, utilizzare la prima parte del file per specificare il numero di sequenza del file immesso nella colonna sequenza.

Le tabelle file e supporti potrebbero essere create come indicato di seguito se sono presenti tre file, due armadi e due dischi. In questo esempio c1.cab si trova in disk1 e c2.cab risiede in disk2. Il file F2 si estende su entrambi i cabinet. Il cabinet c1.cab contiene l'intero file F1 e la prima parte del file F2. Il cabinet c2.cab contiene la seconda parte di F2 e l'intero file F3.

[Tabella media](media-table.md) (parziale)



| DiskId | LastSequence | DiskPrompt | CAB | VolumeLabel |
|--------|--------------|------------|---------|-------------|
| 1      | 5            | 1          | c1.cab  | Disco 1      |
| 2      | 10           | 2          | c2.cab  | Disco 2      |



 

[Tabella file](file-table.md) (parziale)



| File | Sequenza |
|------|----------|
| F1   | 1        |
| F2   | 2        |
| F3   | 6        |



 

 

 



