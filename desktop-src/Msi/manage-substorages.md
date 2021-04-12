---
description: Il file VBScript WiSubStg.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Gestisci sottoarchivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348976"
---
# <a name="manage-substorages"></a><span data-ttu-id="9fcaf-103">Gestisci sottoarchivi</span><span class="sxs-lookup"><span data-stu-id="9fcaf-103">Manage Substorages</span></span>

<span data-ttu-id="9fcaf-104">Il file VBScript WiSubStg.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="9fcaf-104">The VBScript file WiSubStg.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="9fcaf-105">In questo esempio viene illustrato come utilizzare lo script per gestire le sottoarchiviazioni in un database Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-105">This sample shows how script can be used to manage substorages in a Windows Installer database.</span></span> <span data-ttu-id="9fcaf-106">Una trasformazione può essere aggiunta a un database di Windows Installer esistente come sottoarchivio.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-106">A transform can be added to an existing Windows Installer database as a substorage.</span></span>

<span data-ttu-id="9fcaf-107">Nell'esempio viene illustrato l'utilizzo di:</span><span class="sxs-lookup"><span data-stu-id="9fcaf-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="9fcaf-108">\_Tabella Storages</span><span class="sxs-lookup"><span data-stu-id="9fcaf-108">\_Storages table</span></span>](-storages-table.md)
-   [<span data-ttu-id="9fcaf-109">**Metodo OpenDatabase (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="9fcaf-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="9fcaf-110">**Metodo CreaRecord**</span><span class="sxs-lookup"><span data-stu-id="9fcaf-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="9fcaf-111">[**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="9fcaf-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="9fcaf-112">**OpenView (metodo)**</span><span class="sxs-lookup"><span data-stu-id="9fcaf-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="9fcaf-113">[**Metodo commit**](database-commit.md) dell' [ **oggetto di database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="9fcaf-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="9fcaf-114">**Fetch (metodo)**</span><span class="sxs-lookup"><span data-stu-id="9fcaf-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="9fcaf-115">**Metodo Modify**</span><span class="sxs-lookup"><span data-stu-id="9fcaf-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="9fcaf-116">[**Metodo Execute**](view-execute.md) dell' [ **oggetto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="9fcaf-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="9fcaf-117">**Proprietà StringData**</span><span class="sxs-lookup"><span data-stu-id="9fcaf-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="9fcaf-118">[**Metodo sestream**](record-setstream.md) dell' [ **oggetto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="9fcaf-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="9fcaf-119">Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="9fcaf-120">Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="9fcaf-121">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="9fcaf-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="9fcaf-122">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-122">or if too few arguments are specified.</span></span> <span data-ttu-id="9fcaf-123">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .</span><span class="sxs-lookup"><span data-stu-id="9fcaf-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="9fcaf-124">Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="9fcaf-125">**cscript WiSubStg.vbs \[ percorso al percorso del database \] \[ \] \[ nome del \] \[ sottoarchivio delle opzioni file\]**</span><span class="sxs-lookup"><span data-stu-id="9fcaf-125">**cscript WiSubStg.vbs \[path to database\]\[path to file\]\[options\]\[substorage name\]**</span></span>

<span data-ttu-id="9fcaf-126">Specificare il percorso del database di Windows Installer per aggiungere o rimuovere l'archivio secondario.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-126">Specify the path to the Windows Installer database to add or remove substorage.</span></span> <span data-ttu-id="9fcaf-127">Specificare un percorso per il file di trasformazione o di database che viene aggiunto come sottoarchivio.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-127">Specify a path to the transform or database file that is being added as substorage.</span></span> <span data-ttu-id="9fcaf-128">Per elencare le sottoarchiviazioni nel database di Windows Installer, omettere il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-128">To list the substorages in the Windows Installer database, omit the path to this file.</span></span> <span data-ttu-id="9fcaf-129">È possibile specificare un nome di sottoarchiviazione facoltativo, se viene omesso, per impostazione predefinita il nome del sottoarchivio viene impostato sul nome del file.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-129">You may specify an optional substorage name, if this is omitted the substorage name defaults to the file name.</span></span>

<span data-ttu-id="9fcaf-130">È possibile specificare l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-130">The following option may be specified.</span></span>



| <span data-ttu-id="9fcaf-131">Opzione</span><span class="sxs-lookup"><span data-stu-id="9fcaf-131">Option</span></span>              | <span data-ttu-id="9fcaf-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fcaf-132">Description</span></span>                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fcaf-133">non è stata specificata alcuna opzione</span><span class="sxs-lookup"><span data-stu-id="9fcaf-133">no option specified</span></span> | <span data-ttu-id="9fcaf-134">Aggiungere una risorsa di archiviazione al database Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-134">Add a substorage to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="9fcaf-135">/d</span><span class="sxs-lookup"><span data-stu-id="9fcaf-135">/d</span></span>                  | <span data-ttu-id="9fcaf-136">Rimuovere un sottoarchivio.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-136">Remove a substorage.</span></span> <span data-ttu-id="9fcaf-137">Questo flag di opzione deve essere seguito dal nome dell'archivio subarchiviazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9fcaf-137">This option flag must be followed by the name of the substorage to be removed.</span></span> |



 

<span data-ttu-id="9fcaf-138">Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="9fcaf-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="9fcaf-139">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="9fcaf-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="9fcaf-140">Si noti che [un esempio di localizzazione](a-localization-example.md) illustra [come incorporare le trasformazioni di personalizzazione come sottoarchivio](embedding-customization-transforms-as-substorage.md).</span><span class="sxs-lookup"><span data-stu-id="9fcaf-140">Note that [A Localization Example](a-localization-example.md) demonstrates [Embedding Customization Transforms as Substorage](embedding-customization-transforms-as-substorage.md).</span></span>

 

 



