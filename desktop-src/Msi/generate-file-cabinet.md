---
description: Il file VBScript WiMakCab.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. In questo esempio viene illustrato come utilizzare lo script per generare file CAB da un database Windows Installer.
ms.assetid: 26671cb9-a200-4520-8b52-4cff3f71a2f2
title: Genera file CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df2355c247ff602d644d2865ec3b9d9a8447ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967803"
---
# <a name="generate-file-cabinet"></a>Genera file CAB

Il file VBScript WiMakCab.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come utilizzare lo script per generare file CAB da un database Windows Installer.

Questo esempio dimostra:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md) e [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [**oggetto Installer**](installer-object.md)
-   [**Metodo commit**](database-commit.md), il [**Metodo OpenView**](database-openview.md) e la [**Proprietà SummaryInformation (oggetto di database)**](database-summaryinformation.md) dell' [**oggetto di database**](database-object.md)
-   [**Metodo fetch**](view-fetch.md), metodo [**Execute**](view-execute.md) e [**metodo modify**](view-modify.md) dell' [**oggetto View**](view-object.md)
-   [**Proprietà StringData**](record-stringdata.md) e [**Proprietà IntegerData**](record-integerdata.md) dell' [**oggetto record**](record-object.md)
-   [**Metodo DoAction**](session-doaction.md), [**Proprietà Property (oggetto Session)**](session-session.md)e [**proprietà Mode**](session-mode.md) dell' [**oggetto Session**](session-object.md)

Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiMakCab.vbs \[ percorso del \] \[ nome base del database percorsi di \] \[ origine facoltativi\]**

Per generare un file CAB, Makecab.exe deve trovarsi nel percorso. L'utilità Makecab.exe è inclusa nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Si noti che l'esempio non aggiorna la [tabella dei supporti](media-table.md) per gestire più file CAB. Per sostituire un file CAB incorporato, includere le opzioni:/R/C/U/E.

Specificare il percorso del database del programma di installazione. Deve trovarsi nella radice dell'albero di origine. Specificare il nome di base con distinzione tra maiuscole e minuscole per i file CAB generati. Se il tipo di origine è compresso, tutti i file vengono aperti alla radice. È possibile specificare le opzioni seguenti in qualsiasi punto della riga di comando.



| Opzione              | Descrizione                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| non è stata specificata alcuna opzione |                                                                                                                                           |
| /C                  | Eseguire la compressione. Se/C non è specificato, WiMakCab.vbs genera solo il file DDF.                                                        |
| /L                  | Usare la compressione LZX anziché MSZIP                                                                                                      |
| /F                  | Limitare le dimensioni del cabinet a dimensioni floppy di 1,44 MB anziché CD-ROM                                                                              |
| /U                  | Aggiornare il database in modo che faccia riferimento al file CAB generato                                                                                    |
| /E                  | Incorporare il file CAB nel pacchetto del programma di installazione come flusso                                                                               |
| /S                  | USA i numeri di sequenza nella tabella file ordinata in base alle directory                                                                             |
| /R                  | Ripristinare un'installazione non-cabinet, rimuovere il file CAB se è specificato/E (l'opzione/R rimuove la proprietà bit-SummaryInfo compressa 15 & 2) |



 

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



