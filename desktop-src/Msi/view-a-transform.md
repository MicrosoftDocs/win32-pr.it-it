---
description: Il file VBScript WiLstXfm.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Questo esempio di script può essere utilizzato per visualizzare un file di trasformazione.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Visualizzazione di una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306568"
---
# <a name="view-a-transform"></a>Visualizzazione di una trasformazione

Il file VBScript WiLstXfm.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Questo esempio di script può essere utilizzato per visualizzare un file di trasformazione.

Nell'esempio viene illustrato l'utilizzo di:

-   [\_Tabella transformview](-transformview-table.md)
-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)
-   [**Metodo ApplyTransform**](database-applytransform.md)
-   [**OpenView (metodo)**](database-openview.md)
-   [**Metodo commit**](database-commit.md) dell' [ **oggetto di database**](database-object.md)
-   [**Proprietà IsNull**](record-isnull.md)
-   [**Proprietà StringData**](record-stringdata.md) dell' [ **oggetto record**](record-object.md)

Per usare questo esempio è necessaria la versione CScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiLstXfm.vbs** *\[ percorso per fare riferimento al \] \[ percorso dell'opzione \] \[ di database per \] la trasformazione da visualizzare*

Consente di specificare il percorso del database di riferimento Windows Installer. Consente di specificare un elenco di percorsi per trasformare i file che vengono visualizzati. Ogni percorso nell'elenco può essere preceduto da un valore numerico facoltativo. Questo valore specifica un set di condizioni di errore che devono essere eliminati. È possibile aggiungere questi valori insieme per escludere più condizioni. Se non viene specificata alcuna opzione numerica, tutte le condizioni di errore vengono evitate. Gli argomenti in questo elenco vengono eseguiti nell'ordine da sinistra a destra in cui vengono visualizzati nella riga di comando.



| Valore | Condizione di errore da disattivare                   |
|-------|-----------------------------------------------|
| 1     | Aggiunta di una riga già esistente.             |
| 2     | Eliminazione di una riga inesistente.           |
| 4     | Aggiunta di una tabella già esistente.           |
| 8     | Eliminazione di una tabella inesistente.         |
| 16    | Aggiornamento di una riga inesistente.           |
| 256   | Mancata corrispondenza delle tabelle codici del database e della trasformazione. |



 

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



