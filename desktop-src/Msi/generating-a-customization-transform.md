---
description: È possibile generare un file di trasformazione utilizzando MsiDatabaseGenerateTransform o il metodo GenerateTransform dell'oggetto di database.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Generazione di una trasformazione di personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f73609b7be60dbfe236d31ed5a865e86ff6e310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314268"
---
# <a name="generating-a-customization-transform"></a><span data-ttu-id="c505a-103">Generazione di una trasformazione di personalizzazione</span><span class="sxs-lookup"><span data-stu-id="c505a-103">Generating a Customization Transform</span></span>

<span data-ttu-id="c505a-104">È possibile generare un file di trasformazione utilizzando [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) o il [**Metodo GenerateTransform**](database-generatetransform.md) dell' [**oggetto di database**](database-object.md).</span><span class="sxs-lookup"><span data-stu-id="c505a-104">You may generate a transform file by using [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) or the [**GenerateTransform method**](database-generatetransform.md) of the [**Database object**](database-object.md).</span></span> <span data-ttu-id="c505a-105">Un esempio è fornito in Windows Installer SDK come WiGenXfm.vbs di utilità.</span><span class="sxs-lookup"><span data-stu-id="c505a-105">An example of this is provided in the Windows Installer SDK as the utility WiGenXfm.vbs.</span></span> <span data-ttu-id="c505a-106">Il frammento di codice seguente, Gen.vbs, illustra anche il metodo **GenerateTransform** ed è utilizzabile con Windows script host.</span><span class="sxs-lookup"><span data-stu-id="c505a-106">The following snippet, Gen.vbs, also illustrates the **GenerateTransform** method and is for use with Windows Script Host.</span></span>


```VB
'Gen.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is gen.vbs [original database] [customized database] [transform file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
' Open databases
Dim database1 : Set database1 = 
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 = 
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
' Generate transform
Dim transform : transform = Database2.GenerateTransform(Database1,
    Wscript.Arguments(2))
```



<span data-ttu-id="c505a-107">Per generare il file di trasformazione MNPtrans. MST dal database MNP2000.msi originale e dal database MNP2000t.msi modificato in [personalizzazione di un database originale](customizing-an-original-database.md), passare alla cartella contenente Gen.vbs, il database originale e il database del programma di installazione aggiornato e immettere la riga di comando seguente.</span><span class="sxs-lookup"><span data-stu-id="c505a-107">To generate the transform file MNPtrans.mst from the original MNP2000.msi database and the MNP2000t.msi database you modified in [Customizing an Original Database](customizing-an-original-database.md), change directories to the folder containing Gen.vbs, the original database, and the updated installer database and enter the following command line.</span></span>

<span data-ttu-id="c505a-108">**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**</span><span class="sxs-lookup"><span data-stu-id="c505a-108">**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**</span></span>

[<span data-ttu-id="c505a-109">Continua</span><span class="sxs-lookup"><span data-stu-id="c505a-109">Continue</span></span>](adding-summary-information-to-customization-transform.md)

 

 



