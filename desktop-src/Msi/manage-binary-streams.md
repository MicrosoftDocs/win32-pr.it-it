---
description: Il file VBScript WiStream.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Gestisci flussi binari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316266"
---
# <a name="manage-binary-streams"></a>Gestisci flussi binari

Il file VBScript WiStream.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come utilizzare gli script per gestire i flussi binari in un database Windows Installer. È possibile utilizzare l'esempio per immettere file CAB compressi in un database. In questo esempio viene illustrata l'operazione della [ \_ tabella Streams](-streams-table.md) nel database Windows Installer.

Nell'esempio viene inoltre illustrato l'utilizzo di:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo CreaRecord**](installer-createrecord.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)
-   [**OpenView (metodo)**](database-openview.md)
-   [**Metodo commit**](database-commit.md) dell' [ **oggetto di database**](database-object.md)
-   [**Fetch (metodo)**](view-fetch.md)
-   [**Metodo Modify**](view-modify.md)
-   [**Metodo Execute**](view-execute.md) dell' [ **oggetto View**](view-object.md)
-   [**Proprietà StringData**](record-stringdata.md)
-   [**Metodo sestream**](record-setstream.md) dell' [ **oggetto record**](record-object.md)

Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiStream.vbs \[ percorso al percorso del database \] \[ per il nome del \] \[ flusso di opzioni \] \[ file\]**

Specificare il percorso del database di Windows Installer che deve ricevere il flusso. Specificare il percorso del file binario contenente i dati del flusso. Per elencare i flussi nel database del programma di installazione, omettere questo percorso. È possibile specificare un nome di flusso facoltativo. Se viene omesso, viene impostato come predefinito il nome del file.

È possibile specificare l'opzione seguente.



| Opzione              | Descrizione                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| non è stata specificata alcuna opzione | Aggiungere un flusso al database Windows Installer.                                                 |
| /d                  | Rimuovere un flusso. Questo flag di opzione deve essere seguito dal nome della sottoarchiviazione da rimuovere. |



 

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



