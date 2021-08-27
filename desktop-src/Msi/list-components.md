---
description: Il file VBScript WiCompon.vbs disponibile in Windows SDK Components for Windows Installer Developers. Questo script di esempio può essere usato per elencare i componenti in un database Windows Installer.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Elencare i componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec396e66ed55d78131c74b85432b2f01829cdb5400fc5c00a6ced5725edadeae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129321"
---
# <a name="list-components"></a>Elencare i componenti

Il file VBScript WiCompon.vbs in Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio può essere usato per elencare i componenti in un database Windows Installer.

In questo esempio viene illustrato l'utilizzo della chiave primaria nella [tabella Component](component-table.md).

L'esempio illustra anche:

-   [**Metodo OpenDatabase (oggetto Installer),**](installer-opendatabase.md) [**metodo CreateRecord**](installer-createrecord.md)e [**metodo LastErrorRecord**](installer-lasterrorrecord.md) dell'oggetto [**Installer.**](installer-object.md)
-   [**Metodo OpenView**](database-openview.md), [**proprietà TablePersistent**](database-tablepersistent.md)e [**proprietà PrimaryKeys**](database-primarykeys.md) dell'oggetto [**di database**](database-object.md).
-   [**Metodo Execute**](view-execute.md) e metodo [**Fetch dell'oggetto**](view-fetch.md) [**View.**](view-object.md)
-   [**Proprietà StringData**](record-stringdata.md) dell'oggetto [**Record.**](record-object.md)

L'uso di questo esempio richiede CScript.exe o WScript.exe versione di Windows Script Host. Per usare CScript.exe eseguire questo esempio, digitare un comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con vbs > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script non riesce.

**cscript WiCompon.vbs \[ al nome del componente di \] \[ database\]**

Specificare il percorso del database Windows Installer. Specificare il nome del componente. Il nome deve essere elencato nella colonna Componente della [tabella Componente](component-table.md). Se il nome del componente viene omesso, vengono elencati tutti i componenti. Se come nome del componente viene usato un asterisco ( \* ), WiCompon.vbs la composizione di tutti i componenti. Si noti che i database di grandi dimensioni vengono visualizzati meglio usando CScript anziché WScript.

Per altri esempi di scripting, vedere Windows [di script del](windows-installer-scripting-examples.md)programma di installazione . Per le utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 



