---
description: Il file VBScript WiDiffDb.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Questo script di esempio genera un file di trasformazione temporaneo tra due database Windows Installer e visualizza la trasformazione.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Visualizzare le differenze tra due database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525873"
---
# <a name="view-differences-between-two-databases"></a>Visualizzare le differenze tra due database

Il file VBScript WiDiffDb.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio genera un file di trasformazione temporaneo tra due database Windows Installer e visualizza la trasformazione.

Nell'esempio viene illustrato l'utilizzo di:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)
-   [**OpenView (metodo)**](database-openview.md)
-   [**Proprietà SummaryInformation (oggetto di database)**](database-summaryinformation.md)
-   [**Metodo GenerateTransform**](database-generatetransform.md)
-   [**Metodo ApplyTransform**](database-applytransform.md)
-   [**Oggetto di database**](database-object.md)
-   [**Metodo fetch**](view-fetch.md) dell' [ **oggetto View**](view-object.md)
-   [**Proprietà IsNull**](record-isnull.md)
-   [**Proprietà StringData**](record-stringdata.md) dell' [ **oggetto record**](record-object.md)
-   [\_Tabella transformview](-transformview-table.md)

Per usare questo esempio è necessaria la versione CScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiDiffDb.vbs** *\[ percorso del database originale \] \[ al database \] modificato*

Consente di specificare il percorso del database di Windows Installer originale. Consente di specificare il percorso del database modificato. Lo script di esempio visualizzerà la trasformazione.

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



