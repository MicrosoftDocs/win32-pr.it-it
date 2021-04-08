---
description: Il file VBScript WiFilVer.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Nell'esempio viene illustrato come utilizzare uno script per segnalare o aggiornare la versione del file, le dimensioni e le informazioni sulla lingua.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Gestire le dimensioni e le versioni dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752775"
---
# <a name="manage-file-sizes-and-versions"></a><span data-ttu-id="5e6ab-104">Gestire le dimensioni e le versioni dei file</span><span class="sxs-lookup"><span data-stu-id="5e6ab-104">Manage File Sizes and Versions</span></span>

<span data-ttu-id="5e6ab-105">Il file VBScript WiFilVer.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="5e6ab-105">The VBScript file WiFilVer.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="5e6ab-106">Nell'esempio viene illustrato come utilizzare uno script per segnalare o aggiornare la versione del file, le dimensioni e le informazioni sulla lingua.</span><span class="sxs-lookup"><span data-stu-id="5e6ab-106">The sample shows you how you can use a script to report or update the file version, size, and language information.</span></span>

<span data-ttu-id="5e6ab-107">Nell'esempio vengono inoltre illustrate le azioni Windows Installer, le modalità di accesso a un database Windows Installer e l'utilizzo degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5e6ab-107">The sample also shows you Windows Installer actions, how to access a Windows Installer database, and the use of the following:</span></span>

-   <span data-ttu-id="5e6ab-108">Metodo [**Installer. OpenDatabase**](installer-opendatabase.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="5e6ab-108">[**Installer.OpenDatabase**](installer-opendatabase.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="5e6ab-109">Proprietà [**Installer. FileAttributes**](installer-fileattributes.md)</span><span class="sxs-lookup"><span data-stu-id="5e6ab-109">[**Installer.FileAttributes**](installer-fileattributes.md) property</span></span>
-   <span data-ttu-id="5e6ab-110">[**Installer. filehash**](installer-filehash.md) (metodo)</span><span class="sxs-lookup"><span data-stu-id="5e6ab-110">[**Installer.FileHash**](installer-filehash.md) method</span></span>
-   <span data-ttu-id="5e6ab-111">[**Installer. FileVersion**](installer-fileversion.md) (metodo)</span><span class="sxs-lookup"><span data-stu-id="5e6ab-111">[**Installer.FileVersion**](installer-fileversion.md) method</span></span>
-   <span data-ttu-id="5e6ab-112">Metodo [**Installer. LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="5e6ab-112">[**Installer.LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="5e6ab-113">Metodo [**database. OpenView**](database-openview.md)</span><span class="sxs-lookup"><span data-stu-id="5e6ab-113">[**Database.OpenView**](database-openview.md) method</span></span>
-   <span data-ttu-id="5e6ab-114">Proprietà [**database. SummaryInformation**](database-summaryinformation.md) dell' [ **oggetto di database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="5e6ab-114">[**Database.SummaryInformation**](database-summaryinformation.md) property of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="5e6ab-115">[**Session. DoAction,**](session-doaction.md) metodo</span><span class="sxs-lookup"><span data-stu-id="5e6ab-115">[**Session.DoAction**](session-doaction.md) method</span></span>
-   [<span data-ttu-id="5e6ab-116">**Session. Property**</span><span class="sxs-lookup"><span data-stu-id="5e6ab-116">**Session.Property**</span></span>](session-session.md)
-   <span data-ttu-id="5e6ab-117">Proprietà [**Session. SourcePath**](session-sourcepath.md)</span><span class="sxs-lookup"><span data-stu-id="5e6ab-117">[**Session.SourcePath**](session-sourcepath.md) property</span></span>
-   <span data-ttu-id="5e6ab-118">Proprietà [**Session. Mode**](session-mode.md) dell' [ **oggetto Session**](session-object.md)</span><span class="sxs-lookup"><span data-stu-id="5e6ab-118">[**Session.Mode**](session-mode.md) property of the [**Session Object**](session-object.md)</span></span>
-   <span data-ttu-id="5e6ab-119">Proprietà [**record. StringData**](record-stringdata.md)</span><span class="sxs-lookup"><span data-stu-id="5e6ab-119">[**Record.StringData**](record-stringdata.md) property</span></span>
-   <span data-ttu-id="5e6ab-120">Proprietà [**record. IntegerData**](record-integerdata.md) dell' [ **oggetto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="5e6ab-120">[**Record.IntegerData**](record-integerdata.md) property of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="5e6ab-121">Per usare questo esempio è necessaria la versione CScript.exe o WScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="5e6ab-121">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="5e6ab-122">Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="5e6ab-122">To use CScript.exe to run this sample, type a command at the command prompt by using the following syntax:</span></span>

<span data-ttu-id="5e6ab-123">**cscript WiFilVer.vbs \[ percorso di \] \[ origine facoltativo del database\]**</span><span class="sxs-lookup"><span data-stu-id="5e6ab-123">**cscript WiFilVer.vbs \[path to database\]\[optional source locations\]**</span></span>

<span data-ttu-id="5e6ab-124">Tenere inoltre presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="5e6ab-124">Also be aware of the following:</span></span>

-   <span data-ttu-id="5e6ab-125">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="5e6ab-125">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="5e6ab-126">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="5e6ab-126">or if too few arguments are specified.</span></span>
-   <span data-ttu-id="5e6ab-127">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .</span><span class="sxs-lookup"><span data-stu-id="5e6ab-127">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span>
-   <span data-ttu-id="5e6ab-128">L'esempio restituisce un valore pari a 0 (zero) per esito positivo, 1 (uno) se la guida viene richiamata e 2 (due) se lo script non riesce.</span><span class="sxs-lookup"><span data-stu-id="5e6ab-128">The sample returns a value of 0 (zero) for success, 1 (one) if help is invoked, and 2 (two) if the script fails.</span></span>

<span data-ttu-id="5e6ab-129">Specificare il database di Windows Installer che si desidera aggiornare, che deve trovarsi nella radice del file di origine.</span><span class="sxs-lookup"><span data-stu-id="5e6ab-129">Specify the Windows Installer database that you want to be updated, which must be located at the source file root.</span></span> <span data-ttu-id="5e6ab-130">Tuttavia, è possibile specificare le origini per il database in posizioni separate.</span><span class="sxs-lookup"><span data-stu-id="5e6ab-130">However, you can specify sources for the database at separate locations.</span></span> <span data-ttu-id="5e6ab-131">Se l'origine è compressa, tutti i file vengono aperti alla radice.</span><span class="sxs-lookup"><span data-stu-id="5e6ab-131">If the source is compressed, all the files are opened at the root.</span></span>

<span data-ttu-id="5e6ab-132">È possibile specificare le opzioni seguenti in qualsiasi posizione nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5e6ab-132">The following options can be specified at any location on the command line.</span></span>



| <span data-ttu-id="5e6ab-133">Opzione</span><span class="sxs-lookup"><span data-stu-id="5e6ab-133">Option</span></span>                | <span data-ttu-id="5e6ab-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e6ab-134">Description</span></span>                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e6ab-135">*non è stata specificata alcuna opzione*</span><span class="sxs-lookup"><span data-stu-id="5e6ab-135">*no option specified*</span></span> | <span data-ttu-id="5e6ab-136">Visualizza le informazioni sul file del database.</span><span class="sxs-lookup"><span data-stu-id="5e6ab-136">Display the file information of the database.</span></span>                                            |
| <span data-ttu-id="5e6ab-137">/U</span><span class="sxs-lookup"><span data-stu-id="5e6ab-137">/u</span></span>                    | <span data-ttu-id="5e6ab-138">Aggiornare le informazioni relative alle dimensioni, alla versione e alla lingua del file nel database dall'origine.</span><span class="sxs-lookup"><span data-stu-id="5e6ab-138">Update the file size, version, and language information in the database from the source.</span></span> |



 

<span data-ttu-id="5e6ab-139">Per ulteriori informazioni, vedere [Windows Installer esempi di script](windows-installer-scripting-examples.md) e [strumenti di sviluppo Windows Installer](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5e6ab-139">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) and [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



