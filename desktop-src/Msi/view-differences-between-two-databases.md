---
description: Il file VBScript WiDiffDb.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Questo script di esempio genera un file di trasformazione temporaneo tra due database Windows Installer e visualizza la trasformazione.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Visualizzare le differenze tra due database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525873"
---
# <a name="view-differences-between-two-databases"></a><span data-ttu-id="43908-104">Visualizzare le differenze tra due database</span><span class="sxs-lookup"><span data-stu-id="43908-104">View Differences Between Two Databases</span></span>

<span data-ttu-id="43908-105">Il file VBScript WiDiffDb.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="43908-105">The VBScript file WiDiffDb.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="43908-106">Questo script di esempio genera un file di trasformazione temporaneo tra due database Windows Installer e visualizza la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="43908-106">This sample script generates a temporary transform file between two Windows Installer databases and displays the transform.</span></span>

<span data-ttu-id="43908-107">Nell'esempio viene illustrato l'utilizzo di:</span><span class="sxs-lookup"><span data-stu-id="43908-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="43908-108">**Metodo OpenDatabase (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="43908-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="43908-109">[**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="43908-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="43908-110">**OpenView (metodo)**</span><span class="sxs-lookup"><span data-stu-id="43908-110">**OpenView method**</span></span>](database-openview.md)
-   [<span data-ttu-id="43908-111">**Proprietà SummaryInformation (oggetto di database)**</span><span class="sxs-lookup"><span data-stu-id="43908-111">**SummaryInformation property (Database Object)**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="43908-112">**Metodo GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="43908-112">**GenerateTransform method**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="43908-113">**Metodo ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="43908-113">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="43908-114">**Oggetto di database**</span><span class="sxs-lookup"><span data-stu-id="43908-114">**Database object**</span></span>](database-object.md)
-   <span data-ttu-id="43908-115">[**Metodo fetch**](view-fetch.md) dell' [ **oggetto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="43908-115">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="43908-116">**Proprietà IsNull**</span><span class="sxs-lookup"><span data-stu-id="43908-116">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="43908-117">[**Proprietà StringData**](record-stringdata.md) dell' [ **oggetto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="43908-117">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>
-   [<span data-ttu-id="43908-118">\_Tabella transformview</span><span class="sxs-lookup"><span data-stu-id="43908-118">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="43908-119">Per usare questo esempio è necessaria la versione CScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="43908-119">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="43908-120">Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="43908-120">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="43908-121">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="43908-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="43908-122">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="43908-122">or if too few arguments are specified.</span></span> <span data-ttu-id="43908-123">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .</span><span class="sxs-lookup"><span data-stu-id="43908-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="43908-124">Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="43908-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="43908-125">**cscript WiDiffDb.vbs** *\[ percorso del database originale \] \[ al database \] modificato*</span><span class="sxs-lookup"><span data-stu-id="43908-125">**cscript WiDiffDb.vbs** *\[path to original database\]\[path to revised database\]*</span></span>

<span data-ttu-id="43908-126">Consente di specificare il percorso del database di Windows Installer originale.</span><span class="sxs-lookup"><span data-stu-id="43908-126">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="43908-127">Consente di specificare il percorso del database modificato.</span><span class="sxs-lookup"><span data-stu-id="43908-127">Specify the path to the revised database.</span></span> <span data-ttu-id="43908-128">Lo script di esempio visualizzerà la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="43908-128">The sample script will display the transform.</span></span>

<span data-ttu-id="43908-129">Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="43908-129">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="43908-130">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="43908-130">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



