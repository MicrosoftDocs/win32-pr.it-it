---
description: Il file VBScript WiExport.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Esporta file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309485"
---
# <a name="export-files"></a><span data-ttu-id="390bf-103">Esporta file</span><span class="sxs-lookup"><span data-stu-id="390bf-103">Export Files</span></span>

<span data-ttu-id="390bf-104">Il file VBScript WiExport.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="390bf-104">The VBScript file WiExport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="390bf-105">In questo esempio viene illustrato come scrivere uno script per esportare le tabelle in un database Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="390bf-105">This sample shows how to write script to export tables into a Windows Installer database.</span></span> <span data-ttu-id="390bf-106">L'esempio di script si connette a un oggetto del [**programma di installazione**](installer-object.md) , apre un database ed Esporta le tabelle in file di archivio.</span><span class="sxs-lookup"><span data-stu-id="390bf-106">The script sample connects to an [**Installer**](installer-object.md) object, opens a database and exports tables to archive files.</span></span>

<span data-ttu-id="390bf-107">Nell'esempio viene illustrato l'utilizzo di:</span><span class="sxs-lookup"><span data-stu-id="390bf-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="390bf-108">**Metodo OpenDatabase (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="390bf-108">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="390bf-109">[**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="390bf-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="390bf-110">**Export (metodo)**</span><span class="sxs-lookup"><span data-stu-id="390bf-110">**Export method**</span></span>](database-export.md)
-   <span data-ttu-id="390bf-111">[**Metodo OpenView**](database-openview.md) dell' [ **oggetto di database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="390bf-111">[**OpenView method**](database-openview.md) of the [**Database object**](database-object.md)</span></span>
-   <span data-ttu-id="390bf-112">[**Metodo fetch**](view-fetch.md) dell' [ **oggetto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="390bf-112">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   <span data-ttu-id="390bf-113">[**Proprietà StringData**](record-stringdata.md) dell' [ **oggetto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="390bf-113">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="390bf-114">Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="390bf-114">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="390bf-115">Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="390bf-115">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="390bf-116">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="390bf-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="390bf-117">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="390bf-117">or if too few arguments are specified.</span></span> <span data-ttu-id="390bf-118">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .</span><span class="sxs-lookup"><span data-stu-id="390bf-118">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="390bf-119">Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="390bf-119">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="390bf-120">**cscript WiExport.vbs \[ percorso del percorso del database \] \[ all' \] \[ \] \[ elenco di nomi di tabella Opzioni cartella\]**</span><span class="sxs-lookup"><span data-stu-id="390bf-120">**cscript WiExport.vbs \[path to database\]\[path to folder\]\[options\]\[table name list\]**</span></span>

<span data-ttu-id="390bf-121">Consente di specificare il percorso del database del programma di installazione da cui vengono esportate le tabelle.</span><span class="sxs-lookup"><span data-stu-id="390bf-121">Specify the path to the installer database from which the tables are being exported.</span></span> <span data-ttu-id="390bf-122">Consente di specificare il percorso della cartella in cui devono essere copiati i file di archivio esportati.</span><span class="sxs-lookup"><span data-stu-id="390bf-122">Specify the path to the folder into which the exported archive files are to be copied.</span></span> <span data-ttu-id="390bf-123">Elenca i nomi con distinzione tra maiuscole e minuscole delle [tabelle di database](database-tables.md) esportate.</span><span class="sxs-lookup"><span data-stu-id="390bf-123">List the case-sensitive names of the [database tables](database-tables.md) being exported.</span></span> <span data-ttu-id="390bf-124">Specificare ' \* ' per esportare tutte le tabelle \_ , incluso SummaryInformation.</span><span class="sxs-lookup"><span data-stu-id="390bf-124">Specify '\*' to export all the tables including \_SummaryInformation.</span></span>

<span data-ttu-id="390bf-125">È possibile specificare le opzioni seguenti in qualsiasi punto della riga di comando prima dell'elenco nome tabella.</span><span class="sxs-lookup"><span data-stu-id="390bf-125">The following options may be specified anywhere on the command line before the table name list.</span></span>



| <span data-ttu-id="390bf-126">Opzione</span><span class="sxs-lookup"><span data-stu-id="390bf-126">Option</span></span>              | <span data-ttu-id="390bf-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="390bf-127">Description</span></span>                                            |
|---------------------|--------------------------------------------------------|
| <span data-ttu-id="390bf-128">non è stata specificata alcuna opzione</span><span class="sxs-lookup"><span data-stu-id="390bf-128">no option specified</span></span> | <span data-ttu-id="390bf-129">I file di archivio esportati possono avere un nome file lungo.</span><span class="sxs-lookup"><span data-stu-id="390bf-129">Exported archive files may have a long file name.</span></span>      |
| <span data-ttu-id="390bf-130">/s</span><span class="sxs-lookup"><span data-stu-id="390bf-130">/s</span></span>                  | <span data-ttu-id="390bf-131">Forzare i file di archivio esportati con nomi di file brevi.</span><span class="sxs-lookup"><span data-stu-id="390bf-131">Force exported archive files to have short file names.</span></span> |



 

<span data-ttu-id="390bf-132">Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="390bf-132">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="390bf-133">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="390bf-133">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



