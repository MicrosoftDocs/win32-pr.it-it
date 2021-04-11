---
title: Come funzionano i pacchetti di download di Windows Media (deprecato)
description: Come funzionano i pacchetti di download di Windows Media (deprecato)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Metafile di Windows Media, pacchetti di download di Windows Media
- Windows Media Player, pacchetti di download di Windows Media
- Metafile, pacchetti di download di Windows Media
- Windows Media, pacchetti di download di Windows Media
- Pacchetti di download di Windows Media, informazioni
- Pacchetti di download di Windows Media, funzionamento dei pacchetti
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116796"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a><span data-ttu-id="9dc09-109">Come funzionano i pacchetti di download di Windows Media (deprecato)</span><span class="sxs-lookup"><span data-stu-id="9dc09-109">How Windows Media Download Packages Work (deprecated)</span></span>

<span data-ttu-id="9dc09-110">Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="9dc09-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="9dc09-111">Un pacchetto di download di Windows Media viene avviato da un sito Web quando un utente fa clic su un collegamento in un Web browser, ad esempio Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9dc09-111">A Windows Media Download package is launched from a website when a user clicks a link in a Web browser, such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="9dc09-112">Questa azione apre Windows Media Player, quindi Scarica e Annulla il pacchetto del pacchetto di download di Windows Media sul disco rigido dell'utente in una cartella predefinita.</span><span class="sxs-lookup"><span data-stu-id="9dc09-112">This action opens Windows Media Player and then downloads and un-packages the Windows Media Download package on the user's hard disk in a default folder.</span></span>

<span data-ttu-id="9dc09-113">Una volta estratti i file dal pacchetto di download di Windows Media, Windows Media Player individua una playlist Windows Media Metafile con estensione di file ASX tra i file in pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9dc09-113">Once the files have been extracted from the Windows Media Download package, Windows Media Player locates a Windows Media metafile playlist with an .asx file name extension among the packaged files.</span></span> <span data-ttu-id="9dc09-114">Se ne trova uno, il lettore crea una playlist basata sul metafile incluso.</span><span class="sxs-lookup"><span data-stu-id="9dc09-114">If it finds one, the Player creates a playlist based on the included metafile.</span></span> <span data-ttu-id="9dc09-115">I file che contengono contenuto multimediale vengono quindi aggiunti alla libreria.</span><span class="sxs-lookup"><span data-stu-id="9dc09-115">Files that contain multimedia content are then added to the library.</span></span>

<span data-ttu-id="9dc09-116">Windows Media Player cerca anche un elemento **Skin** nel metafile.</span><span class="sxs-lookup"><span data-stu-id="9dc09-116">Windows Media Player also looks for a **SKIN** element in the metafile.</span></span> <span data-ttu-id="9dc09-117">Se l'elemento **Skin** contiene un riferimento a un file di bordo con estensione WMZ, il lettore carica il bordo nel riquadro **Now Playing** .</span><span class="sxs-lookup"><span data-stu-id="9dc09-117">If the **SKIN** element contains a reference to a border file with a .wmz file name extension, the Player loads the border into the **Now Playing** pane.</span></span> <span data-ttu-id="9dc09-118">Il lettore inizia quindi a riprodurre il contenuto fornito nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9dc09-118">The Player then starts to play the content provided in the package.</span></span>

<span data-ttu-id="9dc09-119">Il diagramma seguente illustra il modo in cui il contenuto viene inserito in un pacchetto in un file di download di Windows Media, pubblicato in un sito Web, scaricato e riprodotto in un computer client con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9dc09-119">The following diagram shows how content is packaged in a Windows Media Download file, posted to a website, downloaded, and played on a client computer using Windows Media Player.</span></span>

![come ottenere e riprodurre un file di download di Windows Media.](images/wmd-image.png) <span data-ttu-id="9dc09-121">Download di Windows Media</span><span class="sxs-lookup"><span data-stu-id="9dc09-121">Windows Media Download</span></span>

<span data-ttu-id="9dc09-122">Nella tabella seguente vengono descritti i tre elementi che costituiscono un pacchetto di download di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9dc09-122">The following table describes the three elements that make up a Windows Media Download package.</span></span>



| <span data-ttu-id="9dc09-123">Elemento Package</span><span class="sxs-lookup"><span data-stu-id="9dc09-123">Package element</span></span>    | <span data-ttu-id="9dc09-124">Funzione</span><span class="sxs-lookup"><span data-stu-id="9dc09-124">Function</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="9dc09-125">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="9dc09-125">File name extensions</span></span>                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="9dc09-126">Bordo</span><span class="sxs-lookup"><span data-stu-id="9dc09-126">Border</span></span>             | <span data-ttu-id="9dc09-127">Interfaccia utente fissa e personalizzata creata dal proprietario del contenuto per la visualizzazione, il collegamento e la riproduzione di tutti i supporti inclusi nel pacchetto di download di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9dc09-127">A fixed, customized user interface created by the content owner for displaying, linking, and playing all media packaged in the Windows Media Download package.</span></span> <span data-ttu-id="9dc09-128">Le tecniche utilizzate per creare i bordi sono simili a quelle utilizzate per creare le interfacce.</span><span class="sxs-lookup"><span data-stu-id="9dc09-128">The techniques used to create borders are similar to those used to create skins.</span></span> | <span data-ttu-id="9dc09-129">wmz</span><span class="sxs-lookup"><span data-stu-id="9dc09-129">.wmz</span></span>                                     |
| <span data-ttu-id="9dc09-130">Playlist metafile</span><span class="sxs-lookup"><span data-stu-id="9dc09-130">Metafile Playlist</span></span>  | <span data-ttu-id="9dc09-131">Metafile di Windows Media contenente elementi **voce** , informazioni sulla playlist e un'identità dell'elemento **Skin** per i file di contenuto.</span><span class="sxs-lookup"><span data-stu-id="9dc09-131">A Windows Media metafile that contains **ENTRY** elements, playlist information, and a **SKIN** element identity for content files.</span></span>                                                                                                             | <span data-ttu-id="9dc09-132">.asx</span><span class="sxs-lookup"><span data-stu-id="9dc09-132">.asx</span></span>                                     |
| <span data-ttu-id="9dc09-133">Contenuto multimediale</span><span class="sxs-lookup"><span data-stu-id="9dc09-133">Multimedia Content</span></span> | <span data-ttu-id="9dc09-134">File contenente qualsiasi formato audio o video supportato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9dc09-134">A file containing any audio or video format that is supported by Windows Media Player.</span></span>                                                                                                                                                          | <span data-ttu-id="9dc09-135">WMA, WMV, ASF, WAV, AVI, MPG, MP3</span><span class="sxs-lookup"><span data-stu-id="9dc09-135">.wma, .wmv, .asf, .wav, .avi, .mpg, .mp3</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9dc09-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9dc09-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dc09-137">**Pacchetti di download di Windows Media (deprecato)**</span><span class="sxs-lookup"><span data-stu-id="9dc09-137">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




