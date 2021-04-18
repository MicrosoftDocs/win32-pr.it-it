---
description: Per applicare la trasformazione personalizzazione durante un'installazione del prodotto, è necessario aggiungere un flusso di informazioni di riepilogo al file di trasformazione MNPtrans. MST generato durante la generazione di una trasformazione di personalizzazione.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Aggiunta di informazioni di riepilogo alla trasformazione personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64957fcf8f29ab8793517015c7018292ba9a6e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311076"
---
# <a name="adding-summary-information-to-customization-transform"></a><span data-ttu-id="04d41-103">Aggiunta di informazioni di riepilogo alla trasformazione personalizzazione</span><span class="sxs-lookup"><span data-stu-id="04d41-103">Adding Summary Information to Customization Transform</span></span>

<span data-ttu-id="04d41-104">Per applicare la trasformazione personalizzazione durante un'installazione del prodotto, è necessario aggiungere un [flusso di informazioni di riepilogo](summary-information-stream.md) al file di trasformazione MNPtrans. MST generato durante la generazione di [una trasformazione di personalizzazione](generating-a-customization-transform.md).</span><span class="sxs-lookup"><span data-stu-id="04d41-104">To apply the customization transform during an installation of the product, you must add a [Summary Information Stream](summary-information-stream.md) to the transform file MNPtrans.mst generated in [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

<span data-ttu-id="04d41-105">È possibile generare informazioni di riepilogo per una trasformazione utilizzando [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) o il [**Metodo CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md).</span><span class="sxs-lookup"><span data-stu-id="04d41-105">You may generate summary information for a transform using [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) or the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md).</span></span> <span data-ttu-id="04d41-106">Il frammento di codice seguente, Sum.vbs, illustra il [**Metodo CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) ed è utilizzabile con Windows script host.</span><span class="sxs-lookup"><span data-stu-id="04d41-106">The following snippet, Sum.vbs, illustrates the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md) and is for use with Windows Script Host.</span></span> <span data-ttu-id="04d41-107">Si noti che in questo esempio non viene eseguita alcuna convalida e non vengono evitate condizioni di errore.</span><span class="sxs-lookup"><span data-stu-id="04d41-107">Note that this example performs no validation and suppresses no error conditions.</span></span>


```VB
'Sum.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is sum.vbs [original database] [customized database] [transform]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
 
' Open databases and transform 
Dim database1 : Set database1 =
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 =
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
Dim transform : transform = Wscript.Arguments(2)
 
' Create and add Summary Information
Dim transinfo : transinfo =
    Database2.CreateTransformSummaryInfo(Database1, transform,0,0)
```



<span data-ttu-id="04d41-108">Per creare e aggiungere informazioni di riepilogo al file di trasformazione MNPtrans. MST creato durante la [generazione di una trasformazione di personalizzazione](generating-a-customization-transform.md), passare alla cartella contenente Gen.vbs, il database originale, il database aggiornato e la trasformazione, quindi immettere la riga di comando seguente.</span><span class="sxs-lookup"><span data-stu-id="04d41-108">To create and add summary information to the transform file MNPtrans.mst you created in [Generating a Customization Transform](generating-a-customization-transform.md), change directories to the folder containing Gen.vbs, the original database, the updated database, and the transform, and enter the following command line.</span></span>

<span data-ttu-id="04d41-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**</span><span class="sxs-lookup"><span data-stu-id="04d41-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**</span></span>

<span data-ttu-id="04d41-110">Fare clic sull'icona MNP2000.msi per avviare un'installazione o utilizzare la riga di comando seguente.</span><span class="sxs-lookup"><span data-stu-id="04d41-110">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="04d41-111">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="04d41-111">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="04d41-112">Il prodotto verrà installato senza le personalizzazioni.</span><span class="sxs-lookup"><span data-stu-id="04d41-112">This installs the product without the customizations.</span></span> <span data-ttu-id="04d41-113">Per eseguire l'installazione con la personalizzazione, immettere la riga di comando seguente.</span><span class="sxs-lookup"><span data-stu-id="04d41-113">To install with the customization, enter the following command line.</span></span> <span data-ttu-id="04d41-114">Si noti che il valore della proprietà [**TRANSforms**](transforms.md) si riferisce al file di trasformazione situato nell'origine.</span><span class="sxs-lookup"><span data-stu-id="04d41-114">Note that the value of the [**TRANSFORMS**](transforms.md) Property refers to transform file located at the source.</span></span>

<span data-ttu-id="04d41-115">**msiexec/i MNP2000.msi Transforms = MNPtrans. MST**</span><span class="sxs-lookup"><span data-stu-id="04d41-115">**msiexec /i MNP2000.msi TRANSFORMS=MNPtrans.mst**</span></span>

<span data-ttu-id="04d41-116">La funzionalità di controllo non viene visualizzata nell'albero di selezione delle funzionalità e i componenti della funzionalità di controllo non vengono installati anche se nell'interfaccia utente è selezionato un tipo completo di installazione.</span><span class="sxs-lookup"><span data-stu-id="04d41-116">The Gate feature does not appear in the feature selection tree and the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

[<span data-ttu-id="04d41-117">Continua</span><span class="sxs-lookup"><span data-stu-id="04d41-117">Continue</span></span>](embedding-customization-transforms-as-substorage.md)

 

 



