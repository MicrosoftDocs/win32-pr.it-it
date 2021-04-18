---
description: Il file VBScript WiLstScr.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Questo script di esempio illustra il Visualizzatore di script Windows Installer.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Visualizza script del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308664"
---
# <a name="view-installer-script"></a>Visualizza script del programma di installazione

Il file VBScript WiLstScr.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio illustra il Visualizzatore di script Windows Installer.

Nell'esempio viene illustrato l'utilizzo di:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   Metodo [**LastErrorRecord**](installer-lasterrorrecord.md) dell'oggetto [**Installer**](installer-object.md)
-   Metodo [**OpenView**](database-openview.md) dell'oggetto di [**database**](database-object.md)
-   Metodo [**Fetch**](view-fetch.md) dell'oggetto [**View**](view-object.md)
-   Metodo [**FormatText**](record-formattext.md)
-   Proprietà [**FieldCount**](record-fieldcount.md)
-   Proprietà [**StringData**](record-stringdata.md) dell'oggetto [**record**](record-object.md)
-   [\_Tabella transformview](-transformview-table.md)

Per usare questo esempio è necessaria la versione CScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiLstScr.vbs** *\[ percorso Windows Installer script \] di esecuzione*

Specificare il percorso dello script di esecuzione del programma di installazione.

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



