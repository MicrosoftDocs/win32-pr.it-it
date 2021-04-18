---
description: Il file VBScript WiExport.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Esporta file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309485"
---
# <a name="export-files"></a>Esporta file

Il file VBScript WiExport.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come scrivere uno script per esportare le tabelle in un database Windows Installer. L'esempio di script si connette a un oggetto del [**programma di installazione**](installer-object.md) , apre un database ed Esporta le tabelle in file di archivio.

Nell'esempio viene illustrato l'utilizzo di:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)
-   [**Export (metodo)**](database-export.md)
-   [**Metodo OpenView**](database-openview.md) dell' [ **oggetto di database**](database-object.md)
-   [**Metodo fetch**](view-fetch.md) dell' [ **oggetto View**](view-object.md)
-   [**Proprietà StringData**](record-stringdata.md) dell' [ **oggetto record**](record-object.md)

Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiExport.vbs \[ percorso del percorso del database \] \[ all' \] \[ \] \[ elenco di nomi di tabella Opzioni cartella\]**

Consente di specificare il percorso del database del programma di installazione da cui vengono esportate le tabelle. Consente di specificare il percorso della cartella in cui devono essere copiati i file di archivio esportati. Elenca i nomi con distinzione tra maiuscole e minuscole delle [tabelle di database](database-tables.md) esportate. Specificare ' \* ' per esportare tutte le tabelle \_ , incluso SummaryInformation.

È possibile specificare le opzioni seguenti in qualsiasi punto della riga di comando prima dell'elenco nome tabella.



| Opzione              | Descrizione                                            |
|---------------------|--------------------------------------------------------|
| non è stata specificata alcuna opzione | I file di archivio esportati possono avere un nome file lungo.      |
| /s                  | Forzare i file di archivio esportati con nomi di file brevi. |



 

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



