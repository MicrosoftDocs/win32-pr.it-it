---
description: Il file VBScript WiFeatur.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: 797cb383-22c0-42b4-82c1-d5bcc3a8bafb
title: Elencare le funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e166401b514f1beec9c14c74aba7ca0601f446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345056"
---
# <a name="list-features"></a>Elencare le funzionalità

Il file VBScript WiFeatur.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come utilizzare lo script per elencare le funzionalità di un database di Windows Installer. In questo esempio viene illustrata l'aggiunta di colonne temporanee a un database di Windows Installer di sola lettura.

Questo esempio dimostra:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md), [**Metodo CreaRecord**](installer-createrecord.md)e [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [**oggetto Installer**](installer-object.md)
-   [**Metodo Execute**](view-execute.md) e [**Metodo fetch**](view-fetch.md) dell' [**oggetto View**](view-object.md)
-   [**Metodo OpenView**](database-openview.md), la [**Proprietà TablePersistent**](database-tablepersistent.md)e la [**Proprietà PrimaryKeys**](database-primarykeys.md) dell'oggetto di [**database**](database-object.md)
-   [**Proprietà FieldCount**](record-fieldcount.md), [**Proprietà IntegerData**](record-integerdata.md)e [**Proprietà StringData**](record-stringdata.md) dell' [**oggetto record**](record-object.md)

Per usare questo esempio è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiFeatur.vbs il \[ percorso del \] \[ nome della funzionalità del database\]**

Consente di specificare il percorso del database di Windows Installer. Specificare il nome della funzionalità. Questa deve essere elencata nella colonna feature della [tabella Feature](feature-table.md). Se il nome della funzionalità viene omesso, tutte le funzionalità sono elencate come albero delle funzionalità. Se \* come nome della funzionalità viene usato un asterisco (), WiFeatur.vbs elenca la composizione di tutte le funzionalità. Si noti che i database di grandi dimensioni vengono visualizzati meglio utilizzando CScript anziché WScript.

Per ulteriori informazioni, vedere [Windows Installer esempi di script](windows-installer-scripting-examples.md) per ulteriori esempi di scripting. Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



