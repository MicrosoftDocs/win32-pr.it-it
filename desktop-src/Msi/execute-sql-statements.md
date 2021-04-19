---
description: Il file VBScript WiRunSQL.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: 1027b187-1237-43d1-9905-8fcdaec63903
title: Istruzioni EXECUTE SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99da54f85b02ee867003b140d505f5754f58cc00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310802"
---
# <a name="execute-sql-statements"></a>Istruzioni EXECUTE SQL

Il file VBScript WiRunSQL.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come utilizzare lo script per eseguire query e aggiornamenti SQL su un database Windows Installer. Per altre informazioni, vedere [sintassi SQL](sql-syntax.md) ed [esempi di query sul database con SQL e script](examples-of-database-queries-using-sql-and-script.md).

Lo script di esempio illustra:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md) e [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [**oggetto Installer**](installer-object.md)
-   [**OpenView (metodo**](database-openview.md)) e [**metodo commit**](database-commit.md) dell' [**oggetto di database**](database-object.md)
-   [**Metodo Execute**](view-execute.md) dell' [ **oggetto View**](view-object.md)
-   [**Proprietà StringData**](record-stringdata.md) Propertyof [ **oggetto record**](record-object.md)

Per usare questo esempio è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiRunSQL.vbs \[ percorso di \] \[ query SQL del database\]**

Consente di specificare il percorso di un database Windows Installer. Specificare le query SQL da eseguire. Si noti che la query SQL deve essere racchiusa tra virgolette doppie. Seleziona query consente di visualizzare le righe dell'elenco dei risultati specificato nella query. Le colonne di dati binari selezionate da una query non vengono visualizzate.

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

Per ulteriori informazioni, vedere [utilizzo di query](working-with-queries.md) ed [esempi di query di database tramite SQL e script](examples-of-database-queries-using-sql-and-script.md). Nell' [esempio un esempio di localizzazione](a-localization-example.md) viene illustrato l'utilizzo di SQL per la [localizzazione delle colonne del database](localizing-database-columns.md) e l' [aggiornamento di un flusso di informazioni di riepilogo](updating-a-summary-information-stream.md).

 

 



