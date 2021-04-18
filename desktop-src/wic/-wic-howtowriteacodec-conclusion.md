---
description: La creazione di un codec sulla piattaforma Windows Imaging Component (WIC) consente a tutte le applicazioni basate su WIC di ottenere lo stesso supporto di piattaforma per il formato di immagine ottenuto per i formati di immagine comuni forniti con la piattaforma.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Conclusione (come scrivere un codec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312976"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="857b3-103">Conclusione (come scrivere un codec WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="857b3-103">Conclusion (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="857b3-104">La creazione di un codec sulla piattaforma Windows Imaging Component (WIC) consente a tutte le applicazioni basate su WIC di ottenere lo stesso supporto di piattaforma per il formato di immagine ottenuto per i formati di immagine comuni forniti con la piattaforma.</span><span class="sxs-lookup"><span data-stu-id="857b3-104">Building your codec on the Windows Imaging Component (WIC) platform makes it possible for all applications built on WIC to get the same platform support for your image format that they get for the common image formats shipped with the platform.</span></span> <span data-ttu-id="857b3-105">Consente inoltre la raccolta foto di Windows Vista, Esplora risorse e Visualizzatore foto per visualizzare anteprime e anteprime delle immagini nel formato usando il decodificatore fornito.</span><span class="sxs-lookup"><span data-stu-id="857b3-105">It also enables the Windows Vista Photo Gallery, Windows Explorer, and Photo Viewer to display thumbnails and previews of images in your format using the decoder that you provide.</span></span> <span data-ttu-id="857b3-106">Per i formati RAW, consente alle applicazioni di imaging più sofisticate di sfruttare le funzionalità di elaborazione non elaborate del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="857b3-106">For raw formats, it enables more sophisticated imaging applications to take advantage of your decoder’s raw processing capabilities.</span></span> <span data-ttu-id="857b3-107">A seconda delle opzioni del codificatore supportate, è anche possibile esporre funzionalità univoche del codificatore per consentire alle applicazioni di sfruttare al meglio le funzionalità avanzate del formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="857b3-107">Depending on the encoder options you support, you can also expose unique capabilities of your encoder to enable applications to take full advantage of the advanced features of your image format.</span></span>

<span data-ttu-id="857b3-108">Per lo sviluppo di un codec abilitato per WIC è necessario implementare alcune nuove interfacce.</span><span class="sxs-lookup"><span data-stu-id="857b3-108">Developing a WIC-enabled codec requires you to implement some new interfaces.</span></span> <span data-ttu-id="857b3-109">In molti casi, è possibile scrivere un wrapper per il codec esistente che implementa tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="857b3-109">In many cases, you can write a wrapper for your existing codec that implements these interfaces.</span></span> <span data-ttu-id="857b3-110">Quando si installa il codec, è necessario apportare alcune voci del registro di sistema per rendere individuabile il codec dalla piattaforma WIC e associarlo ai gestori di metadati appropriati.</span><span class="sxs-lookup"><span data-stu-id="857b3-110">When you install your codec, you must make some registry entries to make your codec discoverable by the WIC platform and associate it with the appropriate metadata handlers.</span></span> <span data-ttu-id="857b3-111">È anche necessario richiamare un'API per cancellare la cache delle anteprime delle anteprime predefinite (vuote) che potrebbero essere state precedentemente associate alle immagini nel formato.</span><span class="sxs-lookup"><span data-stu-id="857b3-111">You also need to invoke an API to clear the thumbnail cache of any default (empty) thumbnails that may have previously associated with images in your format.</span></span> <span data-ttu-id="857b3-112">Se lo si desidera, è possibile abilitare la raccolta foto di Windows Vista per fornire agli utenti un collegamento per scaricare il codec quando la raccolta foto rileva un'immagine con l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="857b3-112">If you want, you can enable the Windows Vista Photo Gallery to provide users with a link to download your codec when the Photo Gallery encounters an image with your file name extension.</span></span> <span data-ttu-id="857b3-113">A tale scopo, è necessario fornire a Microsoft informazioni sull'estensione del nome file del codec e sull'URL per il sito di download.</span><span class="sxs-lookup"><span data-stu-id="857b3-113">To do this, you must provide Microsoft with information about your codec’s file name extension and the URL for your download site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="857b3-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="857b3-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="857b3-115">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="857b3-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="857b3-116">Installazione e registrazione di CODEC</span><span class="sxs-lookup"><span data-stu-id="857b3-116">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="857b3-117">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="857b3-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="857b3-118">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="857b3-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



