---
description: Il file VBScript WiGenXfm.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Questo script di esempio può generare una trasformazione da due database Windows Installer. Per altre informazioni, vedere trasformazioni del database.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Genera una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757643"
---
# <a name="generate-a-transform"></a><span data-ttu-id="c7654-105">Genera una trasformazione</span><span class="sxs-lookup"><span data-stu-id="c7654-105">Generate a Transform</span></span>

<span data-ttu-id="c7654-106">Il file VBScript WiGenXfm.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="c7654-106">The VBScript file WiGenXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="c7654-107">Questo script di esempio può generare una trasformazione da due database Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c7654-107">This sample script can generate a transform from two Windows Installer databases.</span></span> <span data-ttu-id="c7654-108">Per altre informazioni, vedere [trasformazioni del database](database-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="c7654-108">For more information see [Database Transforms](database-transforms.md).</span></span>

<span data-ttu-id="c7654-109">Nell'esempio viene illustrato l'utilizzo di:</span><span class="sxs-lookup"><span data-stu-id="c7654-109">The sample demonstrates the use of:</span></span>

[<span data-ttu-id="c7654-110">**Metodo OpenDatabase (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="c7654-110">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)

<span data-ttu-id="c7654-111">[**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="c7654-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="c7654-112">[**Metodo GenerateTransform**](database-generatetransform.md) dell' [ **oggetto di database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="c7654-112">[**GenerateTransform method**](database-generatetransform.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="c7654-113">Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="c7654-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="c7654-114">Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="c7654-114">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="c7654-115">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="c7654-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="c7654-116">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="c7654-116">or if too few arguments are specified.</span></span> <span data-ttu-id="c7654-117">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .</span><span class="sxs-lookup"><span data-stu-id="c7654-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="c7654-118">Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c7654-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="c7654-119">**cscript WiGenXfm.vbs \[ percorso del database originale al percorso del \] \[ database modificato \] \[ per il file di trasformazione\]**</span><span class="sxs-lookup"><span data-stu-id="c7654-119">**cscript WiGenXfm.vbs \[path to original database\]\[path to revised database\]\[path to transform file\]**</span></span>

<span data-ttu-id="c7654-120">Consente di specificare il percorso del database di Windows Installer originale.</span><span class="sxs-lookup"><span data-stu-id="c7654-120">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="c7654-121">Consente di specificare il percorso del database modificato.</span><span class="sxs-lookup"><span data-stu-id="c7654-121">Specify the path to the revised database.</span></span> <span data-ttu-id="c7654-122">Consente di specificare il percorso del file di trasformazione da creare.</span><span class="sxs-lookup"><span data-stu-id="c7654-122">Specify the path to the transform file to be created.</span></span> <span data-ttu-id="c7654-123">Se il percorso del file di trasformazione viene omesso, vengono confrontati solo i due database.</span><span class="sxs-lookup"><span data-stu-id="c7654-123">If the path to the transform file is omitted, the two databases are only compared.</span></span>

<span data-ttu-id="c7654-124">Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="c7654-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="c7654-125">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="c7654-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="c7654-126">Si noti che [un esempio di localizzazione](a-localization-example.md) illustra la [generazione di una trasformazione di personalizzazione](generating-a-customization-transform.md).</span><span class="sxs-lookup"><span data-stu-id="c7654-126">Note that [A Localization Example](a-localization-example.md) demonstrates [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

 

 



