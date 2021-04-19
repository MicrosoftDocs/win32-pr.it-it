---
description: Le versioni in lingua localizzata della tabella degli errori e della tabella ActionText sono fornite da Windows Installer SDK. Le versioni in lingua francese di queste tabelle, Error. FRA e ActionTe. FRA, si trovano nella cartella Intl del Windows Installer SDK.
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: Importazione delle tabelle ActionText e degli errori localizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d48a68ca1053a1a1c66899a17802ac337c3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314786"
---
# <a name="importing-localized-error-and-actiontext-tables"></a>Importazione delle tabelle ActionText e degli errori localizzati

Le versioni in lingua localizzata della [tabella degli errori](error-table.md) e della [tabella ActionText](actiontext-table.md) sono fornite da Windows Installer SDK. Le versioni in lingua francese di queste tabelle, Error. FRA e ActionTe. FRA, si trovano nella cartella Intl del Windows Installer SDK.

È possibile utilizzare l'Editor tabella Orca o l'utilità Msidb.exe fornita con l'SDK per importare le versioni in francese di queste tabelle nel database.

Un esempio di utilizzo di [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) e del [**Metodo Import**](database-import.md) dell' [**oggetto di database**](database-object.md) viene fornito in Windows Installer SDK come WiImport.vbs di utilità. Il frammento di codice seguente, Imp.vbs, illustra anche l'uso del metodo Import ed è da usare con Windows script host.


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



Per importare e sostituire la tabella degli errori con Error. FRA è possibile utilizzare una riga di comando simile alla seguente.

**Cscript Imp.vbs MNPFren.msi C: \\ Nota il \_ programma di installazione \\ francese Error. fra**

Per importare e sostituire la tabella ActionText con ActionTe. FRA, è possibile usare una riga di comando simile alla seguente.

**Cscript Imp.vbs MNPFren.msi C: \\ Note \_ Installer \\ francese ActionTe. fra**

Eseguire di nuovo la convalida in MNPFren.msi come descritto in [convalida di un aggiornamento dell'installazione](validating-an-installation-upgrade.md).

[Continua](localizing-database-columns.md)

 

 



