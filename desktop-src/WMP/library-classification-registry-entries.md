---
title: Voci del registro di sistema di classificazione delle librerie
description: Voci del registro di sistema di classificazione delle librerie
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows Media Player, libreria
- Media Player di Windows, voci del registro di sistema di classificazione
- Windows Media Player, estensioni di file
- Windows Media Player, registro di sistema
- Registro di sistema, estensioni di file
- Registro di sistema, voci di classificazione delle librerie
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
- raccolta, voci del registro di sistema di classificazione
- libreria, registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298557"
---
# <a name="library-classification-registry-entries"></a><span data-ttu-id="3c16f-113">Voci del registro di sistema di classificazione delle librerie</span><span class="sxs-lookup"><span data-stu-id="3c16f-113">Library Classification Registry Entries</span></span>

<span data-ttu-id="3c16f-114">Quando Windows Media Player rileva un file multimediale con un'estensione di file personalizzata, non sa se il file deve essere classificato come audio, video o un altro tipo.</span><span class="sxs-lookup"><span data-stu-id="3c16f-114">When Windows Media Player encounters a media file that has a custom file name extension, it does not know whether the file should be classified as audio, video, or some other type.</span></span> <span data-ttu-id="3c16f-115">Per impostazione predefinita, Windows Media Player inserisce tali file nell'altra parte relativa ai supporti della libreria.</span><span class="sxs-lookup"><span data-stu-id="3c16f-115">By default, Windows Media Player places such files in the Other Media portion of the library.</span></span>

<span data-ttu-id="3c16f-116">Se i file multimediali digitali hanno un formato personalizzato, è possibile specificare Windows Media Player con le informazioni sulla posizione in cui i file devono essere visualizzati nella libreria del lettore inserendo due voci nel registro di sistema nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3c16f-116">If your digital media files have a custom format, you can provide Windows Media Player with information about where your files should appear in the Player's library by placing two entries in the registry on the user's computer.</span></span>

<span data-ttu-id="3c16f-117">Una voce viene inserita nella sottochiave seguente.</span><span class="sxs-lookup"><span data-stu-id="3c16f-117">One entry goes in the following subkey.</span></span>

<span data-ttu-id="3c16f-118">**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**</span><span class="sxs-lookup"><span data-stu-id="3c16f-118">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="3c16f-119">La voce del registro di sistema ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="3c16f-119">The registry entry has the following format.</span></span>



| <span data-ttu-id="3c16f-120">Nome</span><span class="sxs-lookup"><span data-stu-id="3c16f-120">Name</span></span>                                                  | <span data-ttu-id="3c16f-121">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3c16f-121">Data type</span></span>   | <span data-ttu-id="3c16f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3c16f-122">Value</span></span>                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| <span data-ttu-id="3c16f-123">Estensione del nome file senza il separatore punto (.)</span><span class="sxs-lookup"><span data-stu-id="3c16f-123">The file name extension without the dot (.) separator</span></span> | <span data-ttu-id="3c16f-124">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="3c16f-124">**REG\_SZ**</span></span> | <span data-ttu-id="3c16f-125">Stringa che specifica un percorso di libreria</span><span class="sxs-lookup"><span data-stu-id="3c16f-125">A string that specifies a library location</span></span> |



 

<span data-ttu-id="3c16f-126">L'altra voce del registro di sistema passa alla sottochiave seguente che è stata creata.</span><span class="sxs-lookup"><span data-stu-id="3c16f-126">The other registry entry goes in the following subkey that you create.</span></span>

<span data-ttu-id="3c16f-127">**HKEY \_ CustomExtension \_ radice \\ classi** </span><span class="sxs-lookup"><span data-stu-id="3c16f-127">**HKEY\_CLASSES\_ROOT\\** *customExtension*</span></span>

<span data-ttu-id="3c16f-128">dove *customExtension* è l'estensione del nome di file, incluso il separatore del punto (.).</span><span class="sxs-lookup"><span data-stu-id="3c16f-128">where *customExtension* is the file name extension including the dot (.) separator.</span></span>

<span data-ttu-id="3c16f-129">La voce del registro di sistema ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="3c16f-129">The registry entry has the following format.</span></span>



| <span data-ttu-id="3c16f-130">Nome</span><span class="sxs-lookup"><span data-stu-id="3c16f-130">Name</span></span>          | <span data-ttu-id="3c16f-131">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3c16f-131">Data type</span></span>   | <span data-ttu-id="3c16f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="3c16f-132">Value</span></span>                                      |
|---------------|-------------|--------------------------------------------|
| <span data-ttu-id="3c16f-133">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="3c16f-133">PerceivedType</span></span> | <span data-ttu-id="3c16f-134">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="3c16f-134">**REG\_SZ**</span></span> | <span data-ttu-id="3c16f-135">Stringa che specifica un percorso di libreria</span><span class="sxs-lookup"><span data-stu-id="3c16f-135">A string that specifies a library location</span></span> |



 

<span data-ttu-id="3c16f-136">Entrambe le voci del registro di sistema devono avere lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="3c16f-136">Both registry entries must have the same value.</span></span> <span data-ttu-id="3c16f-137">Nella tabella seguente sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="3c16f-137">Possible values are given in the following table.</span></span>



| <span data-ttu-id="3c16f-138">Valore</span><span class="sxs-lookup"><span data-stu-id="3c16f-138">Value</span></span> | <span data-ttu-id="3c16f-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c16f-139">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3c16f-140">Audio</span><span class="sxs-lookup"><span data-stu-id="3c16f-140">audio</span></span> | <span data-ttu-id="3c16f-141">I file con estensione personalizzata vengono visualizzati nella parte musicale della libreria.</span><span class="sxs-lookup"><span data-stu-id="3c16f-141">Files that have the custom extension appear in the music portion of the library.</span></span> |
| <span data-ttu-id="3c16f-142">Video</span><span class="sxs-lookup"><span data-stu-id="3c16f-142">video</span></span> | <span data-ttu-id="3c16f-143">I file con estensione personalizzata vengono visualizzati nella parte video della libreria.</span><span class="sxs-lookup"><span data-stu-id="3c16f-143">Files that have the custom extension appear in the video portion of the library.</span></span> |



 

<span data-ttu-id="3c16f-144">Ad esempio, le voci del registro di sistema seguenti specificano che i file con estensione xyz verranno visualizzati nella parte musicale della libreria:</span><span class="sxs-lookup"><span data-stu-id="3c16f-144">For example, the following registry entries specify that files having the file name extension .xyz will appear in the music portion of the library:</span></span>


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



<span data-ttu-id="3c16f-145">Si noti che il codice che tenta di scrivere nel registro di sistema nel computer dell'utente può scrivere nel \_ sottoalbero del computer locale HKEY \_ solo se l'utente corrente dispone di privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="3c16f-145">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="3c16f-146">Le voci del registro di sistema di classificazione delle librerie sono supportate dalle seguenti versioni di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3c16f-146">Library classification registry entries are supported by the following versions of Windows Media Player.</span></span>

-   <span data-ttu-id="3c16f-147">Windows Media Player 9 serie con hotfix 823275</span><span class="sxs-lookup"><span data-stu-id="3c16f-147">Windows Media Player 9 Series with hotfix 823275</span></span>
-   <span data-ttu-id="3c16f-148">Windows Media Player 10 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="3c16f-148">Windows Media Player 10 and later</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c16f-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c16f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c16f-150">**Impostazioni del registro di sistema estensione del nome file**</span><span class="sxs-lookup"><span data-stu-id="3c16f-150">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




