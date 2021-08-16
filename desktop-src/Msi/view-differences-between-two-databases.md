---
description: Il file VBScript WiDiffDb.vbs disponibile in Windows SDK Components for Windows Installer Developers. Questo script di esempio genera un file di trasformazione temporaneo tra due database Windows Installer e visualizza la trasformazione.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Visualizzare le differenze tra due database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbb04ad6ed1ecaa9d4d5be73708c5edc7dc8c84c9fe230a3725f971d949d335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375914"
---
# <a name="view-differences-between-two-databases"></a>Visualizzare le differenze tra due database

Il file VBScript WiDiffDb.vbs in Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio genera un file di trasformazione temporaneo tra due database Windows Installer e visualizza la trasformazione.

L'esempio illustra l'uso di:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) [ **dell'oggetto Installer**](installer-object.md)
-   [**Metodo OpenView**](database-openview.md)
-   [**Proprietà SummaryInformation (oggetto Database)**](database-summaryinformation.md)
-   [**Metodo GenerateTransform**](database-generatetransform.md)
-   [**Metodo ApplyTransform**](database-applytransform.md)
-   [**Oggetto di database**](database-object.md)
-   [**Metodo Fetch**](view-fetch.md) [ **dell'oggetto View**](view-object.md)
-   [**Proprietà IsNull**](record-isnull.md)
-   [**Proprietà StringData**](record-stringdata.md) [ **dell'oggetto Record**](record-object.md)
-   [\_Tabella TransformView](-transformview-table.md)

L'uso di questo esempio richiede CScript.exe versione di Windows Host script. Per usare CScript.exe eseguire questo esempio, digitare un comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con vbs > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script non riesce.

**cscript WiDiffDb.vbs** *\[ percorso del database originale al \] \[ database modificato \]*

Specificare il percorso del database Windows Installer. Specificare il percorso del database modificato. Lo script di esempio visualizza la trasformazione.

Per altri esempi di scripting, vedere Windows [di script del](windows-installer-scripting-examples.md)programma di installazione . Per le utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 



