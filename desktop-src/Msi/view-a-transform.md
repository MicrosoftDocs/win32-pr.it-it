---
description: Il file VBScript WiLstXfm.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Questo esempio di script può essere utilizzato per visualizzare un file di trasformazione.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Visualizzazione di una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306568"
---
# <a name="view-a-transform"></a><span data-ttu-id="3e599-104">Visualizzazione di una trasformazione</span><span class="sxs-lookup"><span data-stu-id="3e599-104">View a Transform</span></span>

<span data-ttu-id="3e599-105">Il file VBScript WiLstXfm.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="3e599-105">The VBScript file WiLstXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="3e599-106">Questo esempio di script può essere utilizzato per visualizzare un file di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="3e599-106">This script sample can be used to view a transform file.</span></span>

<span data-ttu-id="3e599-107">Nell'esempio viene illustrato l'utilizzo di:</span><span class="sxs-lookup"><span data-stu-id="3e599-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="3e599-108">\_Tabella transformview</span><span class="sxs-lookup"><span data-stu-id="3e599-108">\_TransformView table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="3e599-109">**Metodo OpenDatabase (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="3e599-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="3e599-110">[**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="3e599-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="3e599-111">**Metodo ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="3e599-111">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="3e599-112">**OpenView (metodo)**</span><span class="sxs-lookup"><span data-stu-id="3e599-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="3e599-113">[**Metodo commit**](database-commit.md) dell' [ **oggetto di database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="3e599-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="3e599-114">**Proprietà IsNull**</span><span class="sxs-lookup"><span data-stu-id="3e599-114">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="3e599-115">[**Proprietà StringData**](record-stringdata.md) dell' [ **oggetto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="3e599-115">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="3e599-116">Per usare questo esempio è necessaria la versione CScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="3e599-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="3e599-117">Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="3e599-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="3e599-118">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="3e599-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="3e599-119">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="3e599-119">or if too few arguments are specified.</span></span> <span data-ttu-id="3e599-120">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .</span><span class="sxs-lookup"><span data-stu-id="3e599-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="3e599-121">Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3e599-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="3e599-122">**cscript WiLstXfm.vbs** *\[ percorso per fare riferimento al \] \[ percorso dell'opzione \] \[ di database per \] la trasformazione da visualizzare*</span><span class="sxs-lookup"><span data-stu-id="3e599-122">**cscript WiLstXfm.vbs** *\[path to reference database\]\[option\]\[path to transform to be viewed\]*</span></span>

<span data-ttu-id="3e599-123">Consente di specificare il percorso del database di riferimento Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3e599-123">Specify the path to the reference Windows Installer database.</span></span> <span data-ttu-id="3e599-124">Consente di specificare un elenco di percorsi per trasformare i file che vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="3e599-124">Specify a list of paths to transform files that are being viewed.</span></span> <span data-ttu-id="3e599-125">Ogni percorso nell'elenco può essere preceduto da un valore numerico facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3e599-125">Each path in the list may by preceded by an optional numeric value.</span></span> <span data-ttu-id="3e599-126">Questo valore specifica un set di condizioni di errore che devono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="3e599-126">This value specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="3e599-127">È possibile aggiungere questi valori insieme per escludere più condizioni.</span><span class="sxs-lookup"><span data-stu-id="3e599-127">You may add these values together to suppress multiple conditions.</span></span> <span data-ttu-id="3e599-128">Se non viene specificata alcuna opzione numerica, tutte le condizioni di errore vengono evitate.</span><span class="sxs-lookup"><span data-stu-id="3e599-128">If no numeric option is specified, all the error conditions are suppressed.</span></span> <span data-ttu-id="3e599-129">Gli argomenti in questo elenco vengono eseguiti nell'ordine da sinistra a destra in cui vengono visualizzati nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="3e599-129">The arguments in this list are executed in the left-to-right order in which they appear on the command line.</span></span>



| <span data-ttu-id="3e599-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3e599-130">Value</span></span> | <span data-ttu-id="3e599-131">Condizione di errore da disattivare</span><span class="sxs-lookup"><span data-stu-id="3e599-131">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="3e599-132">1</span><span class="sxs-lookup"><span data-stu-id="3e599-132">1</span></span>     | <span data-ttu-id="3e599-133">Aggiunta di una riga già esistente.</span><span class="sxs-lookup"><span data-stu-id="3e599-133">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="3e599-134">2</span><span class="sxs-lookup"><span data-stu-id="3e599-134">2</span></span>     | <span data-ttu-id="3e599-135">Eliminazione di una riga inesistente.</span><span class="sxs-lookup"><span data-stu-id="3e599-135">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="3e599-136">4</span><span class="sxs-lookup"><span data-stu-id="3e599-136">4</span></span>     | <span data-ttu-id="3e599-137">Aggiunta di una tabella già esistente.</span><span class="sxs-lookup"><span data-stu-id="3e599-137">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="3e599-138">8</span><span class="sxs-lookup"><span data-stu-id="3e599-138">8</span></span>     | <span data-ttu-id="3e599-139">Eliminazione di una tabella inesistente.</span><span class="sxs-lookup"><span data-stu-id="3e599-139">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="3e599-140">16</span><span class="sxs-lookup"><span data-stu-id="3e599-140">16</span></span>    | <span data-ttu-id="3e599-141">Aggiornamento di una riga inesistente.</span><span class="sxs-lookup"><span data-stu-id="3e599-141">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="3e599-142">256</span><span class="sxs-lookup"><span data-stu-id="3e599-142">256</span></span>   | <span data-ttu-id="3e599-143">Mancata corrispondenza delle tabelle codici del database e della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="3e599-143">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="3e599-144">Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="3e599-144">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="3e599-145">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3e599-145">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



