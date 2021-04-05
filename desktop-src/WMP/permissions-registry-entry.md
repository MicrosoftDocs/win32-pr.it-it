---
title: Voce del registro di sistema autorizzazioni
description: Voce del registro di sistema autorizzazioni
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player, estensioni di file
- Windows Media Player, autorizzazioni
- Windows Media Player, registro di sistema
- Registro di sistema, estensioni di file
- Registro di sistema, autorizzazioni
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
- autorizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046284"
---
# <a name="permissions-registry-entry"></a><span data-ttu-id="e21d8-111">Voce del registro di sistema autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="e21d8-111">Permissions Registry Entry</span></span>

<span data-ttu-id="e21d8-112">Quando Windows Media Player rileva un'estensione del nome di file personalizzata, Cerca una sottochiave del registro di sistema corrispondente all'estensione.</span><span class="sxs-lookup"><span data-stu-id="e21d8-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="e21d8-113">La sottochiave è descritta in [impostazioni del registro di sistema estensione del nome file](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e21d8-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="e21d8-114">Una delle voci del registro di sistema che possono essere visualizzate sotto la sottochiave dell'estensione è la voce **autorizzazioni** .</span><span class="sxs-lookup"><span data-stu-id="e21d8-114">One of the registry entries that can appear under the extension's subkey is the **Permissions** entry.</span></span>

<span data-ttu-id="e21d8-115">La voce **autorizzazioni** specifica le azioni che Windows Media Player può eseguire sui file con estensione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="e21d8-115">The **Permissions** entry specifies the actions that Windows Media Player is allowed to perform on files that have the custom extension.</span></span> <span data-ttu-id="e21d8-116">La voce **autorizzazioni** ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="e21d8-116">The **Permissions** entry has the following form.</span></span>



| <span data-ttu-id="e21d8-117">Nome</span><span class="sxs-lookup"><span data-stu-id="e21d8-117">Name</span></span>        | <span data-ttu-id="e21d8-118">Type</span><span class="sxs-lookup"><span data-stu-id="e21d8-118">Type</span></span>           | <span data-ttu-id="e21d8-119">valore</span><span class="sxs-lookup"><span data-stu-id="e21d8-119">Value</span></span>                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="e21d8-120">Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="e21d8-120">Permissions</span></span> | <span data-ttu-id="e21d8-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e21d8-121">**REG\_DWORD**</span></span> | <span data-ttu-id="e21d8-122">Set di flag, ciascuno dei quali concede l'autorizzazione per un'azione specifica.</span><span class="sxs-lookup"><span data-stu-id="e21d8-122">A set of flags, each of which grants permission for a specific action.</span></span> |



 

<span data-ttu-id="e21d8-123">Il valore della voce delle **autorizzazioni** è un **or** bit per bit di uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="e21d8-123">The value of the **Permissions** entry is a bitwise **OR** of one or more of the following flags.</span></span>



| <span data-ttu-id="e21d8-124">Flag (valore decimale)</span><span class="sxs-lookup"><span data-stu-id="e21d8-124">Flag (decimal value)</span></span> | <span data-ttu-id="e21d8-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e21d8-125">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e21d8-126">1</span><span class="sxs-lookup"><span data-stu-id="e21d8-126">1</span></span>                    | <span data-ttu-id="e21d8-127">Autorizzazione per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="e21d8-127">Permission for playback.</span></span> <span data-ttu-id="e21d8-128">È possibile riprodurre i file con l'estensione di file registrato.</span><span class="sxs-lookup"><span data-stu-id="e21d8-128">Files having the registered file name extension can be played.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="e21d8-129">2</span><span class="sxs-lookup"><span data-stu-id="e21d8-129">2</span></span>                    | <span data-ttu-id="e21d8-130">Autorizzazione per l'eliminazione della cartella.</span><span class="sxs-lookup"><span data-stu-id="e21d8-130">Permission for folder drop.</span></span> <span data-ttu-id="e21d8-131">I file con estensione registrata verranno inclusi nella playlist creata quando l'utente trascina una cartella che contiene i file e la rilascia sull'interfaccia utente del lettore.</span><span class="sxs-lookup"><span data-stu-id="e21d8-131">Files having the registered file name extension will be included in the playlist created when the user drags a folder containing the files and drops it on the user interface of the Player.</span></span>                                                      |
| <span data-ttu-id="e21d8-132">4</span><span class="sxs-lookup"><span data-stu-id="e21d8-132">4</span></span>                    | <span data-ttu-id="e21d8-133">Autorizzazione per il CD multimediale.</span><span class="sxs-lookup"><span data-stu-id="e21d8-133">Permission for media CD.</span></span> <span data-ttu-id="e21d8-134">I file con l'estensione di file registrata verranno inclusi nella playlist creata quando un CD contenente i file viene inserito nell'unità CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="e21d8-134">Files having the registered file name extension will be included in the playlist created when a CD containing the files is inserted into the CD-ROM drive.</span></span>                                                                                           |
| <span data-ttu-id="e21d8-135">8</span><span class="sxs-lookup"><span data-stu-id="e21d8-135">8</span></span>                    | <span data-ttu-id="e21d8-136">Autorizzazione per la libreria.</span><span class="sxs-lookup"><span data-stu-id="e21d8-136">Permission for the library.</span></span> <span data-ttu-id="e21d8-137">I file con l'estensione di file registrata possono essere aggiunti alla libreria.</span><span class="sxs-lookup"><span data-stu-id="e21d8-137">Files having the registered file name extension can be added to the library.</span></span> <span data-ttu-id="e21d8-138">Obbligatorio per i plug-in di conversione.</span><span class="sxs-lookup"><span data-stu-id="e21d8-138">Required for conversion plug-ins.</span></span>                                                                                                                                    |
| <span data-ttu-id="e21d8-139">16</span><span class="sxs-lookup"><span data-stu-id="e21d8-139">16</span></span>                   | <span data-ttu-id="e21d8-140">Autorizzazione per lo streaming HTML.</span><span class="sxs-lookup"><span data-stu-id="e21d8-140">Permission for HTML streaming.</span></span> <span data-ttu-id="e21d8-141">I file con l'estensione del nome file registrato verranno inseriti nella cache di Internet Explorer quando vengono recapitati da un flusso Web.</span><span class="sxs-lookup"><span data-stu-id="e21d8-141">Files having the registered file name extension will be inserted into the Internet Explorer cache when delivered from a Web stream.</span></span>                                                                                                            |
| <span data-ttu-id="e21d8-142">128</span><span class="sxs-lookup"><span data-stu-id="e21d8-142">128</span></span>                  | <span data-ttu-id="e21d8-143">Autorizzazione per la transcodifica.</span><span class="sxs-lookup"><span data-stu-id="e21d8-143">Permission for transcoding.</span></span> <span data-ttu-id="e21d8-144">I file con l'estensione del nome file registrato possono essere trascodificati in formato Windows Media in determinate condizioni.</span><span class="sxs-lookup"><span data-stu-id="e21d8-144">Files having the registered file name extension can be transcoded to Windows Media Format under certain conditions.</span></span> <span data-ttu-id="e21d8-145">Vedere [IWMPTranscodePolicy:: allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span><span class="sxs-lookup"><span data-stu-id="e21d8-145">See [IWMPTranscodePolicy::allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span></span> <span data-ttu-id="e21d8-146">Richiede Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e21d8-146">Requires Windows Media Player 10 or later.</span></span> |



 

<span data-ttu-id="e21d8-147">Quando l'utente tenta di riprodurre un file multimediale con estensione di file personalizzata, Windows Media Player ricerca una sottochiave del registro di sistema corrispondente all'estensione.</span><span class="sxs-lookup"><span data-stu-id="e21d8-147">When the user attempts to play a media file that has a custom file name extension, Windows Media Player looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="e21d8-148">Se non viene trovata alcuna corrispondenza, il lettore Visualizza all'utente una finestra di dialogo di avviso che richiede all'utente l'autorizzazione per tentare di riprodurre il file.</span><span class="sxs-lookup"><span data-stu-id="e21d8-148">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="e21d8-149">Se si creano file multimediali digitali con estensioni di file personalizzate, è possibile impedire che questo avviso venga visualizzato nel computer dell'utente registrando l'estensione del nome file e specificando una voce di **autorizzazione** .</span><span class="sxs-lookup"><span data-stu-id="e21d8-149">If you create digital media files with custom file name extensions, you can prevent this warning from appearing on the user's computer by registering the file name extension and providing a **Permissions** entry.</span></span>

<span data-ttu-id="e21d8-150">La voce relativa alle **autorizzazioni** (ad eccezione del valore del flag 128) è supportata dalla serie Windows Media Player 9 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e21d8-150">The **Permissions** entry (except for the flag value 128) is supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="e21d8-151">Il valore del flag 128 è supportato da Windows Media Player 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e21d8-151">The flag value 128 is supported by Windows Media Player 10 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e21d8-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e21d8-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e21d8-153">**Impostazioni del registro di sistema estensione del nome file**</span><span class="sxs-lookup"><span data-stu-id="e21d8-153">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




