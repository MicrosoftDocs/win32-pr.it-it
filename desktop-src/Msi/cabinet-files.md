---
description: Un file cab è un singolo file, in genere con .cab, che archivia i file compressi in una libreria di file.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: File CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2331b60c42bf975856987d1e13d67c95bc01fa685f99f49543650c48347cac49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380721"
---
# <a name="cabinet-files"></a>File CAB

Un file cab è un singolo file, in genere con .cab, che archivia i file compressi in una libreria di file. Il formato cab è un modo efficiente per creare un pacchetto di più file perché la compressione viene eseguita tra i limiti dei file, migliorando in modo significativo il rapporto di compressione.

Gli sviluppatori possono usare uno strumento di creazione di file cab, ad esempio Makecab.exe creare file cab da usare con i pacchetti del programma di installazione. LMakecab.exe utilimentazione è inclusa [nell'Windows SDK per sviluppatori Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

Gli sviluppatori possono anche usare uno strumento di creazione di file cab, ad esempio Cabarc.exe per creare file cab da usare con i pacchetti del programma di installazione. Questo strumento scrive nella struttura dell'archivio Diamond.

Le chiavi file dei file archiviati all'interno di un file CAB devono corrispondere alle voci nella colonna File della tabella [File](file-table.md) e la sequenza di file nel file cab deve corrispondere alla sequenza di file specificata nella colonna Sequence. Per altre informazioni, vedere [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).

I file di grandi dimensioni possono essere suddivisi tra due o più file CAB. Non possono essere presenti più di 15 file in un file CAB che si estende fino al file CAB successivo. Ad esempio, se si dispone di tre file CAB, il primo file cab può avere 15 file che si estendono al secondo file cab e il secondo file cab può avere 15 file che si estendono al terzo file cab.

Il programma di installazione estrae i file da un file cab in base alle esigenze dell'installazione e li installa nello stesso ordine in cui vengono archiviati nel file cab. I requisiti di spazio per l'installazione di un file archiviato in un file cab non sono diversi da quelli per l'installazione di un file non compresso.

Un file cab può trovarsi all'interno o all'esterno .msi file. A partire da Windows Installer 5.0 in esecuzione in Windows 7 o Windows Server 2008 R2, il programma di installazione salva tutti gli archivi incorporati nel file .msi prima di memorizzare nella cache il pacchetto di installazione.

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Per risparmiare spazio su disco, il programma di installazione rimuove sempre tutti gli archivi incorporati nel file .msi prima di memorizzare nella cache il pacchetto di installazione nel computer dell'utente.

 

 



