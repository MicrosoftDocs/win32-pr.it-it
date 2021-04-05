---
title: Sottochiave ConvertPluginCLSID
description: Sottochiave ConvertPluginCLSID
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Media Player di Windows, sottochiave ConvertPluginCLSID
- Windows Media Player, estensioni di file
- Windows Media Player, registro di sistema
- Registro di sistema, estensioni di file
- Registro di sistema, sottochiave ConvertPluginCLSID
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema estensione del nome file
- Sottochiave ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044807"
---
# <a name="convertpluginclsid-subkey"></a><span data-ttu-id="876ea-111">Sottochiave ConvertPluginCLSID</span><span class="sxs-lookup"><span data-stu-id="876ea-111">ConvertPluginCLSID Subkey</span></span>

<span data-ttu-id="876ea-112">Quando Windows Media Player 11 rileva un'estensione del nome di file personalizzata, Cerca una sottochiave del registro di sistema corrispondente all'estensione.</span><span class="sxs-lookup"><span data-stu-id="876ea-112">When Windows Media Player 11 encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="876ea-113">La sottochiave è descritta in [impostazioni del registro di sistema estensione del nome file](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="876ea-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="876ea-114">In alcuni casi, la sottochiave dell'estensione contiene una sottochiave denominata **ConvertPluginCLSID**.</span><span class="sxs-lookup"><span data-stu-id="876ea-114">In some cases, the extension's subkey has a subkey named **ConvertPluginCLSID**.</span></span>

<span data-ttu-id="876ea-115">Si supponga, ad esempio, di aver creato un formato di file personalizzato (con estensione xyz) e un plug-in di conversione che converte i file in un formato supportato da Windows Media Player quindi archiviare l'ID classe del plug-in in una o entrambe le sottochiavi riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="876ea-115">For example, suppose you have created a custom file format (with file name extension .xyz) and a conversion plug-in that converts the files to a format supported by Windows Media Player Then you would store the class ID of the plug-in in one or both of the following subkeys.</span></span>

<span data-ttu-id="876ea-116">**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Multimedia \\ wmplayer \\ Extensions \\ . xyz \\ ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="876ea-116">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="876ea-117">**HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\ . xyz \\ ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="876ea-117">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="876ea-118">La sottochiave **ConvertPluginCLSID** specifica gli ID di classe dei plug-in che Windows Media Player può usare per convertire un file multimediale dal formato personalizzato in un formato supportato dal lettore.</span><span class="sxs-lookup"><span data-stu-id="876ea-118">The **ConvertPluginCLSID** subkey specifies the class IDs of plug-ins that Windows Media Player can use to convert a media file from its custom format to a format supported by the Player.</span></span>

<span data-ttu-id="876ea-119">La sottochiave **ConvertPluginCLSID** contiene le voci seguenti.</span><span class="sxs-lookup"><span data-stu-id="876ea-119">The **ConvertPluginCLSID** subkey has the following entries.</span></span>

-   <span data-ttu-id="876ea-120">Una voce predefinita che rappresenta il plug-in di conversione predefinito.</span><span class="sxs-lookup"><span data-stu-id="876ea-120">A default entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="876ea-121">Una voce denominata che rappresenta il plug-in di conversione predefinito.</span><span class="sxs-lookup"><span data-stu-id="876ea-121">A named entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="876ea-122">Voci denominate aggiuntive che rappresentano plug-in di conversione alternativi.</span><span class="sxs-lookup"><span data-stu-id="876ea-122">Additional named entries that represent alternate conversion plug-ins.</span></span>

<span data-ttu-id="876ea-123">Si supponga, ad esempio, che un formato di file personalizzato disponga di un plug-in di conversione predefinito e di due plug-in di conversione alternativi. Le voci del registro di sistema nella sottochiave **ConvertPluginCLSID** hanno il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="876ea-123">For example, suppose a custom file format has a default conversion plug-in and two alternate conversion plug-ins. The registry entries under the **ConvertPluginCLSID** subkey would have the following form.</span></span>



| <span data-ttu-id="876ea-124">Nome</span><span class="sxs-lookup"><span data-stu-id="876ea-124">Name</span></span>                                                                          | <span data-ttu-id="876ea-125">Type</span><span class="sxs-lookup"><span data-stu-id="876ea-125">Type</span></span>        | <span data-ttu-id="876ea-126">valore</span><span class="sxs-lookup"><span data-stu-id="876ea-126">Value</span></span>                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="876ea-127">Predefinito</span><span class="sxs-lookup"><span data-stu-id="876ea-127">Default</span></span>                                                                       | <span data-ttu-id="876ea-128">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="876ea-128">**REG\_SZ**</span></span> | <span data-ttu-id="876ea-129">ID classe nel formato del registro di sistema del plug-in di conversione predefinito.</span><span class="sxs-lookup"><span data-stu-id="876ea-129">The class ID, in registry format, of the default conversion plug-in.</span></span> |
| <span data-ttu-id="876ea-130">ID classe nel formato del registro di sistema del plug-in di conversione predefinito.</span><span class="sxs-lookup"><span data-stu-id="876ea-130">The class ID, in registry format, of the default conversion plug-in.</span></span>          | <span data-ttu-id="876ea-131">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="876ea-131">**REG\_SZ**</span></span> | <span data-ttu-id="876ea-132">Nome descrittivo del plug-in di conversione predefinito.</span><span class="sxs-lookup"><span data-stu-id="876ea-132">The friendly name of the default conversion plug-in.</span></span>                 |
| <span data-ttu-id="876ea-133">ID di classe, nel formato del registro di sistema, del primo plug-in di conversione alternativa.</span><span class="sxs-lookup"><span data-stu-id="876ea-133">The class ID, in registry format, of the first alternate conversion plug-in.</span></span>  | <span data-ttu-id="876ea-134">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="876ea-134">**REG\_SZ**</span></span> | <span data-ttu-id="876ea-135">Nome descrittivo del primo plug-in per la conversione alternativa.</span><span class="sxs-lookup"><span data-stu-id="876ea-135">The friendly name of the first alternate conversion plug-in.</span></span>         |
| <span data-ttu-id="876ea-136">ID di classe, nel formato del registro di sistema, del secondo plug-in di conversione alternativa.</span><span class="sxs-lookup"><span data-stu-id="876ea-136">The class ID, in registry format, of the second alternate conversion plug-in.</span></span> | <span data-ttu-id="876ea-137">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="876ea-137">**REG\_SZ**</span></span> | <span data-ttu-id="876ea-138">Nome descrittivo del secondo plug-in di conversione alternativa.</span><span class="sxs-lookup"><span data-stu-id="876ea-138">The friendly name of the second alternate conversion plug-in.</span></span>        |



 

<span data-ttu-id="876ea-139">Si noti che il plug-in di conversione predefinito è rappresentato da due voci del registro di sistema: la voce predefinita e una voce denominata.</span><span class="sxs-lookup"><span data-stu-id="876ea-139">Note that the default conversion plug-in is represented by two registry entries: the default entry and a named entry.</span></span> <span data-ttu-id="876ea-140">Windows Media Player utilizza la voce predefinita per determinare quale plug-in è il plug-in di conversione predefinito (primario).</span><span class="sxs-lookup"><span data-stu-id="876ea-140">Windows Media Player uses the default entry to determine which plug-in is the default (primary) conversion plug-in.</span></span> <span data-ttu-id="876ea-141">Windows Media Player usa le voci denominate per ottenere nomi descrittivi per tutti i plug-in di conversione, incluso il plug-in predefinito.</span><span class="sxs-lookup"><span data-stu-id="876ea-141">Windows Media Player uses the named entries to obtain friendly names for all conversion plug-ins, including the default plug-in.</span></span>

<span data-ttu-id="876ea-142">Il nome descrittivo di un plug-in di conversione è determinato dall'azienda che crea il plug-in.</span><span class="sxs-lookup"><span data-stu-id="876ea-142">The friendly name of a conversion plug-in is determined by the company that creates the plug-in.</span></span> <span data-ttu-id="876ea-143">Windows Media Player potrebbe visualizzare il nome descrittivo nella relativa interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="876ea-143">Windows Media Player might display the friendly name in its user interface.</span></span>

<span data-ttu-id="876ea-144">Quando Windows Media Player tenta di convertire un file da un formato personalizzato in un formato standard, carica innanzitutto il plug-in predefinito.</span><span class="sxs-lookup"><span data-stu-id="876ea-144">When Windows Media Player attempts to convert a file from a custom format to a standard format, it first loads the default plug-in.</span></span> <span data-ttu-id="876ea-145">Se il plug-in predefinito non riesce a convertire il file e restituisce il plug-in NS \_ e \_ WMP \_ Convert \_ plugin \_ Unknown \_ file \_ Owner, il lettore carica ogni plug-in alternativo fino a quando non si verifica una conversione corretta o non ci sono altri plug-in da provare.</span><span class="sxs-lookup"><span data-stu-id="876ea-145">If the default plug-in fails to convert the file and returns NS\_E\_WMP\_CONVERT\_PLUGIN\_UNKNOWN\_FILE\_OWNER, the Player loads each alternate plug-in until a successful conversion happens or there are no more plug-ins to try.</span></span> <span data-ttu-id="876ea-146">Il lettore non visualizza un messaggio di avviso se non viene trovato alcun plug-in di conversione per l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="876ea-146">The Player does not display a warning message if no conversion plug-in is found for the file name extension.</span></span>

<span data-ttu-id="876ea-147">La voce del registro di sistema **ConvertPluginCLSID** è supportata da Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="876ea-147">The **ConvertPluginCLSID** registry entry is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="876ea-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="876ea-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="876ea-149">**Impostazioni del registro di sistema estensione del nome file**</span><span class="sxs-lookup"><span data-stu-id="876ea-149">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> <dt>

[<span data-ttu-id="876ea-150">**Plug-in di conversione di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="876ea-150">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




