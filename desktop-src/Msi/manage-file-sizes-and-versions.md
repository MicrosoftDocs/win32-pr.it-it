---
description: Il file VBScript WiFilVer.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Nell'esempio viene illustrato come utilizzare uno script per segnalare o aggiornare la versione del file, le dimensioni e le informazioni sulla lingua.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Gestire le dimensioni e le versioni dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752775"
---
# <a name="manage-file-sizes-and-versions"></a>Gestire le dimensioni e le versioni dei file

Il file VBScript WiFilVer.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Nell'esempio viene illustrato come utilizzare uno script per segnalare o aggiornare la versione del file, le dimensioni e le informazioni sulla lingua.

Nell'esempio vengono inoltre illustrate le azioni Windows Installer, le modalità di accesso a un database Windows Installer e l'utilizzo degli elementi seguenti:

-   Metodo [**Installer. OpenDatabase**](installer-opendatabase.md) dell' [ **oggetto Installer**](installer-object.md)
-   Proprietà [**Installer. FileAttributes**](installer-fileattributes.md)
-   [**Installer. filehash**](installer-filehash.md) (metodo)
-   [**Installer. FileVersion**](installer-fileversion.md) (metodo)
-   Metodo [**Installer. LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)
-   Metodo [**database. OpenView**](database-openview.md)
-   Proprietà [**database. SummaryInformation**](database-summaryinformation.md) dell' [ **oggetto di database**](database-object.md)
-   [**Session. DoAction,**](session-doaction.md) metodo
-   [**Session. Property**](session-session.md)
-   Proprietà [**Session. SourcePath**](session-sourcepath.md)
-   Proprietà [**Session. Mode**](session-mode.md) dell' [ **oggetto Session**](session-object.md)
-   Proprietà [**record. StringData**](record-stringdata.md)
-   Proprietà [**record. IntegerData**](record-integerdata.md) dell' [ **oggetto record**](record-object.md)

Per usare questo esempio è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente:

**cscript WiFilVer.vbs \[ percorso di \] \[ origine facoltativo del database\]**

Tenere inoltre presente quanto segue:

-   La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti.
-   Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .
-   L'esempio restituisce un valore pari a 0 (zero) per esito positivo, 1 (uno) se la guida viene richiamata e 2 (due) se lo script non riesce.

Specificare il database di Windows Installer che si desidera aggiornare, che deve trovarsi nella radice del file di origine. Tuttavia, è possibile specificare le origini per il database in posizioni separate. Se l'origine è compressa, tutti i file vengono aperti alla radice.

È possibile specificare le opzioni seguenti in qualsiasi posizione nella riga di comando.



| Opzione                | Descrizione                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| *non è stata specificata alcuna opzione* | Visualizza le informazioni sul file del database.                                            |
| /U                    | Aggiornare le informazioni relative alle dimensioni, alla versione e alla lingua del file nel database dall'origine. |



 

Per ulteriori informazioni, vedere [Windows Installer esempi di script](windows-installer-scripting-examples.md) e [strumenti di sviluppo Windows Installer](windows-installer-development-tools.md).

 

 



