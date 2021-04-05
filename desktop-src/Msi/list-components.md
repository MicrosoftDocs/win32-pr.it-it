---
description: Il file VBScript WiCompon.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Questo script di esempio può essere usato per elencare i componenti in un database Windows Installer.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Elenca componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b79fa34f62374632ec7fdf52a13c6da8ddbfd82a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751703"
---
# <a name="list-components"></a>Elenca componenti

Il file VBScript WiCompon.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio può essere usato per elencare i componenti in un database Windows Installer.

In questo esempio viene illustrato l'utilizzo di varie chiavi primarie nella [tabella dei componenti](component-table.md).

Nell'esempio viene inoltre illustrato quanto segue:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md), [**Metodo CreaRecord**](installer-createrecord.md)e [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [**oggetto Installer**](installer-object.md).
-   Il [**Metodo OpenView**](database-openview.md), la [**Proprietà TablePersistent**](database-tablepersistent.md)e la [**Proprietà PrimaryKeys**](database-primarykeys.md) dell' [**oggetto di database**](database-object.md).
-   [**Metodo Execute**](view-execute.md) e [**Metodo fetch**](view-fetch.md) dell' [**oggetto View**](view-object.md).
-   Proprietà di [**Proprietà StringData**](record-stringdata.md) dell' [**oggetto record**](record-object.md).

Per usare questo esempio è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiCompon.vbs il \[ percorso del \] \[ nome del componente del database\]**

Consente di specificare il percorso del database di Windows Installer. Specificare il nome del componente. Il nome deve essere elencato nella colonna componente della tabella dei [componenti](component-table.md). Se il nome del componente viene omesso, vengono elencati tutti i componenti. Se \* come nome del componente viene usato un asterisco () WiCompon.vbs elenca la composizione di tutti i componenti. Si noti che i database di grandi dimensioni vengono visualizzati meglio utilizzando CScript anziché WScript.

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



