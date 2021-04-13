---
description: Il file VBScript Manifestchk.vbs è uno strumento di convalida disponibile in Microsoft Windows Software Development Kit (SDK) che convalida i file manifesto dell'applicazione e dell'assembly.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401696"
---
# <a name="manifestchkvbs"></a><span data-ttu-id="6219a-103">Manifestchk.vbs</span><span class="sxs-lookup"><span data-stu-id="6219a-103">Manifestchk.vbs</span></span>

<span data-ttu-id="6219a-104">Il file VBScript Manifestchk.vbs è uno strumento di convalida disponibile in Microsoft Windows Software Development Kit (SDK) che convalida i file manifesto dell'applicazione e dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="6219a-104">The VBScript file Manifestchk.vbs is a validation tool provided in the Microsoft Windows Software Development Kit (SDK) that validates application and assembly manifest files.</span></span>

<span data-ttu-id="6219a-105">Per eseguire questo esempio è necessario Windows script host.</span><span class="sxs-lookup"><span data-stu-id="6219a-105">Running this sample requires Windows Script Host.</span></span> <span data-ttu-id="6219a-106">Per ulteriori informazioni su Windows script host, vedere la sezione Windows script host del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6219a-106">For more information about Windows Script Host, see the Windows Script Host section of the Windows SDK.</span></span> <span data-ttu-id="6219a-107">Windows script host è in realtà costituito da due host.</span><span class="sxs-lookup"><span data-stu-id="6219a-107">Windows Script Host is actually two hosts.</span></span> <span data-ttu-id="6219a-108">CScript.exe è la versione che consente di eseguire gli script dal prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="6219a-108">CScript.exe is the version that enables you to run scripts from the command prompt.</span></span> <span data-ttu-id="6219a-109">CScript.exe fornisce opzioni della riga di comando per l'impostazione delle proprietà dello script.</span><span class="sxs-lookup"><span data-stu-id="6219a-109">CScript.exe provides command-line switches for setting script properties.</span></span>

<span data-ttu-id="6219a-110">Il formato della riga di comando è il seguente:</span><span class="sxs-lookup"><span data-stu-id="6219a-110">The command-line format is the following:</span></span>

<span data-ttu-id="6219a-111">**Cscript//NoLogo manifestchk.vbs/s:** *\[ unità: \] \[ percorso \] schemafilename* **/m:** *\[ unità: \] \[ percorso \] ManifestFileName* **\[ /q \] /t:** *opzione*</span><span class="sxs-lookup"><span data-stu-id="6219a-111">**Cscript //nologo manifestchk.vbs /s:** *\[drive:\]\[path\]schemafilename* **/m:** *\[drive:\]\[path\]manifestfilename* **\[/q\] /t:** *option*</span></span>

<span data-ttu-id="6219a-112">I flag definiti per Manifestchk.vbs sono descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6219a-112">The flags defined for Manifestchk.vbs are described in the following table.</span></span>



| <span data-ttu-id="6219a-113">Flag</span><span class="sxs-lookup"><span data-stu-id="6219a-113">Flag</span></span> | <span data-ttu-id="6219a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6219a-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6219a-115">/s</span><span class="sxs-lookup"><span data-stu-id="6219a-115">/s</span></span>   | <span data-ttu-id="6219a-116">Specifica il nome del file di schema del manifesto rispetto al quale convalidare i manifesti.</span><span class="sxs-lookup"><span data-stu-id="6219a-116">Specifies the manifest schema file name to validate manifests against.</span></span> <span data-ttu-id="6219a-117">Vedere lo schema nello [schema del file manifesto](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="6219a-117">See the schema at [Manifest File Schema](manifest-file-schema.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6219a-118">/m</span><span class="sxs-lookup"><span data-stu-id="6219a-118">/m</span></span>   | <span data-ttu-id="6219a-119">Specifica il nome del file manifesto da convalidare.</span><span class="sxs-lookup"><span data-stu-id="6219a-119">Specifies the manifest file name to validate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6219a-120">/q</span><span class="sxs-lookup"><span data-stu-id="6219a-120">/q</span></span>   | <span data-ttu-id="6219a-121">Disattiva tutto l'output nella console.</span><span class="sxs-lookup"><span data-stu-id="6219a-121">Suppresses all output to the console.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6219a-122">/t</span><span class="sxs-lookup"><span data-stu-id="6219a-122">/t</span></span>   | <span data-ttu-id="6219a-123">Specifica il tipo di file manifesto.</span><span class="sxs-lookup"><span data-stu-id="6219a-123">Specifies the type of manifest file.</span></span> <span data-ttu-id="6219a-124">I valori validi sono: AM Validate the [manifest file schema](manifest-file-schema.md) of a [assembly manifest](assembly-manifests.md) o [Application Manifest](application-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="6219a-124">The valid values are: AM   Validate the [manifest file schema](manifest-file-schema.md) of an [assembly manifest](assembly-manifests.md) or [application manifest](application-manifests.md)</span></span><br/> <span data-ttu-id="6219a-125">PC convalida lo [schema del file di configurazione](publisher-configuration-file-schema.md) dell'editore di un [file di configurazione del server di pubblicazione](publisher-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="6219a-125">PC   Validate the [publisher configuration file schema](publisher-configuration-file-schema.md) of a [publisher configuration file](publisher-configuration-files.md)</span></span><br/> <span data-ttu-id="6219a-126">AC convalida lo schema del file di configurazione dell'applicazione di un [file di configurazione dell'applicazione](application-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="6219a-126">AC   Validate the application configuration file schema of an [application configuration file](application-configuration-files.md).</span></span><br/> |



 

<span data-ttu-id="6219a-127">Se il flag/q non è specificato, Manifestchk.vbs Visualizza informazioni dettagliate sul primo errore rilevato nel file e visualizza un messaggio che indica se il processo di convalida ha avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="6219a-127">If the /q flag is not specified, Manifestchk.vbs displays detailed information about the first error encountered in the file, and displays a message stating whether the validation process was successful or not.</span></span>

<span data-ttu-id="6219a-128">Questa utilità verifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="6219a-128">This utility checks for the following:</span></span>

-   <span data-ttu-id="6219a-129">Riga di comando valida.</span><span class="sxs-lookup"><span data-stu-id="6219a-129">A valid command line.</span></span>
-   <span data-ttu-id="6219a-130">È installato MSXML versione 3.</span><span class="sxs-lookup"><span data-stu-id="6219a-130">That MSXML version 3 is installed.</span></span>
-   <span data-ttu-id="6219a-131">Il manifesto utilizza codice XML ben formato.</span><span class="sxs-lookup"><span data-stu-id="6219a-131">That the manifest uses well-formed XML.</span></span>
-   <span data-ttu-id="6219a-132">Che il manifesto acconsente allo schema fornito.</span><span class="sxs-lookup"><span data-stu-id="6219a-132">That the manifest agrees with the provided schema.</span></span> <span data-ttu-id="6219a-133">Si noti che Manifestchk.vbs verifica il file manifesto solo in base a quanto specificato nello schema fornito.</span><span class="sxs-lookup"><span data-stu-id="6219a-133">Note that Manifestchk.vbs verifies the manifest file based only on what is specified in the provided schema.</span></span> <span data-ttu-id="6219a-134">Per un esempio di schema del manifesto, vedere [schema del file manifesto](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="6219a-134">For an example of a manifest schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="6219a-135">Cscript.exe restituisce il valore 0 se il processo di convalida ha avuto esito positivo e 1 in caso di esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6219a-135">Cscript.exe returns a value of 0 if the validation process was successful and 1 if it was not successful.</span></span> <span data-ttu-id="6219a-136">Restituisce 2 Se si verifica un errore in un argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="6219a-136">It returns 2 if there is an error in a command line argument.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6219a-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6219a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6219a-138">Strumenti di sviluppo di assembly affiancati</span><span class="sxs-lookup"><span data-stu-id="6219a-138">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




