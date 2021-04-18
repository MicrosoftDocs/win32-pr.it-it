---
description: Il file VBScript WiDialog.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. In questo esempio viene illustrato come utilizzare lo script per visualizzare in anteprima le finestre di dialogo in un database Windows Installer.
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: Interfaccia utente di anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7736c442cdfcb22034326ff459eb89fc28b0c9af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313338"
---
# <a name="preview-user-interface"></a>Interfaccia utente di anteprima

Il file VBScript WiDialog.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come utilizzare lo script per visualizzare in anteprima le finestre di dialogo in un database Windows Installer.

Questo esempio dimostra:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md), [**Metodo CreaRecord**](installer-createrecord.md)e [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [**oggetto Installer**](installer-object.md)
-   [**Metodo OpenView**](database-openview.md) e [**Metodo EnableUIpreview**](database-enableuipreview.md) dell'oggetto di [**database**](database-object.md)
-   [**Metodo Execute**](view-execute.md) e [**Metodo fetch**](view-fetch.md) dell' [**oggetto View**](view-object.md)
-   [**Proprietà StringData**](record-stringdata.md) Propertyof [ **oggetto record**](record-object.md)

Questo esempio richiede la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiDialog.vbs** *\[ percorso \] \[ dei nomi \] delle finestre di dialogo del database*

Consente di specificare il percorso di un database Windows Installer. Consente di specificare il nome di una finestra di dialogo. Questo nome deve essere elencato nella colonna finestra di dialogo della [tabella della finestra di dialogo](dialog-table.md). Per visualizzare un tabellone, aggiungere il nome della finestra di dialogo con il nome del controllo dalla [tabella di controllo](control-table.md) e aggiungerlo al nome del Billboard nella [tabella Billboard](billboard-table.md). Se non viene specificata alcuna finestra di dialogo, tutte le finestre di dialogo nella tabella della finestra di dialogo vengono visualizzate in sequenza.

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



