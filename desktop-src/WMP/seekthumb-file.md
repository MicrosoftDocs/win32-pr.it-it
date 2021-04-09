---
title: File SeekThumb
description: File SeekThumb
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, file SeekThumbd
- Windows Media Player Mobile Skins, file SeekThumb
- interfacce, file SeekThumb
- SeekThumb i file nelle interfacce
- Thumb, file SeekThumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f1e9434a614dbc02e48b63508c7c2c04f553d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955604"
---
# <a name="seekthumb-file"></a><span data-ttu-id="6a24e-111">File SeekThumb</span><span class="sxs-lookup"><span data-stu-id="6a24e-111">SeekThumb File</span></span>

<span data-ttu-id="6a24e-112">Il file SeekThumb definisce l'immagine che indica il percorso di riproduzione all'interno dell'elemento multimediale per un TrackBar Seek.</span><span class="sxs-lookup"><span data-stu-id="6a24e-112">The SeekThumb file defines the image that indicates the playback location within the media item for a Seek trackbar.</span></span> <span data-ttu-id="6a24e-113">È possibile usare un file e definirlo per l'uso da parte di SeekThumb e VolumeThumb.</span><span class="sxs-lookup"><span data-stu-id="6a24e-113">You can use one file and define it for use by both SeekThumb and VolumeThumb.</span></span> <span data-ttu-id="6a24e-114">Diversamente dagli altri file grafici, i file Thumb vengono definiti nella sezione trackbars del file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6a24e-114">Unlike the other art files, the thumb files are defined in the Trackbars section of the skin definition file.</span></span>

<span data-ttu-id="6a24e-115">L'immagine seguente è un file SeekThumb tipico.</span><span class="sxs-lookup"><span data-stu-id="6a24e-115">The following image is a typical SeekThumb file.</span></span>

![file seekthumb](images/cesdksee.gif)

<span data-ttu-id="6a24e-117">Questi due file di pulsanti hanno lo stesso aspetto ma hanno dimensioni leggermente diverse.</span><span class="sxs-lookup"><span data-stu-id="6a24e-117">These two button files look the same but are slightly different sizes.</span></span> <span data-ttu-id="6a24e-118">L'immagine a sinistra è la visualizzazione normale visualizzata dall'utente e l'immagine corretta è l'immagine push visualizzata dall'utente quando tocca il pulsante.</span><span class="sxs-lookup"><span data-stu-id="6a24e-118">The left image is the normal view that the user sees, and the right image is the Pushed image the user sees when they tap on the button.</span></span>

> [!Note]  
> <span data-ttu-id="6a24e-119">I file di SeekThumb Art creati per le interfacce usate in Windows Media Player 10 mobile o versioni successive devono avere le tre immagini seguenti (da sinistra a destra): normale, push e disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6a24e-119">SeekThumb art files created for skins used in Windows Media Player 10 Mobile or later must have the following three images (from left to right): normal, pushed, and disabled.</span></span>

 

<span data-ttu-id="6a24e-120">Potrebbe essere necessario rendere trasparente alcune aree delle immagini Thumb.</span><span class="sxs-lookup"><span data-stu-id="6a24e-120">You may want to make certain areas of the thumb images transparent.</span></span> <span data-ttu-id="6a24e-121">Ciò consentirà di creare immagini Thumb in forme diverse da rettangolare.</span><span class="sxs-lookup"><span data-stu-id="6a24e-121">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="6a24e-122">Qualsiasi area di un'immagine Thumb riempita con il colore specificato dal valore RGB 255, 0, 255 verrà visualizzata trasparente nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6a24e-122">Any region of a thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a24e-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a24e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a24e-124">**File di immagine**</span><span class="sxs-lookup"><span data-stu-id="6a24e-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




