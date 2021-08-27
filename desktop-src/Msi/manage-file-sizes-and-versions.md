---
description: Il file VBScript WiFilVer.vbs disponibile in Windows SDK Components for Windows Installer Developers. Nell'esempio viene illustrato come utilizzare uno script per segnalare o aggiornare la versione del file, le dimensioni e le informazioni sulla lingua.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Gestire le dimensioni e le versioni dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79dcb5bec9b7fd24d7171efed9295479e56d979a3f7aa69352f2231d409417f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629042"
---
# <a name="manage-file-sizes-and-versions"></a>Gestire le dimensioni e le versioni dei file

Il file VBScript WiFilVer.vbs in Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Nell'esempio viene illustrato come utilizzare uno script per segnalare o aggiornare la versione del file, le dimensioni e le informazioni sulla lingua.

L'esempio illustra anche Windows di installazione, come accedere a un database del programma di installazione di Windows e come usare quanto segue:

-   [**Metodo Installer.OpenDatabase**](installer-opendatabase.md) [ **dell'oggetto Installer**](installer-object.md)
-   [**Installer.FileAttributes -**](installer-fileattributes.md) proprietà
-   [**Metodo Installer.FileHash**](installer-filehash.md)
-   [**Metodo Installer.FileVersion**](installer-fileversion.md)
-   [**Metodo Installer.LastErrorRecord**](installer-lasterrorrecord.md) dell'oggetto [ **Installer**](installer-object.md)
-   [**Metodo Database.OpenView**](database-openview.md)
-   [**Proprietà Database.SummaryInformation**](database-summaryinformation.md) [ **dell'oggetto di database**](database-object.md)
-   [**Metodo Session.DoAction**](session-doaction.md)
-   [**Session.Property**](session-session.md)
-   [**Session.SourcePath -**](session-sourcepath.md) proprietà
-   [**Proprietà Session.Mode**](session-mode.md) [ **dell'oggetto Session**](session-object.md)
-   [**Record.StringData -**](record-stringdata.md) proprietà
-   [**Proprietà Record.IntegerData**](record-integerdata.md) [ **dell'oggetto Record**](record-object.md)

L'uso di questo esempio richiede CScript.exe o WScript.exe versione di Windows Script Host. Per usare CScript.exe eseguire questo esempio, digitare un comando al prompt dei comandi usando la sintassi seguente:

**cscript WiFilVer.vbs \[ percorso di origine facoltativo \] \[ del database\]**

Tenere presente anche quanto segue:

-   La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti.
-   Per reindirizzare l'output a un file, terminare la riga di comando con vbs > \[ *percorso del file* \] .
-   Nell'esempio viene restituito il valore 0 (zero) per l'esito positivo, 1 (uno) se viene richiamata la Guida e 2 (due) se lo script ha esito negativo.

Specificare il Windows del programma di installazione che si vuole aggiornare, che deve trovarsi nella radice del file di origine. Tuttavia, è possibile specificare le origini per il database in posizioni separate. Se l'origine è compressa, tutti i file vengono aperti nella radice.

Le opzioni seguenti possono essere specificate in qualsiasi posizione nella riga di comando.



| Opzione                | Descrizione                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| *nessuna opzione specificata* | Consente di visualizzare le informazioni sul file del database.                                            |
| /U                    | Aggiornare le informazioni sulle dimensioni, la versione e la lingua del file nel database dall'origine. |



 

Per altre informazioni, vedere Esempi [Windows di scripting](windows-installer-scripting-examples.md) del programma di installazione e strumenti Windows di sviluppo del programma di [installazione.](windows-installer-development-tools.md)

 

 



