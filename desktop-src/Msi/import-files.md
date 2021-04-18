---
description: Il file VBScript WiImport.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. In questo esempio viene illustrato come scrivere uno script per importare le tabelle in un database Windows Installer.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importa file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308903"
---
# <a name="import-files"></a>Importa file

Il file VBScript WiImport.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come scrivere uno script per importare le tabelle in un database Windows Installer.

Lo script si connette a un oggetto del [**programma di installazione**](installer-object.md) , apre un database, elabora un elenco di file ed esegue il commit delle modifiche prima di chiudere il database.

Nell'esempio viene illustrato l'utilizzo di:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)
-   [**Metodo Import**](database-import.md)
-   [**Metodo commit**](database-commit.md) dell' [ **oggetto di database**](database-object.md)

Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire l'esempio, utilizzare la sintassi seguente al prompt dei comandi.

**cscript WiImport.vbs \[ percorso del percorso del database \] \[ all' \] \[ \] \[ elenco dei file di archivio delle opzioni della cartella**\]

La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ percorso del file \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

Specificare il percorso di un database di Windows Installer da creare o che deve ricevere le tabelle importate. Specificare il percorso della cartella contenente i file di archivio delle tabelle da importare. Elenca i nomi dei file di archivio che vengono importati. \*Per importare più file, è possibile usare nomi di file con caratteri jolly, ad esempio IDT.

Le opzioni seguenti possono essere specificate in un punto qualsiasi della riga di comando prima dell'elenco dei file.



| Opzione              | Descrizione                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| non è stata specificata alcuna opzione | Importa l'elenco dei file di archivio tabelle dalla cartella specificata nel database Windows Installer.                                |
| /C                  | Creare un database di Windows Installer e quindi importare l'elenco dei file di archivio tabelle dalla cartella specificata al nuovo database. |



 

Per ulteriori informazioni, vedere [Windows Installer esempi di script](windows-installer-scripting-examples.md) per ulteriori esempi di scripting. Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

Si noti che in [un esempio di localizzazione](a-localization-example.md) viene inoltre illustrato l' [importazione delle tabelle ActionText e degli errori localizzati](importing-localized-error-and-actiontext-tables.md).

 

 



