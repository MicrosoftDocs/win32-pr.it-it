---
title: Creazione di un pacchetto di download di Windows Media (deprecato)
description: Creazione di un pacchetto di download di Windows Media (deprecato)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Metafile di Windows Media, pacchetti di download di Windows Media
- Windows Media Player, pacchetti di download di Windows Media
- Metafile, pacchetti di download di Windows Media
- Windows Media, pacchetti di download di Windows Media
- Pacchetti di download di Windows Media, creazione
- creazione di pacchetti di download di Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044920"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a><span data-ttu-id="078b5-109">Creazione di un pacchetto di download di Windows Media (deprecato)</span><span class="sxs-lookup"><span data-stu-id="078b5-109">Creating a Windows Media Download Package (deprecated)</span></span>

<span data-ttu-id="078b5-110">Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="078b5-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="078b5-111">Per creare un pacchetto di download di Windows Media, attenersi alla seguente procedura.</span><span class="sxs-lookup"><span data-stu-id="078b5-111">Follow these steps to create a Windows Media Download package.</span></span>

1.  <span data-ttu-id="078b5-112">**Creare un bordo.**</span><span class="sxs-lookup"><span data-stu-id="078b5-112">**Create a border.**</span></span> <span data-ttu-id="078b5-113">Utilizzare le stesse tecniche utilizzate per creare un'interfaccia per Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="078b5-113">Use the same techniques you would use to build a skin for Windows Media Player.</span></span> <span data-ttu-id="078b5-114">Progettare il bordo in modo che il ridimensionamento di Windows Media Player non rovini la composizione degli elementi del bordo.</span><span class="sxs-lookup"><span data-stu-id="078b5-114">Design the border so that resizing Windows Media Player will not ruin the composition of the border elements.</span></span> <span data-ttu-id="078b5-115">Usare, ad esempio, una visualizzazione o un colore a tinta unita come sfondo, in quanto questi aumenteranno le prestazioni in base al ridimensionamento di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="078b5-115">For instance, use a solid color or visualization as a background because these will scale well as Windows Media Player is resized.</span></span>
2.  <span data-ttu-id="078b5-116">**Comprimere il contenuto del bordo.**</span><span class="sxs-lookup"><span data-stu-id="078b5-116">**Compress the border contents.**</span></span> <span data-ttu-id="078b5-117">Creare una cartella compressa (con estensione zip) che contiene i file di bordo: immagini, file JScript e il file di definizione dell'interfaccia con estensione WMS.</span><span class="sxs-lookup"><span data-stu-id="078b5-117">Create a compressed folder (with a .zip file name extension) that contains the border files: images, JScript files, and the skin definition file with a .wms file name extension.</span></span> <span data-ttu-id="078b5-118">Rinominare il file compresso in modo che disponga di un'estensione di file WMZ.</span><span class="sxs-lookup"><span data-stu-id="078b5-118">Rename the compressed file so that it has a .wmz file name extension.</span></span>
3.  <span data-ttu-id="078b5-119">**Scrivere un metafile di Windows Media.**</span><span class="sxs-lookup"><span data-stu-id="078b5-119">**Write a Windows Media metafile.**</span></span> <span data-ttu-id="078b5-120">Windows Media Player non caricherà il bordo a meno che non si crei un metafile Windows Media con un'estensione del nome di file. ASX che implementi l'elemento **Skin** .</span><span class="sxs-lookup"><span data-stu-id="078b5-120">Windows Media Player will not load the border unless you create a Windows Media metafile with an .asx file name extension that implements the **SKIN** element.</span></span> <span data-ttu-id="078b5-121">Il metafile può essere utilizzato anche per creare una playlist che descriva il contenuto incluso nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="078b5-121">The metafile can also be used to create a playlist that describes the content included in the package.</span></span>
4.  <span data-ttu-id="078b5-122">**Assemblare il contenuto.**</span><span class="sxs-lookup"><span data-stu-id="078b5-122">**Assemble your content.**</span></span> <span data-ttu-id="078b5-123">Inserire tutti i file che si desidera utilizzare in una cartella.</span><span class="sxs-lookup"><span data-stu-id="078b5-123">Put all the files that you want to use into a folder.</span></span> <span data-ttu-id="078b5-124">Sono inclusi file audio, file video, metafile e file di definizione dei bordi.</span><span class="sxs-lookup"><span data-stu-id="078b5-124">This includes audio files, video files, metafiles, and border definition files.</span></span>
5.  <span data-ttu-id="078b5-125">**Creare il pacchetto.**</span><span class="sxs-lookup"><span data-stu-id="078b5-125">**Create the package.**</span></span> <span data-ttu-id="078b5-126">Creare una cartella compressa (con estensione zip) che contiene il file del bordo, i file di contenuto e il metafile.</span><span class="sxs-lookup"><span data-stu-id="078b5-126">Create a compressed folder (with a .zip file name extension) that contains the border file, content files, and the metafile.</span></span> <span data-ttu-id="078b5-127">Modificare l'estensione del nome file del file con estensione zip in un'estensione di file WMD.</span><span class="sxs-lookup"><span data-stu-id="078b5-127">Change the file name extension of this .zip file to a .wmd file name extension.</span></span>
6.  <span data-ttu-id="078b5-128">**Pubblica il pacchetto in un sito Web.**</span><span class="sxs-lookup"><span data-stu-id="078b5-128">**Post the package to a website.**</span></span> <span data-ttu-id="078b5-129">Il pacchetto completato è pronto per essere pubblicato in un sito Web e scaricato dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="078b5-129">The completed package is ready to be posted to a website and downloaded by users.</span></span>

## <a name="related-topics"></a><span data-ttu-id="078b5-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="078b5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="078b5-131">**Pacchetti di download di Windows Media (deprecato)**</span><span class="sxs-lookup"><span data-stu-id="078b5-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




