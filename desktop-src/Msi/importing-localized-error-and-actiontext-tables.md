---
description: Le versioni localizzate della tabella Error e della tabella ActionText vengono fornite da Windows Installer SDK. Le versioni in lingua francese di queste tabelle, Error.FRA e ActionTe.FRA, si trovano nella cartella Intl di Windows Installer SDK.
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: Importazione di tabelle Error e ActionText localizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda0916f634d986874cd17f9871fa602277b180e1ba436e9d9786fb061f3ac4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142237"
---
# <a name="importing-localized-error-and-actiontext-tables"></a>Importazione di tabelle Error e ActionText localizzate

Le versioni localizzate della [tabella Error e](error-table.md) della tabella [ActionText](actiontext-table.md) vengono fornite da Windows Installer SDK. Le versioni in lingua francese di queste tabelle, Error.FRA e ActionTe.FRA, si trovano nella cartella Intl di Windows Installer SDK.

È possibile usare l'editor di tabelle Orca o l'utilità Msidb.exe fornita con l'SDK per importare le versioni in francese di queste tabelle nel database.

Un esempio di uso [**di MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) e del metodo [**Import**](database-import.md) dell'oggetto [**Database**](database-object.md) è disponibile in Windows Installer SDK come utilità WiImport.vbs. Il frammento di codice seguente, Imp.vbs, illustra anche l'uso del metodo Import ed è per l'uso con Windows host script.


```VB
'Imp.vbs. Argument(0) is the original database. Argument(1) is the
'    path of the folder containing the file to be imported. Argument(2) is the name of the file to be imported.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is imp.vbs [original database] [folder path] [import file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
Dim databasePath : databasePath = Wscript.Arguments(0)
Dim folder : folder = Wscript.Arguments(1)
 
' Open database and process file
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim table : table = Wscript.Arguments(2)
database.Import folder, table 
 
' Commit database changes
database.Commit 'commit changes
Wscript.Quit 0
```



Per importare e sostituire la tabella Error con Error.FRA, è possibile usare una riga di comando come la seguente.

**Cscript Imp.vbs MNPFren.msi C: \\ Nota Errore francese del programma di \_ \\ installazione.FRA**

Per importare e sostituire la tabella ActionText con ActionTe.FRA, è possibile usare una riga di comando come la seguente.

**Cscript Imp.vbs MNPFren.msi C: \\ Note \_ Installer \\ French ActionTe.FRA**

Eseguire nuovamente la convalida in MNPFren.msi come descritto in [Convalida di un aggiornamento dell'installazione.](validating-an-installation-upgrade.md)

[Continua](localizing-database-columns.md)

 

 



