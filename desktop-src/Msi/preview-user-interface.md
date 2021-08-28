---
description: Il file VBScript WiDialog.vbs è disponibile in componenti sdk Windows per Windows programma di installazione. Questo esempio illustra come usare lo script per visualizzare in anteprima le finestre di dialogo in un database Windows Installer.
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: Anteprima Interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572ab444cc2f6acb6ec426f842318201187336121aa9c2a0557fca8cab94a3ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074711"
---
# <a name="preview-user-interface"></a>Anteprima Interfaccia utente

Il file VBScript WiDialog.vbs è disponibile in componenti dell'SDK Windows per [Windows programma di installazione.](platform-sdk-components-for-windows-installer-developers.md) Questo esempio illustra come usare lo script per visualizzare in anteprima le finestre di dialogo in un database Windows Installer.

Questo esempio dimostra:

-   [**Metodo OpenDatabase (oggetto Installer),**](installer-opendatabase.md) [**metodo CreateRecord**](installer-createrecord.md)e [**metodo LastErrorRecord**](installer-lasterrorrecord.md) dell'oggetto [**Installer**](installer-object.md)
-   [**Metodo OpenView**](database-openview.md) e [**metodo EnableUIpreview**](database-enableuipreview.md) dell'oggetto [**database**](database-object.md)
-   [**Metodo Execute**](view-execute.md) e [**metodo Fetch dell'oggetto**](view-fetch.md) [**View**](view-object.md)
-   [**Proprietà StringData**](record-stringdata.md) dell'oggetto [ **Record**](record-object.md)

Questo esempio richiede la versione CScript.exe o WScript.exe di Windows Script Host. Per usare CScript.exe per questo esempio, digitare un comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . L'esempio restituisce il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script ha esito negativo.

**cscript WiDialog.vbs** *\[ del database Nomi delle finestre \] \[ di dialogo \]*

Specificare il percorso di un database Windows Installer. Specificare il nome di una finestra di dialogo. Questo nome deve essere elencato nella colonna Dialog della [tabella Dialog](dialog-table.md). Per visualizzare un manifesto pubblicitario, aggiungere il nome della finestra di dialogo con il nome del controllo dalla tabella [Controllo](control-table.md) e accoda questo nome al nome del manifesto nella tabella [Del manifesto](billboard-table.md). Se non viene specificato alcun dialogo, tutti i dialoghe nella tabella Dialog vengono visualizzati in sequenza.

Per altri esempi di scripting, vedere Windows [di scripting del programma di installazione](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 



