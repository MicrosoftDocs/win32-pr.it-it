---
description: Il file VBScript WiExport.vbs è disponibile in componenti sdk Windows per Windows programma di installazione.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Esportare file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7cab882778bce6d84412f53987c65211f70f4a8a10b52836ad993d8e813304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044441"
---
# <a name="export-files"></a>Esportare file

Il file VBScript WiExport.vbs è disponibile in componenti dell'SDK Windows per [Windows programma di installazione.](platform-sdk-components-for-windows-installer-developers.md) Questo esempio illustra come scrivere script per esportare tabelle in un database Windows Installer. L'esempio di script si connette a un [**oggetto Installer,**](installer-object.md) apre un database ed esporta tabelle in file di archivio.

L'esempio illustra l'uso di:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) [ **dell'oggetto Installer**](installer-object.md)
-   [**Metodo Export**](database-export.md)
-   [**Metodo OpenView**](database-openview.md) [ **dell'oggetto Database**](database-object.md)
-   [**Metodo Fetch**](view-fetch.md) [ **dell'oggetto View**](view-object.md)
-   [**Proprietà StringData**](record-stringdata.md) [ **dell'oggetto Record**](record-object.md)

Per usare questo esempio, è CScript.exe o WScript.exe'host di script Windows. Per usare CScript.exe eseguire questo esempio, digitare una riga di comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . L'esempio restituisce il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script ha esito negativo.

**cscript WiExport.vbs \[ percorso del database \] \[ all'elenco dei \] \[ \] \[ nomi di tabella delle opzioni cartella\]**

Specificare il percorso del database del programma di installazione da cui vengono esportate le tabelle. Specificare il percorso della cartella in cui copiare i file di archivio esportati. Elencare i nomi con distinzione tra maiuscole e minuscole delle [tabelle di database](database-tables.md) esportate. Specificare ' \* ' per esportare tutte le tabelle, inclusa \_ SummaryInformation.

Le opzioni seguenti possono essere specificate in qualsiasi punto della riga di comando prima dell'elenco dei nomi di tabella.



| Opzione              | Descrizione                                            |
|---------------------|--------------------------------------------------------|
| nessuna opzione specificata | I file di archivio esportati possono avere un nome file lungo.      |
| /s                  | Forzare i file di archivio esportati in modo che abbia nomi di file brevi. |



 

Per altri esempi di scripting, vedere Windows [di scripting del programma di installazione](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 



