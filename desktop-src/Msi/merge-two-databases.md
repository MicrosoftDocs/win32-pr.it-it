---
description: Il file VBScript WiMerge.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Questo script di esempio unisce uno Windows Installer database in un altro database. Per altre informazioni, vedere unioni e trasformazioni.
ms.assetid: 31867082-7c1d-4530-a066-236d8ee5f023
title: Unire due database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0254cbe2bd0785b45d4ced3a16770023e617bc63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318661"
---
# <a name="merge-two-databases"></a>Unire due database

Il file VBScript WiMerge.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio unisce uno Windows Installer database in un altro database. Per altre informazioni, vedere [unioni e trasformazioni](merges-and-transforms.md).

Non è possibile usare la funzione [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) e il metodo [**merge**](database-merge.md) dell'oggetto di [**database**](database-object.md) per unire un modulo incluso nel pacchetto di installazione. Non devono essere utilizzate per unire i [moduli unione](merge-modules.md) in un pacchetto di Windows Installer. Per includere un modulo merge in un pacchetto di installazione, è necessario che gli autori dei pacchetti di installazione seguano le linee guida descritte nell'argomento [Applying merge modules](applying-merge-modules.md) .

Nell'esempio viene illustrato l'utilizzo degli elementi seguenti:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)
-   [**OpenView (metodo)**](database-openview.md)
-   [**Metodo Merge**](database-merge.md)
-   [**Metodo commit**](database-commit.md) dell' [ **oggetto di database**](database-object.md)
-   [**Fetch (metodo)**](view-fetch.md)
-   [**Oggetto View**](view-object.md)
-   [**Proprietà StringData**](record-stringdata.md) dell' [ **oggetto record**](record-object.md)

Per usare questo esempio, è necessario disporre della versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ percorso del file \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiMerge.vbs \[ percorso al percorso del database \] \[ per il \] nome della tabella di database importato \[\]**

Consente di specificare il percorso del database di Windows Installer che riceve il merge. Consente di specificare il percorso del database importato nella prima. È possibile specificare un nome facoltativo per una tabella che contenga gli errori di Unione. Se non viene specificato alcun nome di tabella, il programma di installazione usa il nome \_ MergeErrors e rilascia la tabella dopo la visualizzazione del contenuto.

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



