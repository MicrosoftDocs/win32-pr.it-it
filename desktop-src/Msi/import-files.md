---
description: Il file VBScript WiImport.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. In questo esempio viene illustrato come scrivere uno script per importare le tabelle in un database Windows Installer.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importa file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308903"
---
# <a name="import-files"></a><span data-ttu-id="b8944-104">Importa file</span><span class="sxs-lookup"><span data-stu-id="b8944-104">Import Files</span></span>

<span data-ttu-id="b8944-105">Il file VBScript WiImport.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="b8944-105">The VBScript file WiImport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="b8944-106">In questo esempio viene illustrato come scrivere uno script per importare le tabelle in un database Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b8944-106">This sample shows how to write a script to import tables into a Windows Installer database.</span></span>

<span data-ttu-id="b8944-107">Lo script si connette a un oggetto del [**programma di installazione**](installer-object.md) , apre un database, elabora un elenco di file ed esegue il commit delle modifiche prima di chiudere il database.</span><span class="sxs-lookup"><span data-stu-id="b8944-107">The script connects to an [**Installer**](installer-object.md) object, opens a database, processes a list of files, and commits the changes before closing the database.</span></span>

<span data-ttu-id="b8944-108">Nell'esempio viene illustrato l'utilizzo di:</span><span class="sxs-lookup"><span data-stu-id="b8944-108">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="b8944-109">**Metodo OpenDatabase (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="b8944-109">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="b8944-110">[**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="b8944-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="b8944-111">**Metodo Import**</span><span class="sxs-lookup"><span data-stu-id="b8944-111">**Import method**</span></span>](database-import.md)
-   <span data-ttu-id="b8944-112">[**Metodo commit**](database-commit.md) dell' [ **oggetto di database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="b8944-112">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="b8944-113">Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="b8944-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="b8944-114">Per utilizzare CScript.exe per eseguire l'esempio, utilizzare la sintassi seguente al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="b8944-114">To use CScript.exe to run this sample, use the following syntax at the command prompt.</span></span>

<span data-ttu-id="b8944-115">**cscript WiImport.vbs \[ percorso del percorso del database \] \[ all' \] \[ \] \[ elenco dei file di archivio delle opzioni della cartella**\]</span><span class="sxs-lookup"><span data-stu-id="b8944-115">**cscript WiImport.vbs \[path to database\]\[path to folder\]\[options\] \[archive file list**\]</span></span>

<span data-ttu-id="b8944-116">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="b8944-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="b8944-117">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="b8944-117">or if too few arguments are specified.</span></span> <span data-ttu-id="b8944-118">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ percorso del file \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b8944-118">To redirect the output to a file, end the command line with VBS > \[path to file\].The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="b8944-119">Specificare il percorso di un database di Windows Installer da creare o che deve ricevere le tabelle importate.</span><span class="sxs-lookup"><span data-stu-id="b8944-119">Specify the path to a Windows installer database that is to be created or that is to receive the imported tables.</span></span> <span data-ttu-id="b8944-120">Specificare il percorso della cartella contenente i file di archivio delle tabelle da importare.</span><span class="sxs-lookup"><span data-stu-id="b8944-120">Specify the path to the folder containing the archive files of the tables that are being imported.</span></span> <span data-ttu-id="b8944-121">Elenca i nomi dei file di archivio che vengono importati.</span><span class="sxs-lookup"><span data-stu-id="b8944-121">List the names of the archive files that are being imported.</span></span> <span data-ttu-id="b8944-122">\*Per importare più file, è possibile usare nomi di file con caratteri jolly, ad esempio IDT.</span><span class="sxs-lookup"><span data-stu-id="b8944-122">Wildcard file names, such as \*.idt, can be used to import multiple files.</span></span>

<span data-ttu-id="b8944-123">Le opzioni seguenti possono essere specificate in un punto qualsiasi della riga di comando prima dell'elenco dei file.</span><span class="sxs-lookup"><span data-stu-id="b8944-123">The following options may be specified anywhere on the command line before the file list.</span></span>



| <span data-ttu-id="b8944-124">Opzione</span><span class="sxs-lookup"><span data-stu-id="b8944-124">Option</span></span>              | <span data-ttu-id="b8944-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8944-125">Description</span></span>                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8944-126">non è stata specificata alcuna opzione</span><span class="sxs-lookup"><span data-stu-id="b8944-126">no option specified</span></span> | <span data-ttu-id="b8944-127">Importa l'elenco dei file di archivio tabelle dalla cartella specificata nel database Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b8944-127">Import the list of table archive files from the specified folder into the Windows Installer database.</span></span>                                |
| <span data-ttu-id="b8944-128">/C</span><span class="sxs-lookup"><span data-stu-id="b8944-128">/c</span></span>                  | <span data-ttu-id="b8944-129">Creare un database di Windows Installer e quindi importare l'elenco dei file di archivio tabelle dalla cartella specificata al nuovo database.</span><span class="sxs-lookup"><span data-stu-id="b8944-129">Create a Windows Installer database and then import the list of table archive files from the specified folder into the new database.</span></span> |



 

<span data-ttu-id="b8944-130">Per ulteriori informazioni, vedere [Windows Installer esempi di script](windows-installer-scripting-examples.md) per ulteriori esempi di scripting.</span><span class="sxs-lookup"><span data-stu-id="b8944-130">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="b8944-131">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b8944-131">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="b8944-132">Si noti che in [un esempio di localizzazione](a-localization-example.md) viene inoltre illustrato l' [importazione delle tabelle ActionText e degli errori localizzati](importing-localized-error-and-actiontext-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b8944-132">Note that [A Localization Example](a-localization-example.md) also demonstrates [Importing Localized Error and ActionText Tables](importing-localized-error-and-actiontext-tables.md).</span></span>

 

 



