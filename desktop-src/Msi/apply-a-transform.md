---
description: Il file VBScript WiUseXfm.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. In questo esempio viene illustrato come utilizzare lo script per applicare una trasformazione a un database Windows Installer.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Applicare una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881130"
---
# <a name="apply-a-transform"></a><span data-ttu-id="aa905-104">Applicare una trasformazione</span><span class="sxs-lookup"><span data-stu-id="aa905-104">Apply a Transform</span></span>

<span data-ttu-id="aa905-105">Il file VBScript WiUseXfm.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="aa905-105">The VBScript file WiUseXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="aa905-106">In questo esempio viene illustrato come utilizzare lo script per applicare una trasformazione a un database Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="aa905-106">This sample shows how script can be used to apply a transform to a Windows Installer database.</span></span>

<span data-ttu-id="aa905-107">Nell'esempio viene illustrato l'utilizzo di</span><span class="sxs-lookup"><span data-stu-id="aa905-107">The sample demonstrates the use of</span></span>

-   [<span data-ttu-id="aa905-108">**Metodo OpenDatabase (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="aa905-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="aa905-109">[**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="aa905-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="aa905-110">**Metodo ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="aa905-110">**ApplyTransform method**</span></span>](database-applytransform.md)
-   <span data-ttu-id="aa905-111">[**Metodo commit**](database-commit.md) dell' [ **oggetto di database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="aa905-111">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="aa905-112">Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="aa905-112">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="aa905-113">Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="aa905-113">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="aa905-114">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="aa905-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="aa905-115">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="aa905-115">or if too few arguments are specified.</span></span> <span data-ttu-id="aa905-116">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .</span><span class="sxs-lookup"><span data-stu-id="aa905-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="aa905-117">Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="aa905-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="aa905-118">**cscript WiUseXfm.vbs \[ percorso al percorso del database originale \] \[ per le \] Opzioni del file di trasformazione \[\]**</span><span class="sxs-lookup"><span data-stu-id="aa905-118">**cscript WiUseXfm.vbs \[path to original database\]\[path to transform file\]\[options\]**</span></span>

<span data-ttu-id="aa905-119">Consente di specificare il percorso del database di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="aa905-119">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="aa905-120">Consente di specificare il percorso del file di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="aa905-120">Specify the path to the transform file.</span></span> <span data-ttu-id="aa905-121">Se il percorso del file di trasformazione viene omesso, vengono confrontati solo i due database.</span><span class="sxs-lookup"><span data-stu-id="aa905-121">If the path to the transform file is omitted, the two databases are only compared.</span></span> <span data-ttu-id="aa905-122">Il terzo argomento è un valore numerico facoltativo che specifica un set di condizioni di errore che devono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="aa905-122">The third argument is an optional numeric value that specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="aa905-123">Aggiungere questi valori insieme per escludere più condizioni.</span><span class="sxs-lookup"><span data-stu-id="aa905-123">Add these values together to suppress multiple conditions.</span></span>



| <span data-ttu-id="aa905-124">Valore</span><span class="sxs-lookup"><span data-stu-id="aa905-124">Value</span></span> | <span data-ttu-id="aa905-125">Condizione di errore da disattivare</span><span class="sxs-lookup"><span data-stu-id="aa905-125">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="aa905-126">1</span><span class="sxs-lookup"><span data-stu-id="aa905-126">1</span></span>     | <span data-ttu-id="aa905-127">Aggiunta di una riga già esistente.</span><span class="sxs-lookup"><span data-stu-id="aa905-127">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="aa905-128">2</span><span class="sxs-lookup"><span data-stu-id="aa905-128">2</span></span>     | <span data-ttu-id="aa905-129">Eliminazione di una riga inesistente.</span><span class="sxs-lookup"><span data-stu-id="aa905-129">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="aa905-130">4</span><span class="sxs-lookup"><span data-stu-id="aa905-130">4</span></span>     | <span data-ttu-id="aa905-131">Aggiunta di una tabella già esistente.</span><span class="sxs-lookup"><span data-stu-id="aa905-131">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="aa905-132">8</span><span class="sxs-lookup"><span data-stu-id="aa905-132">8</span></span>     | <span data-ttu-id="aa905-133">Eliminazione di una tabella inesistente.</span><span class="sxs-lookup"><span data-stu-id="aa905-133">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="aa905-134">16</span><span class="sxs-lookup"><span data-stu-id="aa905-134">16</span></span>    | <span data-ttu-id="aa905-135">Aggiornamento di una riga inesistente.</span><span class="sxs-lookup"><span data-stu-id="aa905-135">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="aa905-136">256</span><span class="sxs-lookup"><span data-stu-id="aa905-136">256</span></span>   | <span data-ttu-id="aa905-137">Mancata corrispondenza delle tabelle codici del database e della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="aa905-137">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="aa905-138">Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="aa905-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="aa905-139">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="aa905-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



