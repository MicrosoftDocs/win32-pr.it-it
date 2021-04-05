---
title: Impostazioni del registro di sistema estensione del nome file
description: Impostazioni del registro di sistema estensione del nome file
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Windows Media Player, registro di sistema
- Windows Media Player, estensioni di file
- Registro di sistema, estensioni di file
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712952"
---
# <a name="file-name-extension-registry-settings"></a><span data-ttu-id="44fc7-108">Impostazioni del registro di sistema estensione del nome file</span><span class="sxs-lookup"><span data-stu-id="44fc7-108">File Name Extension Registry Settings</span></span>

<span data-ttu-id="44fc7-109">Se i file multimediali digitali hanno un formato personalizzato, è possibile specificare Windows Media Player con informazioni sul formato personalizzato inserendo le voci nel registro di sistema nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="44fc7-109">If your digital media files have a custom format, you can provide Windows Media Player with information about your custom format by placing entries in the registry on the user's computer.</span></span> <span data-ttu-id="44fc7-110">Windows Media Player controlla le voci del registro di sistema per determinare come gestire i file.</span><span class="sxs-lookup"><span data-stu-id="44fc7-110">Windows Media Player inspects your registry entries to determine how it should handle your files.</span></span> <span data-ttu-id="44fc7-111">Nell'elenco seguente vengono illustrate alcune delle operazioni che è possibile eseguire creando voci del registro di sistema relative al formato di file multimediale personalizzato.</span><span class="sxs-lookup"><span data-stu-id="44fc7-111">The following list shows several of the things you can do by creating registry entries that pertain to your custom media file format.</span></span>

-   <span data-ttu-id="44fc7-112">Concedere all'utente l'autorizzazione per la riproduzione, la copia o la transcodifica dei file.</span><span class="sxs-lookup"><span data-stu-id="44fc7-112">Grant permission for the Player to play, copy, or transcode your files.</span></span>
-   <span data-ttu-id="44fc7-113">Specificare la tecnologia sottostante che il lettore deve utilizzare per riprodurre i file.</span><span class="sxs-lookup"><span data-stu-id="44fc7-113">Specify the underlying technology that the Player should use to play your files.</span></span>
-   <span data-ttu-id="44fc7-114">Specificare la posizione in cui il lettore deve visualizzare i file nella visualizzazione libreria.</span><span class="sxs-lookup"><span data-stu-id="44fc7-114">Specify where the Player should display your files in its library view.</span></span>
-   <span data-ttu-id="44fc7-115">Specificare un plug-in che il lettore deve usare per convertire i file in un formato standard.</span><span class="sxs-lookup"><span data-stu-id="44fc7-115">Specify a plug-in that the Player should use to convert your files to a standard format.</span></span>
-   <span data-ttu-id="44fc7-116">Specificare un codice di formato MTP (Media Transport Protocol) che il lettore può usare per determinare se un dispositivo portatile specifico supporta il formato di file.</span><span class="sxs-lookup"><span data-stu-id="44fc7-116">Specify a Media Transport Protocol (MTP) format code that the Player can use to determine whether a particular portable device supports your file format.</span></span>

<span data-ttu-id="44fc7-117">La maggior parte delle voci fornite si troverà sotto una sottochiave associata all'estensione del nome file personalizzata.</span><span class="sxs-lookup"><span data-stu-id="44fc7-117">Most of the entries that you provide will be under a subkey that is associated with your custom file name extension.</span></span> <span data-ttu-id="44fc7-118">È possibile creare tale sottochiave nel \_ \_ sottoalbero del computer locale HKEY e nel \_ \_ sottoalbero HKEY Current User.</span><span class="sxs-lookup"><span data-stu-id="44fc7-118">You can create that subkey in the HKEY\_LOCAL\_MACHINE subtree and in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="44fc7-119">Windows Media Player cerca innanzitutto nel \_ \_ sottoalbero del computer locale HKEY.</span><span class="sxs-lookup"><span data-stu-id="44fc7-119">Windows Media Player looks first in the HKEY\_LOCAL\_MACHINE subtree.</span></span> <span data-ttu-id="44fc7-120">Se non trova il risultato necessario, Cerca nel \_ \_ sottoalbero dell'utente corrente di HKEY.</span><span class="sxs-lookup"><span data-stu-id="44fc7-120">If it doesn't find what it needs there, it looks in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="44fc7-121">Si noti che il codice che tenta di scrivere nel registro di sistema nel computer dell'utente può scrivere nel \_ sottoalbero del computer locale HKEY \_ solo se l'utente corrente dispone di privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="44fc7-121">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="44fc7-122">Per scrivere informazioni sul formato di file personalizzato nel \_ \_ sottoalbero del computer locale hKey, creare la sottochiave seguente.</span><span class="sxs-lookup"><span data-stu-id="44fc7-122">To write information about your custom file format to the HKEY\_LOCAL\_MACHINE subtree, create the following subkey.</span></span>

<span data-ttu-id="44fc7-123">**HKEY \_ \_Computer locale \\ software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\** *customExtension*</span><span class="sxs-lookup"><span data-stu-id="44fc7-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="44fc7-124">dove *customExtension* è l'estensione del nome di file, incluso il separatore del punto (.).</span><span class="sxs-lookup"><span data-stu-id="44fc7-124">where *customExtension* is the file name extension including the dot (.) separator.</span></span> <span data-ttu-id="44fc7-125">Se, ad esempio, l'estensione per il formato di file personalizzato è. xyz, creare la sottochiave seguente.</span><span class="sxs-lookup"><span data-stu-id="44fc7-125">For example, if the extension for your custom file format is .xyz, create the following subkey.</span></span>

<span data-ttu-id="44fc7-126">**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\ . xyz**</span><span class="sxs-lookup"><span data-stu-id="44fc7-126">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz**</span></span>

<span data-ttu-id="44fc7-127">Per scrivere informazioni sul formato di file personalizzato nel \_ sottoalbero dell'utente corrente di HKEY \_ , creare la sottochiave seguente.</span><span class="sxs-lookup"><span data-stu-id="44fc7-127">To write information about your custom file format to the HKEY\_CURRENT\_USER subtree, create the following subkey.</span></span>

<span data-ttu-id="44fc7-128">**HKEY \_ \_Software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\** *customExtension*</span><span class="sxs-lookup"><span data-stu-id="44fc7-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="44fc7-129">È possibile scrivere una o più delle voci seguenti nella sottochiave *customExtension* .</span><span class="sxs-lookup"><span data-stu-id="44fc7-129">You can write one or more of the following entries in your *customExtension* subkey.</span></span>

-   <span data-ttu-id="44fc7-130">**Autorizzazioni**</span><span class="sxs-lookup"><span data-stu-id="44fc7-130">**Permissions**</span></span>
-   <span data-ttu-id="44fc7-131">**Runtime**</span><span class="sxs-lookup"><span data-stu-id="44fc7-131">**Runtime**</span></span>
-   <span data-ttu-id="44fc7-132">**FormatCode**</span><span class="sxs-lookup"><span data-stu-id="44fc7-132">**FormatCode**</span></span>

<span data-ttu-id="44fc7-133">Per specificare i plug-in di conversione per il formato di file multimediale personalizzato, creare una sottochiave **ConvertPluginCLSID** nella sottochiave *customExtension* .</span><span class="sxs-lookup"><span data-stu-id="44fc7-133">To specify conversion plug-ins for your custom media file format, create a **ConvertPluginCLSID** subkey in your *customExtension* subkey.</span></span>

<span data-ttu-id="44fc7-134">Per specificare la posizione in cui Windows Media Player deve visualizzare i file nella visualizzazione libreria, scrivere una voce che rappresenti il formato di file personalizzato nella sottochiave seguente.</span><span class="sxs-lookup"><span data-stu-id="44fc7-134">To specify where Windows Media Player should display your files in its library view, write an entry that represents your custom file format in the following subkey.</span></span>

<span data-ttu-id="44fc7-135">**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**</span><span class="sxs-lookup"><span data-stu-id="44fc7-135">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="44fc7-136">Negli argomenti seguenti vengono descritte le sottochiavi e le voci del registro di sistema che forniscono Windows Media Player con informazioni sui formati di file multimediali personalizzati.</span><span class="sxs-lookup"><span data-stu-id="44fc7-136">The following topics describe the registry subkeys and entries that provide Windows Media Player with information about custom media file formats.</span></span>

-   [<span data-ttu-id="44fc7-137">Voce del registro di sistema autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="44fc7-137">Permissions Registry Entry</span></span>](permissions-registry-entry.md)
-   [<span data-ttu-id="44fc7-138">Voce del registro di sistema runtime</span><span class="sxs-lookup"><span data-stu-id="44fc7-138">Runtime Registry Entry</span></span>](runtime-registry-entry.md)
-   [<span data-ttu-id="44fc7-139">Voce del registro di sistema FormatCode</span><span class="sxs-lookup"><span data-stu-id="44fc7-139">FormatCode Registry Entry</span></span>](formatcode-registry-entry.md)
-   [<span data-ttu-id="44fc7-140">Voci del registro di sistema di classificazione delle librerie</span><span class="sxs-lookup"><span data-stu-id="44fc7-140">Library Classification Registry Entries</span></span>](library-classification-registry-entries.md)
-   [<span data-ttu-id="44fc7-141">Sottochiave ConvertPluginCLSID</span><span class="sxs-lookup"><span data-stu-id="44fc7-141">ConvertPluginCLSID Subkey</span></span>](convertpluginclsid-subkey.md)

## <a name="related-topics"></a><span data-ttu-id="44fc7-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44fc7-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44fc7-143">**Impostazioni del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="44fc7-143">**Registry Settings**</span></span>](registry-settings.md)
</dt> <dt>

[<span data-ttu-id="44fc7-144">**Plug-in di conversione di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="44fc7-144">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




