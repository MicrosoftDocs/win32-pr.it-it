---
description: Il file VBScript WiSubStg.vbs è disponibile in componenti sdk Windows per Windows programma di installazione.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Gestire le sottocartelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f6d3a0716854755e595133771ede65b11212cdd0fd19b4502bab0c631a9d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945596"
---
# <a name="manage-substorages"></a>Gestire le sottocartelle

Il file VBScript WiSubStg.vbs è disponibile in componenti dell'SDK Windows per [Windows programma di installazione.](platform-sdk-components-for-windows-installer-developers.md) Questo esempio illustra come usare lo script per gestire le sottocartelle in un database Windows Installer. È possibile aggiungere una trasformazione a un database esistente Windows Installer come sottostorage.

L'esempio illustra l'uso di:

-   [\_Tabella Di archiviazione](-storages-table.md)
-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo CreateRecord**](installer-createrecord.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) [ **dell'oggetto Installer**](installer-object.md)
-   [**Metodo OpenView**](database-openview.md)
-   [**Metodo Commit**](database-commit.md) [ **dell'oggetto Database**](database-object.md)
-   [**Metodo Fetch**](view-fetch.md)
-   [**Metodo Modify**](view-modify.md)
-   [**Metodo Execute**](view-execute.md) [ **dell'oggetto View**](view-object.md)
-   [**StringData - proprietà**](record-stringdata.md)
-   [**Metodo SetStream**](record-setstream.md) [ **dell'oggetto Record**](record-object.md)

Per usare questo esempio, è CScript.exe o WScript.exe'host di script Windows. Per usare CScript.exe eseguire questo esempio, digitare una riga di comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . L'esempio restituisce il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script ha esito negativo.

**cscript WiSubStg.vbs \[ percorso del database per le opzioni file nome di archiviazione \] \[ \] \[ \] \[ secondaria\]**

Specificare il percorso del database del Windows Installer per aggiungere o rimuovere le sottocartelle. Specificare un percorso per il file di trasformazione o di database che viene aggiunto come archiviazione secondaria. Per elencare le sottocartelle nel database Windows Installer, omettere il percorso di questo file. È possibile specificare un nome di archiviazione secondario facoltativo, se viene omesso il nome dell'archiviazione secondaria viene utilizzato per impostazione predefinita per il nome file.

È possibile che venga specificata l'opzione seguente.



| Opzione              | Descrizione                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| nessuna opzione specificata | Aggiungere un'archiviazione secondaria al database Windows Installer.                                                 |
| /d                  | Rimuovere un'archiviazione secondaria. Questo flag di opzione deve essere seguito dal nome dell'archiviazione secondaria da rimuovere. |



 

Per altri esempi di scripting, vedere Windows [di scripting del programma di installazione](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

Si noti [che un esempio di localizzazione illustra](a-localization-example.md) [l'incorporamento di trasformazioni di personalizzazione come archiviazione secondaria.](embedding-customization-transforms-as-substorage.md)

 

 



