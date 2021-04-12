---
description: Il file VBScript WiSubStg.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Gestisci sottoarchivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348976"
---
# <a name="manage-substorages"></a>Gestisci sottoarchivi

Il file VBScript WiSubStg.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come utilizzare lo script per gestire le sottoarchiviazioni in un database Windows Installer. Una trasformazione può essere aggiunta a un database di Windows Installer esistente come sottoarchivio.

Nell'esempio viene illustrato l'utilizzo di:

-   [\_Tabella Storages](-storages-table.md)
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

**cscript WiSubStg.vbs \[ percorso al percorso del database \] \[ \] \[ nome del \] \[ sottoarchivio delle opzioni file\]**

Specificare il percorso del database di Windows Installer per aggiungere o rimuovere l'archivio secondario. Specificare un percorso per il file di trasformazione o di database che viene aggiunto come sottoarchivio. Per elencare le sottoarchiviazioni nel database di Windows Installer, omettere il percorso del file. È possibile specificare un nome di sottoarchiviazione facoltativo, se viene omesso, per impostazione predefinita il nome del sottoarchivio viene impostato sul nome del file.

È possibile specificare l'opzione seguente.



| Opzione              | Descrizione                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| non è stata specificata alcuna opzione | Aggiungere una risorsa di archiviazione al database Windows Installer.                                                 |
| /d                  | Rimuovere un sottoarchivio. Questo flag di opzione deve essere seguito dal nome dell'archivio subarchiviazione da rimuovere. |



 

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

Si noti che [un esempio di localizzazione](a-localization-example.md) illustra [come incorporare le trasformazioni di personalizzazione come sottoarchivio](embedding-customization-transforms-as-substorage.md).

 

 



