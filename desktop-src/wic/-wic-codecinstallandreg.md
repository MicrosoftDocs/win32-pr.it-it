---
description: Quando si installa un codec, è necessario registrarlo nel registro di sistema. È inoltre necessario assicurarsi che la cache delle anteprime venga aggiornata nel caso in cui siano presenti immagini nel formato già presenti nel computer.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Installazione e registrazione di codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313417"
---
# <a name="codec-installation-and-registration"></a><span data-ttu-id="3b4a3-104">Installazione e registrazione di codec</span><span class="sxs-lookup"><span data-stu-id="3b4a3-104">Codec Installation and Registration</span></span>

<span data-ttu-id="3b4a3-105">Quando si installa un codec, è necessario registrarlo nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-105">When you install a codec, you must register it in the registry.</span></span> <span data-ttu-id="3b4a3-106">È inoltre necessario assicurarsi che la cache delle anteprime venga aggiornata nel caso in cui siano presenti immagini nel formato già presenti nel computer.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-106">You must also make sure the thumbnail cache gets updated in case any images in your format already exist on the computer.</span></span>

<span data-ttu-id="3b4a3-107">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b4a3-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="3b4a3-108">Registrazione di un codec</span><span class="sxs-lookup"><span data-stu-id="3b4a3-108">Registering a Codec</span></span>](#registering-a-codec)
-   [<span data-ttu-id="3b4a3-109">Aggiornamento della cache delle anteprime durante l'installazione del codec</span><span class="sxs-lookup"><span data-stu-id="3b4a3-109">Updating the Thumbnail Cache When Installing Your Codec</span></span>](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [<span data-ttu-id="3b4a3-110">Rendere disponibile il codec WIC-Enabled per gli utenti</span><span class="sxs-lookup"><span data-stu-id="3b4a3-110">Making Your WIC-Enabled Codec Available To Users</span></span>](#making-your-wic-enabled-codec-available-to-users)
-   [<span data-ttu-id="3b4a3-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b4a3-111">Related topics</span></span>](#related-topics)

## <a name="registering-a-codec"></a><span data-ttu-id="3b4a3-112">Registrazione di un codec</span><span class="sxs-lookup"><span data-stu-id="3b4a3-112">Registering a Codec</span></span>

<span data-ttu-id="3b4a3-113">Quando si registra un codec, si registrano in realtà due componenti, ovvero il codificatore e il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-113">When you register a codec, you are actually registering two components: the encoder and the decoder.</span></span> <span data-ttu-id="3b4a3-114">È anche necessario creare voci del registro di sistema per registrare il formato del contenitore con i gestori dei metadati per i formati di metadati supportati dal formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-114">You also need to make registry entries to register your container format with the metadata handlers for the metadata formats that your image format supports.</span></span>

<span data-ttu-id="3b4a3-115">Negli argomenti seguenti vengono descritte le voci del registro di sistema necessarie per registrare il codec:</span><span class="sxs-lookup"><span data-stu-id="3b4a3-115">The following topics describe the registry entries you need to register your codec:</span></span>

[<span data-ttu-id="3b4a3-116">Voci generali del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="3b4a3-116">General Registry Entries</span></span>](-wic-generalregentries.md)

[<span data-ttu-id="3b4a3-117">Voci del registro di sistema specifiche del codificatore</span><span class="sxs-lookup"><span data-stu-id="3b4a3-117">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)

[<span data-ttu-id="3b4a3-118">Voci del registro di sistema specifiche del decodificatore</span><span class="sxs-lookup"><span data-stu-id="3b4a3-118">Decoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)

[<span data-ttu-id="3b4a3-119">Integrazione con raccolta foto di Windows e Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="3b4a3-119">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a><span data-ttu-id="3b4a3-120">Aggiornamento della cache delle anteprime durante l'installazione del codec</span><span class="sxs-lookup"><span data-stu-id="3b4a3-120">Updating the Thumbnail Cache When Installing Your Codec</span></span>

<span data-ttu-id="3b4a3-121">Quando viene installato un codec, il programma di installazione deve chiamare la funzione seguente dopo aver scritto le relative voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-121">When a codec is installed, the installer needs to call the following function after writing its registry entries.</span></span>


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



<span data-ttu-id="3b4a3-122">Questa chiamata notifica a Windows che sono disponibili nuove informazioni sull'associazione di file.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-122">This call notifies Windows that new file association information is available.</span></span> <span data-ttu-id="3b4a3-123">Se nel computer sono già presenti immagini nel formato immagine, la cache delle anteprime conterrà le anteprime predefinite perché non è disponibile alcun decodificatore per estrarre le anteprime quando le immagini sono state acquisite per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-123">If images in your image format already exist on the computer, the thumbnail cache will contain default thumbnails for them because no decoder was available to extract the thumbnails when the images were first acquired.</span></span> <span data-ttu-id="3b4a3-124">Quando si notifica a Windows che è disponibile una nuova associazione di file, la cache delle anteprime Elimina eventuali anteprime vuote ed estrae le anteprime effettive dai file che possono essere decodificati.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-124">When you notify Windows that a new file association is available, the thumbnail cache discards any empty thumbnails and extracts the actual thumbnails from the files that can now be decoded.</span></span>

## <a name="making-your-wic-enabled-codec-available-to-users"></a><span data-ttu-id="3b4a3-125">Rendere disponibile il codec WIC-Enabled per gli utenti</span><span class="sxs-lookup"><span data-stu-id="3b4a3-125">Making Your WIC-Enabled Codec Available To Users</span></span>

<span data-ttu-id="3b4a3-126">Se sei un produttore di fotocamere, puoi spedire i tuoi codec non elaborati con le tue fotocamere.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-126">If you are a camera manufacturer, you can ship your raw codecs in the box with your cameras.</span></span> <span data-ttu-id="3b4a3-127">È anche possibile pubblicare i codec nella pagina di download del sito Web.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-127">You can also post your codecs on the Download page of your Web site.</span></span> <span data-ttu-id="3b4a3-128">Tuttavia, se un utente acquisisce un file di immagine nel formato da un'altra origine, ad esempio un amico, un socio aziendale o un altro sito Web, potrebbe non essere in grado di individuare la posizione in cui il codec deve decodificare.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-128">However, if a user acquires an image file in your format from some other source, such as a friend, business associate, or some other Web site, they may not know where to get the codec to decode it with.</span></span>

<span data-ttu-id="3b4a3-129">A causa di questo problema, Windows offre agli utenti un modo più semplice per trovare il codec e scaricarlo nel computer, a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-129">Because of this issue, Windows offers an easier way for users of your image format to find your codec and download it onto their computer, starting with Windows Vista.</span></span> <span data-ttu-id="3b4a3-130">Se la raccolta foto di Windows riconosce un'estensione di file come formato di immagine e il codec per tale formato non è installato, una finestra di dialogo indica all'utente che non è possibile visualizzare la foto e chiede se l'utente vuole scaricare il software necessario per visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-130">If the Windows Photo Gallery recognizes a file name extension as an image format, and the codec for that format is not installed, a dialog box tells the user that the photo can’t be displayed, and asks whether the user wants to download the software required to display it.</span></span> <span data-ttu-id="3b4a3-131">Quando l'utente accetta, un sito Web ospitato da Microsoft viene visualizzato con un collegamento al sito di download del produttore di codec.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-131">When the user accepts, a Microsoft-hosted Web site appears with a link to the codec manufacturer’s download site.</span></span> <span data-ttu-id="3b4a3-132">Facoltativamente, è possibile richiedere che gli utenti vengano portati direttamente al sito di download.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-132">(Optionally, you can request that users be taken directly to your download site.)</span></span>

<span data-ttu-id="3b4a3-133">Se si vuole che le estensioni di file del formato di immagine siano riconosciute dalla raccolta foto di Windows in modo che gli utenti possano essere indirizzati al sito di download, è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b4a3-133">If you want your image format’s file name extensions to be recognized by the Windows Photo Gallery so that users can be directed to your download site, you must do the following:</span></span>

1.  <span data-ttu-id="3b4a3-134">Fornire un sito di download per il codec.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-134">Provide a download site for your codec.</span></span> <span data-ttu-id="3b4a3-135">È possibile avere una pagina separata per ogni codec fornito o una pagina che fornisce i download per tutti i codec.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-135">(You can have a separate page for each codec you provide, or one page that provides downloads for all your codecs.)</span></span>

    <span data-ttu-id="3b4a3-136">Il sito di download deve essere localizzato e facilmente ricercabile con il modello di fotocamera.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-136">The download site should be localized and easily searchable by camera model.</span></span>

2.  <span data-ttu-id="3b4a3-137">Fornire a Microsoft un elenco di estensioni per i formati di immagine e gli URL per i siti di download.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-137">Provide Microsoft with a list of extensions for your image formats, and the URLs for your download sites.</span></span>

<span data-ttu-id="3b4a3-138">È necessario informare Microsoft delle estensioni per tutti i nuovi codec sviluppati in futuro e di eventuali modifiche apportate agli URL dei siti di download, in modo da poter aggiungere le nuove informazioni alla raccolta foto di Windows.</span><span class="sxs-lookup"><span data-stu-id="3b4a3-138">You must inform Microsoft of the extensions for any new codecs you develop in the future, and of any changes to the URLs of your download sites, so that the new information can be added to the Windows Photo Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b4a3-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b4a3-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3b4a3-140">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="3b4a3-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3b4a3-141">Implementazione di IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="3b4a3-141">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="3b4a3-142">Conclusione (come scrivere un CODEC WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="3b4a3-142">Conclusion (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[<span data-ttu-id="3b4a3-143">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="3b4a3-143">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="3b4a3-144">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="3b4a3-144">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



