---
description: È possibile archiviare la trasformazione personalizzazione in una risorsa di archiviazione del pacchetto di Windows Installer per garantire che la trasformazione sia sempre disponibile quando è disponibile il pacchetto di installazione.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Incorporamento di trasformazioni di personalizzazione come sottoarchivio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313349"
---
# <a name="embedding-customization-transforms-as-substorage"></a><span data-ttu-id="82e95-103">Incorporamento di trasformazioni di personalizzazione come sottoarchivio</span><span class="sxs-lookup"><span data-stu-id="82e95-103">Embedding Customization Transforms as Substorage</span></span>

<span data-ttu-id="82e95-104">È possibile archiviare la trasformazione personalizzazione in una risorsa di archiviazione del pacchetto di Windows Installer per garantire che la trasformazione sia sempre disponibile quando è disponibile il pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="82e95-104">You may store the customization transform in a storage of the Windows Installer package to guarantee that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="82e95-105">Vedere [trasformazioni incorporate](embedded-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="82e95-105">See [Embedded Transforms](embedded-transforms.md).</span></span> <span data-ttu-id="82e95-106">Un esempio è fornito in Windows Installer SDK come WiSubStg.vbs di utilità.</span><span class="sxs-lookup"><span data-stu-id="82e95-106">An example of this is provided in the Windows Installer SDK as the utility WiSubStg.vbs.</span></span> <span data-ttu-id="82e95-107">Il frammento di codice seguente, Emb.vbs, illustra anche l'uso della [tabella Storages](-storages-table.md) per aggiungere una trasformazione incorporata e deve essere usata con Windows script host.</span><span class="sxs-lookup"><span data-stu-id="82e95-107">The following snippet, Emb.vbs, also illustrates the use of the [Storages table](-storages-table.md) to add an embedded transform and is for use with Windows Script Host.</span></span>


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



<span data-ttu-id="82e95-108">Per aggiungere una risorsa di archiviazione denominata MNPtrans1 a MNP2000.msi e contenente la trasformazione creata in [aggiunta di informazioni di riepilogo alla trasformazione personalizzazione](adding-summary-information-to-customization-transform.md), passare alla cartella contenente Emb.vbs, il database originale e il file di trasformazione, quindi immettere la riga di comando seguente.</span><span class="sxs-lookup"><span data-stu-id="82e95-108">To add a storage named MNPtrans1 to MNP2000.msi, and containing the transform you created in [Adding Summary Information to Customization Transform](adding-summary-information-to-customization-transform.md), change directories to the folder containing Emb.vbs, the original database, and the transform file, then enter the following command line.</span></span>

<span data-ttu-id="82e95-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans. MST MNPtrans1**</span><span class="sxs-lookup"><span data-stu-id="82e95-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans.mst MNPtrans1**</span></span>

<span data-ttu-id="82e95-110">Questa operazione completa l'esempio di trasformazione della personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="82e95-110">This completes the customization transform example.</span></span> <span data-ttu-id="82e95-111">Dopo aver incorporato la trasformazione in MNPtrans. MST, la trasformazione è sempre disponibile con il pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="82e95-111">After embedding the transform in MNPtrans.mst, the transform is always available with the installation package.</span></span> <span data-ttu-id="82e95-112">Non è necessario che il file MNPtrans. MST si trovi nell'origine per applicare la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="82e95-112">The file MNPtrans.mst does not need to be located at the source to apply the transform.</span></span>

<span data-ttu-id="82e95-113">Rimuovere MNPtrans. MST dalla cartella che contiene il pacchetto di installazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="82e95-113">Remove MNPtrans.mst from the folder containing the sample installation package.</span></span> <span data-ttu-id="82e95-114">Fare clic sull'icona MNP2000.msi per avviare un'installazione o utilizzare la riga di comando seguente.</span><span class="sxs-lookup"><span data-stu-id="82e95-114">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="82e95-115">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="82e95-115">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="82e95-116">Si noti che in questo modo viene installato il prodotto senza le personalizzazioni.</span><span class="sxs-lookup"><span data-stu-id="82e95-116">Note that this installs the product without the customizations.</span></span> <span data-ttu-id="82e95-117">Per eseguire l'installazione con le personalizzazioni, immettere la riga di comando seguente.</span><span class="sxs-lookup"><span data-stu-id="82e95-117">To install with the customizations, enter the following command line.</span></span> <span data-ttu-id="82e95-118">Usare i due punti per indicare che il valore della proprietà [**TRANSforms**](transforms.md) si riferisce a una trasformazione incorporata.</span><span class="sxs-lookup"><span data-stu-id="82e95-118">Use a colon to indicate that the value of the [**TRANSFORMS**](transforms.md) Property refers to an embedded transform.</span></span>

<span data-ttu-id="82e95-119">msiexec/i MNP2000.msi Transforms =: MNPtrans1</span><span class="sxs-lookup"><span data-stu-id="82e95-119">msiexec /i MNP2000.msi TRANSFORMS=:MNPtrans1</span></span>

<span data-ttu-id="82e95-120">Si noti che la funzionalità di controllo non viene visualizzata nell'albero di selezione delle funzionalità e che i componenti della funzionalità Gate non sono installati anche se nell'interfaccia utente è selezionato un tipo di installazione completo.</span><span class="sxs-lookup"><span data-stu-id="82e95-120">Note that the Gate feature does not appear in the feature selection tree and that the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

## <a name="next-example"></a><span data-ttu-id="82e95-121">Esempio successivo</span><span class="sxs-lookup"><span data-stu-id="82e95-121">Next example</span></span>

[<span data-ttu-id="82e95-122">Un piccolo esempio di patch di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="82e95-122">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

 

 



