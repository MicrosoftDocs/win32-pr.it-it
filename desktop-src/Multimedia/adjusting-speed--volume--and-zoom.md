---
title: Regolazione della velocità, del volume e dello zoom
description: Regolazione della velocità, del volume e dello zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- MCIWndSetSpeed (macro)
- MCIWndGetSpeed (macro)
- MCIWndSetVolume (macro)
- MCIWndGetVolume (macro)
- MCIWndSetZoom (macro)
- MCIWndGetZoom (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396066"
---
# <a name="adjusting-speed-volume-and-zoom"></a><span data-ttu-id="ce4f2-109">Regolazione della velocità, del volume e dello zoom</span><span class="sxs-lookup"><span data-stu-id="ce4f2-109">Adjusting Speed, Volume, and Zoom</span></span>

<span data-ttu-id="ce4f2-110">Le macro velocità, volume e zoom forniscono le funzionalità dei comandi **Visualizza**, **volume** e **velocità** del menu MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-110">The speed, volume, and zoom macros provide the functionality of the **View**, **Volume**, and **Speed** commands on the MCIWnd menu.</span></span> <span data-ttu-id="ce4f2-111">Le macro descritte in questa sezione vengono in genere usate con video e altri dispositivi che visualizzano immagini durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-111">The macros described in this section are generally used with video and other devices that display images during playback.</span></span>

<span data-ttu-id="ce4f2-112">Alcuni dispositivi supportano più modifiche della velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-112">Some devices support multiple playback speed changes.</span></span> <span data-ttu-id="ce4f2-113">È possibile impostare la velocità di riproduzione per questi dispositivi usando la macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) .</span><span class="sxs-lookup"><span data-stu-id="ce4f2-113">You can set the playback speed for these devices by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span> <span data-ttu-id="ce4f2-114">Questa macro definisce la velocità di riproduzione come 1000.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-114">This macro defines the playback speed as 1000.</span></span> <span data-ttu-id="ce4f2-115">Valori più elevati indicano velocità più veloci.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-115">Higher values indicate faster speeds.</span></span> <span data-ttu-id="ce4f2-116">I valori inferiori indicano velocità più lente.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-116">Lower values indicate slower speeds.</span></span>

<span data-ttu-id="ce4f2-117">È possibile recuperare la velocità di riproduzione corrente usando la macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .</span><span class="sxs-lookup"><span data-stu-id="ce4f2-117">You can retrieve the current playback speed by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span> <span data-ttu-id="ce4f2-118">Questa macro USA gli stessi valori e l'intervallo di quelli usati da **MCIWndSetSpeed**.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-118">This macro uses the same values and range as those used by **MCIWndSetSpeed**.</span></span>

<span data-ttu-id="ce4f2-119">Alcuni dispositivi supportano le modifiche del volume.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-119">Some devices support volume changes.</span></span> <span data-ttu-id="ce4f2-120">È possibile modificare o impostare il volume utilizzando la macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .</span><span class="sxs-lookup"><span data-stu-id="ce4f2-120">You can adjust or set the volume by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span> <span data-ttu-id="ce4f2-121">Questa macro definisce il livello di volume normale come 1000.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-121">This macro defines the normal volume level as 1000.</span></span> <span data-ttu-id="ce4f2-122">I valori più alti indicano volumi più potenti.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-122">Higher values indicate louder volumes.</span></span> <span data-ttu-id="ce4f2-123">I valori inferiori indicano volumi più tranquilli.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-123">Lower values indicate quieter volumes.</span></span>

<span data-ttu-id="ce4f2-124">È possibile recuperare il livello del volume corrente usando la macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .</span><span class="sxs-lookup"><span data-stu-id="ce4f2-124">You can retrieve the current volume level by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span> <span data-ttu-id="ce4f2-125">Questa macro USA gli stessi valori numerici e gli stessi intervalli di quelli usati da **MCIWndSetVolume**.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-125">This macro uses the same numerical values and range as those used by **MCIWndSetVolume**.</span></span>

<span data-ttu-id="ce4f2-126">Per i dispositivi che usano una finestra di riproduzione, MCIWnd supporta una funzionalità di zoom che consente di impostare le dimensioni dell'immagine di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-126">For devices that use a playback window, MCIWnd supports a zoom feature that sets the size of the playback image.</span></span> <span data-ttu-id="ce4f2-127">È possibile impostare le dimensioni dell'immagine di riproduzione usando la macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .</span><span class="sxs-lookup"><span data-stu-id="ce4f2-127">You can set the playback image size by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span> <span data-ttu-id="ce4f2-128">La macro ridefinisce le dimensioni dell'immagine di riproduzione mantenendo una proporzione costante per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-128">The macro redefines the playback image size while maintaining a constant aspect ratio for the image.</span></span> <span data-ttu-id="ce4f2-129">Il valore di zoom viene definito come percentuale delle dimensioni originali dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-129">The zoom value is defined as a percentage of the original image size.</span></span> <span data-ttu-id="ce4f2-130">Pertanto, 100 rappresenta le dimensioni originali dell'immagine, 50 indica che l'immagine mostrata è la metà delle dimensioni originali e 200 indica che l'immagine mostrata è il doppio delle dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-130">Thus, 100 represents the original image size, 50 indicates the image shown is half its original size, and 200 indicates that the image shown is twice its original size.</span></span>

<span data-ttu-id="ce4f2-131">È possibile recuperare il valore di zoom corrente usando la macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .</span><span class="sxs-lookup"><span data-stu-id="ce4f2-131">You can retrieve the current zoom value by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span> <span data-ttu-id="ce4f2-132">Questa macro USA gli stessi valori e l'intervallo di quelli usati da **MCIWndSetZoom**.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-132">This macro uses the same values and range as those used by **MCIWndSetZoom**.</span></span>

> [!Note]  
> <span data-ttu-id="ce4f2-133">I driver audio e waveform CD di MCI standard non supportano le modifiche del volume o della velocità.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-133">The standard MCI CD audio and waveform-audio drivers do not support volume or speed changes.</span></span>

 

 

 




