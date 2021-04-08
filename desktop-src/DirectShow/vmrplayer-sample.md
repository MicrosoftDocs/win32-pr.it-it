---
description: Esempio VMRPlayer
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Esempio VMRPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880042"
---
# <a name="vmrplayer-sample"></a><span data-ttu-id="4521b-103">Esempio VMRPlayer</span><span class="sxs-lookup"><span data-stu-id="4521b-103">VMRPlayer Sample</span></span>

## <a name="description"></a><span data-ttu-id="4521b-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4521b-104">Description</span></span>

<span data-ttu-id="4521b-105">Questo esempio usa il filtro video mixaggio 9 (VMR-9) per la fusione alfa di uno o due video in esecuzione e un'immagine statica.</span><span class="sxs-lookup"><span data-stu-id="4521b-105">This sample uses the Video Mixing Renderer 9 (VMR-9) filter to alpha blend one or two running videos and a static image.</span></span>

## <a name="usage"></a><span data-ttu-id="4521b-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="4521b-106">Usage</span></span>

<span data-ttu-id="4521b-107">Per aprire il primo video, scegliere **Apri flusso primario** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="4521b-107">To open the first video, choose **Open Primary Stream** from the **File** menu.</span></span> <span data-ttu-id="4521b-108">Per aprire un secondo video, scegliere **Apri flusso secondario** dal menu **file** (è necessario prima aprire il flusso primario).</span><span class="sxs-lookup"><span data-stu-id="4521b-108">To open a second video, choose **Open Secondary Stream** from the **File** menu (you must open the primary stream first).</span></span> <span data-ttu-id="4521b-109">Per riprodurre il video, fare clic sul pulsante **Riproduci** .</span><span class="sxs-lookup"><span data-stu-id="4521b-109">To play the video, click the **Play** button.</span></span>

<span data-ttu-id="4521b-110">È possibile impostare la posizione, le dimensioni e i valori alfa dei video selezionando **flusso primario** o **flusso secondard** dal menu **Proprietà VMR** .</span><span class="sxs-lookup"><span data-stu-id="4521b-110">You can set the position, size, and alpha values of the videos by selecting **Primary Stream** or **Secondard Stream** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="4521b-111">Per aggiungere una bitmap statica sul video, scegliere **immagine app statica** dal menu **proprietà di VMR** e fare clic sulla casella **Visualizza immagine dell'app** .</span><span class="sxs-lookup"><span data-stu-id="4521b-111">To add a static bitmap over the video, choose **Static App Image** from the **VMR Properties** menu and click the **Display App Image** box.</span></span> <span data-ttu-id="4521b-112">È possibile utilizzare la stessa finestra di dialogo per controllare la posizione, le dimensioni e il valore alfa della bitmap.</span><span class="sxs-lookup"><span data-stu-id="4521b-112">You can use the same dialog to control the position, size, and alpha value of the bitmap.</span></span>

<span data-ttu-id="4521b-113">Per acquisire l'immagine del video mescolato, scegliere **Acquisisci immagine bitmap** dal menu **Proprietà VMR** .</span><span class="sxs-lookup"><span data-stu-id="4521b-113">To capture the blended video image, choose **Capture Bitmap Image** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="4521b-114">È anche possibile specificare il flusso di immagini primarie dalla riga di comando:</span><span class="sxs-lookup"><span data-stu-id="4521b-114">You can also specify the primary image stream from the command line:</span></span>

<span data-ttu-id="4521b-115">**VMRPlayer** **/p** *nomefile*</span><span class="sxs-lookup"><span data-stu-id="4521b-115">**VMRPlayer** **/P** *filename*</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="4521b-116">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="4521b-116">Downloading the Sample</span></span>

<span data-ttu-id="4521b-117">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4521b-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4521b-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4521b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4521b-119">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="4521b-119">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



