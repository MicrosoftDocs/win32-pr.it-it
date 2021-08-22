---
description: La tabella File contiene un elenco completo di tutti i file di origine per l'installazione.
ms.assetid: 481fdc45-82db-4128-93de-388562f636e9
title: Ordinamento dei numeri di sequenza dei file in un file CAB, una tabella file e una tabella multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f64558a570c7184da36feba8aeea6d2a7dc32c0d8add4c6963dece131c4849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327867"
---
# <a name="ordering-file-sequence-numbers-in-a-cabinet-file-table-and-media-table"></a>Ordinamento dei numeri di sequenza dei file in un file CAB, una tabella file e una tabella multimediale

La [tabella File contiene](file-table.md) un elenco completo di tutti i file di origine per l'installazione. I file possono essere archiviati nel supporto di origine come singoli file o compressi all'interno [di file CAB.](cabinet-files.md) I numeri di sequenza nella colonna Sequenza della tabella File, insieme al campo LastSequence della tabella [Supporti](media-table.md), specificano sia l'ordine di installazione per i file che il supporto di origine in cui si trova ogni file. Ogni record nella tabella Media identifica il disco di origine contenente tutti i file con numeri di sequenza minori o uguali al valore visualizzato nella colonna LastSequence e maggiore del valore LastSequence del disco precedente.

Si supponga, ad esempio, che un file abbia un numero di sequenza di 92 immesso nella colonna Sequenza della tabella File. Per determinare il disco di origine in cui si trova questo file, il programma di installazione controlla il record della tabella Media per la voce con il valore lastSequence più piccolo maggiore di 92. La colonna DiskId è la chiave primaria per la tabella Media e questo campo identifica in modo univoco il disco nella tabella.

Il limite massimo per il numero di file che possono essere elencati nella tabella File di un pacchetto Windows Installer è di 32767 file. Per creare un pacchetto Windows Installer contenente più file, vedere [Creazione di un pacchetto di grandi dimensioni.](authoring-a-large-package.md)

Gli autori di pacchetti possono ridurre le dimensioni dei pacchetti di installazione comprimendo i file di origine e includendoli nei file CAB. L'immagine del file di origine può essere compressa, non compressa o una combinazione di entrambi i tipi. Per altre informazioni sulle origini compresse e non compresse, vedere [Origini compresse e non compresse.](compressed-and-uncompressed-sources.md) I file di origine compressi devono essere archiviati all'interno di un file CAB. I file compressi all'interno di un file CAB hanno i propri numeri di sequenza interni. Non è necessario che i valori di questi numeri di sequenza interni corrispondano al valore dei numeri di sequenza all'interno della tabella File. Tuttavia, la sequenza dei file specificata nella tabella File deve essere identica alla sequenza effettiva dei file all'interno dei file CAB. I numeri di sequenza dei file non compressi non devono essere univoci. Ad esempio, se tutti i file non sono compressi e si trovano in un disco, tutti i file possono avere lo stesso numero di sequenza nella tabella File.

La tabella Supporti descrive il set di dischi che costituiscono il supporto di origine per l'installazione. La prima voce nella tabella Media deve avere sempre un valore 1 nel campo DiskId. I file devono essere organizzati nel supporto di origine in modo che tutti i file sul disco 1 presentino numeri di sequenza della tabella file inferiori ai numeri di sequenza dei file sul disco 2 e che tutti i numeri di sequenza sul disco 2 siano inferiori a quelli sul disco 3 e così via. Questo requisito si applica anche a un disco che contiene origini compresse e non compresse. Ad esempio, se le origini dei supporti per l'installazione si trovano in due dischi di origine e se il disco 1 contiene sia file non compressi che file CAB, entrambi i file non compressi e i file nel file CAB devono avere numeri di sequenza inferiori al numero di sequenza di file più piccolo di qualsiasi file archiviato sul disco 2. Se tutti i file sul disco 1 sono compressi in un file CAB, è possibile creare la tabella Supporti come illustrato nella tabella seguente.

[Media Table](media-table.md) (partial)



| DiskId | LastSequence | DiskPrompt | armadietto   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          | mycab.cab | Disco 1      |
| 2      | 10           | 2          |           | Disco 2      |



 

Se alcuni file sul disco 1 sono compressi in un file CAB e altri non sono compressi, è possibile creare la tabella Supporti come indicato di seguito.

[Media Table](media-table.md) (partial)



| DiskId | LastSequence | DiskPrompt | armadietto   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disco 1      |
| 2      | 10           | 1          | mycab.cab | Disco 1      |
| 3      | 15           | 2          |           | Disco 2      |



 

Si noti che la creazione nella tabella Media seguente non è corretta perché specifica alcuni numeri di sequenza di file sul disco 2 che sono più piccoli di alcuni file all'interno del file CAB sul disco 1.

[Tabella supporti](media-table.md)



| DiskId | LastSequence | DiskPrompt | armadietto   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disco 1      |
| 2      | 10           | 2          |           | Disco 2      |
| 3      | 15           | 1          | mycab.cab | Disco 1      |



 

I file di grandi dimensioni possono essere suddivisi tra due o più file CAB. Non possono essere presenti più di 15 file in un file CAB che si estende fino al file CAB successivo. Ad esempio, se si dispone di tre file CAB, il primo file CAB può avere 15 file che si estendono al secondo file CAB e il secondo file CAB può avere 15 file che si estendono al terzo file CAB. Quando si aggiunge un record alla tabella File per più file CAB, usare la prima parte del file per specificare il numero di sequenza del file immesso nella colonna Sequenza .

Le tabelle File e Supporti possono essere scritte come segue se sono presenti tre file, due file CAB e due dischi. In questo esempio, c1.cab risiede su disk1 e c2.cab risiede su disk2. Il file f2 si estende su entrambi gli archivi. Il c1.cab file CAB contiene l'intero file f1 e la prima parte del file f2. Il c2.cab file CAB contiene la seconda parte di f2 e l'intero file f3.

[Media Table](media-table.md) (partial)



| DiskId | LastSequence | DiskPrompt | armadietto | VolumeLabel |
|--------|--------------|------------|---------|-------------|
| 1      | 5            | 1          | c1.cab  | Disco 1      |
| 2      | 10           | 2          | c2.cab  | Disco 2      |



 

[Tabella file](file-table.md) (parziale)



| File | Sequenza |
|------|----------|
| f1   | 1        |
| f2   | 2        |
| f3   | 6        |



 

 

 



