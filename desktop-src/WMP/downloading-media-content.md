---
title: Download del contenuto multimediale
description: Download del contenuto multimediale
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Windows Media Player Online Stores, download del contenuto multimediale
- negozi online, download di contenuti multimediali
- digitare 1 negozi online, download del contenuto multimediale
- Windows Media Player Online Stores, download di contenuti multimediali
- negozi online, download di contenuti multimediali
- digitare 1 negozi online, download di contenuti multimediali
- contenuti multimediali, download
- Download del contenuto multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00efe44f2bac25a9eeda86f6adcc78b34beea7cd
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104398750"
---
# <a name="downloading-media-content"></a><span data-ttu-id="dfb8b-111">Download del contenuto multimediale</span><span class="sxs-lookup"><span data-stu-id="dfb8b-111">Downloading Media Content</span></span>

<span data-ttu-id="dfb8b-112">Windows Media Player gestisce i download dei file musicali per lo Store online.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-112">Windows Media Player handles music file downloads for the online store.</span></span> <span data-ttu-id="dfb8b-113">È possibile avviare un download quando la pagina di individuazione chiama [External. download](external-download.md) o quando l'utente sceglie, nel lettore, di scaricare un set di tracce.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-113">A download can be initiated when the discovery page calls [External.download](external-download.md) or when the user chooses, in the Player, to download a set of tracks.</span></span> <span data-ttu-id="dfb8b-114">In entrambi i casi, Windows Media Player chiama [IWMPContentPartner::D ownload](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passando un elenco di contenitori di contenuto che descrive il set di tracce da scaricare e un cookie che rappresenta la transazione di download.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-114">In either case, Windows Media Player calls [IWMPContentPartner::Download](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passing a content container list that describes the set of tracks to be downloaded and a cookie that represents the download transaction.</span></span> <span data-ttu-id="dfb8b-115">Il plug-in del partner di contenuti deve quindi chiamare [IWMPContentPartnerCallback::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) una volta per ogni traccia nel set.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-115">The content partner plug-in must then call [IWMPContentPartnerCallback::DownloadTrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) once for each track in the set.</span></span> <span data-ttu-id="dfb8b-116">Quando il plug-in chiama **DownloadTrack**, viene passato un valore **HRESULT** nel parametro *hrDownload* .</span><span class="sxs-lookup"><span data-stu-id="dfb8b-116">When the plug-in calls **DownloadTrack**, it passes an **HRESULT** in the *hrDownload* parameter.</span></span> <span data-ttu-id="dfb8b-117">Se il plug-in passa un codice di esito positivo in *hrDownload*, Windows Media Player Scarica la traccia. Se il plug-in passa un codice di errore in *hrDownload*, il lettore non Scarica la traccia. Per ogni chiamata a **download**, il plug-in deve fornire il cookie di transazione e l'ID della traccia in questione.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-117">If the plug-in passes a success code in *hrDownload*, Windows Media Player downloads the track. If the plug-in passes a failure code in *hrDownload*, the Player does not download the track. For each call to **Download**, the plug-in must supply the transaction cookie and the ID of the track in question.</span></span> <span data-ttu-id="dfb8b-118">Per le tracce che verranno effettivamente scaricate, il plug-in deve fornire anche l'URL della traccia.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-118">For tracks that will actually be downloaded, the plug-in must also supply the URL of the track.</span></span>

<span data-ttu-id="dfb8b-119">Dopo il download di un file, Windows Media Player aggiorna automaticamente la libreria in modo da riflettere la musica appena acquistata.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-119">After a file is downloaded, Windows Media Player automatically updates the library to reflect the newly purchased music.</span></span> <span data-ttu-id="dfb8b-120">Il lettore fornisce informazioni sullo stato per il plug-in sull'operazione di download chiamando [IWMPContentPartner::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span><span class="sxs-lookup"><span data-stu-id="dfb8b-120">The Player provides status information to the plug-in about the download operation by calling [IWMPContentPartner::DownloadTrackComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span></span> <span data-ttu-id="dfb8b-121">In questo metodo, il lettore fornisce un **HRESULT** per indicare l'esito positivo o negativo del download, l'ID di traccia e la stringa di parametri personalizzati fornita dal negozio online quando ha chiamato **DownloadTrack**.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-121">In this method, the Player provides an **HRESULT** to indicate success or failure of the download, the track ID, and the custom parameters string that the online store provided when it called **DownloadTrack**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfb8b-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dfb8b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfb8b-123">**Guida per programmatori per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="dfb8b-123">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




