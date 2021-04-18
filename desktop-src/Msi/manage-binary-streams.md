---
description: Il file VBScript WiStream.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Gestisci flussi binari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316266"
---
# <a name="manage-binary-streams"></a><span data-ttu-id="42b59-103">Gestisci flussi binari</span><span class="sxs-lookup"><span data-stu-id="42b59-103">Manage Binary Streams</span></span>

<span data-ttu-id="42b59-104">Il file VBScript WiStream.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="42b59-104">The VBScript file WiStream.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="42b59-105">In questo esempio viene illustrato come utilizzare gli script per gestire i flussi binari in un database Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="42b59-105">This sample shows how script can be used to manage binary streams in a Windows Installer database.</span></span> <span data-ttu-id="42b59-106">È possibile utilizzare l'esempio per immettere file CAB compressi in un database.</span><span class="sxs-lookup"><span data-stu-id="42b59-106">The sample may be used to enter compressed file cabinets into a database.</span></span> <span data-ttu-id="42b59-107">In questo esempio viene illustrata l'operazione della [ \_ tabella Streams](-streams-table.md) nel database Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="42b59-107">This sample demonstrates the operation of the [\_Streams table](-streams-table.md) in the Windows Installer database.</span></span>

<span data-ttu-id="42b59-108">Nell'esempio viene inoltre illustrato l'utilizzo di:</span><span class="sxs-lookup"><span data-stu-id="42b59-108">The sample also demonstrates the use of:</span></span>

-   [<span data-ttu-id="42b59-109">**Metodo OpenDatabase (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="42b59-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="42b59-110">**Metodo CreaRecord**</span><span class="sxs-lookup"><span data-stu-id="42b59-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="42b59-111">[**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="42b59-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="42b59-112">**OpenView (metodo)**</span><span class="sxs-lookup"><span data-stu-id="42b59-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="42b59-113">[**Metodo commit**](database-commit.md) dell' [ **oggetto di database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="42b59-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="42b59-114">**Fetch (metodo)**</span><span class="sxs-lookup"><span data-stu-id="42b59-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="42b59-115">**Metodo Modify**</span><span class="sxs-lookup"><span data-stu-id="42b59-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="42b59-116">[**Metodo Execute**](view-execute.md) dell' [ **oggetto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="42b59-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="42b59-117">**Proprietà StringData**</span><span class="sxs-lookup"><span data-stu-id="42b59-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="42b59-118">[**Metodo sestream**](record-setstream.md) dell' [ **oggetto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="42b59-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="42b59-119">Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="42b59-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="42b59-120">Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="42b59-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="42b59-121">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="42b59-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="42b59-122">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="42b59-122">or if too few arguments are specified.</span></span> <span data-ttu-id="42b59-123">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .</span><span class="sxs-lookup"><span data-stu-id="42b59-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="42b59-124">Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="42b59-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="42b59-125">**cscript WiStream.vbs \[ percorso al percorso del database \] \[ per il nome del \] \[ flusso di opzioni \] \[ file\]**</span><span class="sxs-lookup"><span data-stu-id="42b59-125">**cscript WiStream.vbs \[path to database\]\[path to file\]\[options\]\[stream name\]**</span></span>

<span data-ttu-id="42b59-126">Specificare il percorso del database di Windows Installer che deve ricevere il flusso.</span><span class="sxs-lookup"><span data-stu-id="42b59-126">Specify the path to the Windows Installer database that is to receive the stream.</span></span> <span data-ttu-id="42b59-127">Specificare il percorso del file binario contenente i dati del flusso.</span><span class="sxs-lookup"><span data-stu-id="42b59-127">Specify a path to the binary file containing the stream data.</span></span> <span data-ttu-id="42b59-128">Per elencare i flussi nel database del programma di installazione, omettere questo percorso.</span><span class="sxs-lookup"><span data-stu-id="42b59-128">To list the streams in the installer database, omit this path.</span></span> <span data-ttu-id="42b59-129">È possibile specificare un nome di flusso facoltativo. Se viene omesso, viene impostato come predefinito il nome del file.</span><span class="sxs-lookup"><span data-stu-id="42b59-129">You may specify an optional stream name, if this is omitted it defaults to the file name.</span></span>

<span data-ttu-id="42b59-130">È possibile specificare l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="42b59-130">The following option may be specified.</span></span>



| <span data-ttu-id="42b59-131">Opzione</span><span class="sxs-lookup"><span data-stu-id="42b59-131">Option</span></span>              | <span data-ttu-id="42b59-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42b59-132">Description</span></span>                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b59-133">non è stata specificata alcuna opzione</span><span class="sxs-lookup"><span data-stu-id="42b59-133">no option specified</span></span> | <span data-ttu-id="42b59-134">Aggiungere un flusso al database Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="42b59-134">Add a stream to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="42b59-135">/d</span><span class="sxs-lookup"><span data-stu-id="42b59-135">/d</span></span>                  | <span data-ttu-id="42b59-136">Rimuovere un flusso.</span><span class="sxs-lookup"><span data-stu-id="42b59-136">Remove a stream.</span></span> <span data-ttu-id="42b59-137">Questo flag di opzione deve essere seguito dal nome della sottoarchiviazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="42b59-137">This option flag must be followed by the name of the substorage being removed.</span></span> |



 

<span data-ttu-id="42b59-138">Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="42b59-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="42b59-139">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="42b59-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



