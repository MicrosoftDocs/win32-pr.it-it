---
description: Un file CAB è un singolo file, in genere con estensione cab, che archivia i file compressi in una libreria di file.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: File CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311005"
---
# <a name="cabinet-files"></a>File CAB

Un file CAB è un singolo file, in genere con estensione cab, che archivia i file compressi in una libreria di file. Il formato CAB è un modo efficiente per creare un pacchetto di più file perché la compressione viene eseguita tra i limiti dei file, migliorando significativamente il rapporto di compressione.

Gli sviluppatori possono usare uno strumento per la creazione di file CAB, ad esempio Makecab.exe per creare file CAB da usare con i pacchetti del programma di installazione. L'utilità Makecab.exe è inclusa nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

Gli sviluppatori possono inoltre usare uno strumento di creazione di file CAB, ad esempio Cabarc.exe per creare file CAB da usare con i pacchetti del programma di installazione. Questo strumento scrive nella struttura del cabinet del diamante.

Le chiavi dei file archiviati all'interno di un file CAB devono corrispondere alle voci della colonna file della [tabella file](file-table.md) e la sequenza di file nel file CAB deve corrispondere alla sequenza di file specificata nella colonna sequenza. Per altre informazioni, vedere [uso di cabinet e origini compresse](using-cabinets-and-compressed-sources.md).

I file di grandi dimensioni possono essere suddivisi tra due o più file CAB. Non possono essere presenti più di 15 file in un file CAB che si estende al file CAB successivo. Se, ad esempio, si dispone di tre file CAB, il primo file CAB può includere 15 file che si estendono al secondo file CAB e il secondo file CAB può includere 15 file che si estendono al terzo file CAB.

Il programma di installazione estrae i file da un file CAB perché sono necessari per l'installazione e li installa nello stesso ordine in cui vengono archiviati nel file CAB. I requisiti di spazio per l'installazione di un file archiviato in un file CAB non sono diversi da quelli per l'installazione di un file non compresso.

Un file CAB può trovarsi all'interno o all'esterno del file con estensione msi. A partire da Windows Installer 5,0 in esecuzione in Windows 7 o Windows Server 2008 R2 il programma di installazione salva tutti i cabinet incorporati nel file con estensione msi prima di memorizzare nella cache il pacchetto di installazione.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Per conservare spazio su disco, il programma di installazione rimuove sempre tutti i cabinet incorporati nel file con estensione msi prima di memorizzare nella cache il pacchetto di installazione nel computer dell'utente.

 

 



