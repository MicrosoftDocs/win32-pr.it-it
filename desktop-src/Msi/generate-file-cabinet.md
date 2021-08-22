---
description: Il file VBScript WiMakCab.vbs è disponibile in componenti sdk Windows per Windows programma di installazione. Questo esempio illustra come viene usato lo script per generare file CAB da un database Windows Installer.
ms.assetid: 26671cb9-a200-4520-8b52-4cff3f71a2f2
title: Generare file CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca9e30822d0683aa09dc015ec2fd98d1f598c70e0fd63fd00f66a6bcdf3edf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581491"
---
# <a name="generate-file-cabinet"></a>Generare file CAB

Il file VBScript WiMakCab.vbs è disponibile in componenti sdk Windows [per Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md). Questo esempio illustra come viene usato lo script per generare file CAB da un database Windows Installer.

Questo esempio dimostra:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md) e [**metodo LastErrorRecord**](installer-lasterrorrecord.md) dell'oggetto [**Installer**](installer-object.md)
-   [**Metodo Commit**](database-commit.md), metodo [**OpenView e**](database-openview.md) [**proprietà SummaryInformation (oggetto database)**](database-summaryinformation.md) dell'oggetto [**database**](database-object.md)
-   [**Metodo Fetch,**](view-fetch.md) [**metodo Execute**](view-execute.md) [**e metodo Modify**](view-modify.md) dell'oggetto [**View**](view-object.md)
-   [**Proprietà StringData**](record-stringdata.md) e [**proprietà IntegerData**](record-integerdata.md) dell'oggetto [**Record**](record-object.md)
-   [**Metodo DoAction**](session-doaction.md), [**proprietà Property (oggetto Sessione)**](session-session.md) [**e proprietà Mode**](session-mode.md) dell'oggetto [**Sessione**](session-object.md)

Per usare questo esempio è CScript.exe o WScript.exe'host di script Windows. Per usare CScript.exe questo esempio, digitare un comando al prompt dei comandi usando la sintassi seguente. Se il primo argomento è /? viene visualizzata la Guida o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . L'esempio restituisce il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script ha esito negativo.

**cscript WiMakCab.vbs \[ percorso di origine facoltativo \] \[ del nome di base \] \[ del database\]**

Per generare un file cab, Makecab.exe deve essere in PATH. LMakecab.exe utilità è inclusa [nell'Windows SDK per gli](platform-sdk-components-for-windows-installer-developers.md)sviluppatori Windows programma di installazione . Si noti che l'esempio non aggiorna la [tabella Media per](media-table.md) gestire più archivi. Per sostituire un file cab incorporato, includere le opzioni /R /C /U /E.

Specificare il percorso del database del programma di installazione. Deve trovarsi nella radice dell'albero di origine. Specificare il nome di base con distinzione tra maiuscole e minuscole per i file CAB generati. Se il tipo di origine è compresso, tutti i file vengono aperti nella radice. Le opzioni seguenti possono essere specificate in qualsiasi punto della riga di comando.



| Opzione              | Descrizione                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| nessuna opzione specificata |                                                                                                                                           |
| /C                  | Eseguire la compressione. Se /C non viene specificato, WiMakCab.vbs genera solo il file DDF.                                                        |
| /L                  | Usare la compressione LZX anziché MSZIP                                                                                                      |
| /F                  | Limitare le dimensioni dell'archivio a 1,44 MB di dimensioni floppy anziché a CD-ROM                                                                              |
| /U                  | Aggiornare il database per fare riferimento all'archivio generato                                                                                    |
| /E                  | Incorporare il file cab nel pacchetto del programma di installazione come flusso                                                                               |
| /S                  | Usare i numeri di sequenza nella tabella File ordinata in base alle directory                                                                             |
| /R                  | Ripristinare l'installazione non cab, rimuovere cab se è specificato /E (l'opzione /R rimuove il bit compresso - proprietà SummaryInfo 15 & 2) |



 

Per altri esempi di scripting, vedere Windows [di scripting del programma di installazione](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 



