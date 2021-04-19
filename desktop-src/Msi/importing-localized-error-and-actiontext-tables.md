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
# <a name="importing-localized-error-and-actiontext-tables"></a><span data-ttu-id="72091-104">Importazione delle tabelle ActionText e degli errori localizzati</span><span class="sxs-lookup"><span data-stu-id="72091-104">Importing Localized Error and ActionText Tables</span></span>

<span data-ttu-id="72091-105">Le versioni in lingua localizzata della [tabella degli errori](error-table.md) e della [tabella ActionText](actiontext-table.md) sono fornite da Windows Installer SDK.</span><span class="sxs-lookup"><span data-stu-id="72091-105">Localized language versions of the [Error table](error-table.md) and [ActionText table](actiontext-table.md) are provided by the Windows Installer SDK.</span></span> <span data-ttu-id="72091-106">Le versioni in lingua francese di queste tabelle, Error. FRA e ActionTe. FRA, si trovano nella cartella Intl del Windows Installer SDK.</span><span class="sxs-lookup"><span data-stu-id="72091-106">The French language versions of these tables, Error.FRA and ActionTe.FRA, are located in the Intl folder of the Windows Installer SDK.</span></span>

<span data-ttu-id="72091-107">È possibile utilizzare l'Editor tabella Orca o l'utilità Msidb.exe fornita con l'SDK per importare le versioni in francese di queste tabelle nel database.</span><span class="sxs-lookup"><span data-stu-id="72091-107">You may use the table editor Orca or the utility Msidb.exe provided with the SDK to import the French versions of these tables into the database.</span></span>

<span data-ttu-id="72091-108">Un esempio di utilizzo di [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) e del [**Metodo Import**](database-import.md) dell' [**oggetto di database**](database-object.md) viene fornito in Windows Installer SDK come WiImport.vbs di utilità.</span><span class="sxs-lookup"><span data-stu-id="72091-108">An example of using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) and the [**Import Method**](database-import.md) of the [**Database object**](database-object.md) is provided in the Windows Installer SDK as the utility WiImport.vbs.</span></span> <span data-ttu-id="72091-109">Il frammento di codice seguente, Imp.vbs, illustra anche l'uso del metodo Import ed è da usare con Windows script host.</span><span class="sxs-lookup"><span data-stu-id="72091-109">The following snippet, Imp.vbs, also illustrates the use of the Import method and is for use with Windows Script Host.</span></span>


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



<span data-ttu-id="72091-110">Per importare e sostituire la tabella degli errori con Error. FRA è possibile utilizzare una riga di comando simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="72091-110">To import and replace the Error table with Error.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="72091-111">**Cscript Imp.vbs MNPFren.msi C: \\ Nota il \_ programma di installazione \\ francese Error. fra**</span><span class="sxs-lookup"><span data-stu-id="72091-111">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French Error.FRA**</span></span>

<span data-ttu-id="72091-112">Per importare e sostituire la tabella ActionText con ActionTe. FRA, è possibile usare una riga di comando simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="72091-112">To import and replace the ActionText table with ActionTe.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="72091-113">**Cscript Imp.vbs MNPFren.msi C: \\ Note \_ Installer \\ francese ActionTe. fra**</span><span class="sxs-lookup"><span data-stu-id="72091-113">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French ActionTe.FRA**</span></span>

<span data-ttu-id="72091-114">Eseguire di nuovo la convalida in MNPFren.msi come descritto in [convalida di un aggiornamento dell'installazione](validating-an-installation-upgrade.md).</span><span class="sxs-lookup"><span data-stu-id="72091-114">Rerun validation on MNPFren.msi as described in [Validating an Installation Upgrade](validating-an-installation-upgrade.md).</span></span>

[<span data-ttu-id="72091-115">Continua</span><span class="sxs-lookup"><span data-stu-id="72091-115">Continue</span></span>](localizing-database-columns.md)

 

 



