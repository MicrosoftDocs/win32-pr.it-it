---
title: Voci di sistema per compresser, decompressori e renderer
description: Voci di sistema per compresser, decompressori e renderer
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Video per Windows (VFW), voci di sistema compressore
- VFW (video per Windows), voci di sistema compressore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713300"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a><span data-ttu-id="158ec-105">Voci di sistema per compresser, decompressori e renderer</span><span class="sxs-lookup"><span data-stu-id="158ec-105">System Entries for Compressors, Decompressors, and Renderers</span></span>

<span data-ttu-id="158ec-106">Il sistema usa le voci nel registro di sistema per trovare i driver VCM.</span><span class="sxs-lookup"><span data-stu-id="158ec-106">The system uses entries in the registry to find VCM drivers.</span></span> <span data-ttu-id="158ec-107">Queste voci sono costituite da codici a 2 4 caratteri separati da un punto.</span><span class="sxs-lookup"><span data-stu-id="158ec-107">These entries are in the form of two four-character codes separated by a period.</span></span> <span data-ttu-id="158ec-108">Il primo codice di quattro caratteri viene definito dal sistema e può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="158ec-108">The first four-character code is defined by the system and can be one of the following:</span></span>



| <span data-ttu-id="158ec-109">Codice a quattro caratteri</span><span class="sxs-lookup"><span data-stu-id="158ec-109">Four-character code</span></span> | <span data-ttu-id="158ec-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="158ec-110">Description</span></span>                               |
|---------------------|-------------------------------------------|
| <span data-ttu-id="158ec-111">VIDC</span><span class="sxs-lookup"><span data-stu-id="158ec-111">"VIDC"</span></span>              | <span data-ttu-id="158ec-112">Identifica i comprimeri e i decompressori.</span><span class="sxs-lookup"><span data-stu-id="158ec-112">Identifies compressors and decompressors.</span></span> |
| <span data-ttu-id="158ec-113">VIDS</span><span class="sxs-lookup"><span data-stu-id="158ec-113">"VIDS"</span></span>              | <span data-ttu-id="158ec-114">Identifica i renderer del flusso video.</span><span class="sxs-lookup"><span data-stu-id="158ec-114">Identifies video-stream renderers.</span></span>        |
| <span data-ttu-id="158ec-115">TXTS</span><span class="sxs-lookup"><span data-stu-id="158ec-115">"TXTS"</span></span>              | <span data-ttu-id="158ec-116">Identifica i renderer del flusso di testo.</span><span class="sxs-lookup"><span data-stu-id="158ec-116">Identifies text-stream renderers.</span></span>         |
| <span data-ttu-id="158ec-117">"AUDS"</span><span class="sxs-lookup"><span data-stu-id="158ec-117">"AUDS"</span></span>              | <span data-ttu-id="158ec-118">Identifica i gestori del flusso audio.</span><span class="sxs-lookup"><span data-stu-id="158ec-118">Identifies audio-stream handlers.</span></span>         |



 

<span data-ttu-id="158ec-119">I renderer personalizzati possono definire i propri codici a quattro caratteri.</span><span class="sxs-lookup"><span data-stu-id="158ec-119">Custom renderers can define their own four-character codes.</span></span>

<span data-ttu-id="158ec-120">Il secondo codice a quattro caratteri viene definito dal driver.</span><span class="sxs-lookup"><span data-stu-id="158ec-120">The second four-character code is defined by the driver.</span></span> <span data-ttu-id="158ec-121">In genere, il secondo codice a quattro caratteri corrisponde al tipo di dati che il driver è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="158ec-121">Typically, the second four-character code corresponds to the type of data the driver can handle.</span></span>

<span data-ttu-id="158ec-122">Quando si apre un driver VCM, un'applicazione specifica il tipo di driver e il tipo di gestore di dati necessari.</span><span class="sxs-lookup"><span data-stu-id="158ec-122">When opening a VCM driver, an application specifies the type of driver and the type of data handler it needs.</span></span> <span data-ttu-id="158ec-123">In genere, queste informazioni provengono dall'intestazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="158ec-123">Typically, this information comes from the stream header.</span></span> <span data-ttu-id="158ec-124">Il sistema tenta di aprire il gestore di dati specificato; in caso contrario, il sistema esegue una ricerca nel registro di sistema di un driver con il gestore obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="158ec-124">The system tries to open the specified data handler, but if it fails, the system searches the registry for a driver that has the required handler.</span></span>

<span data-ttu-id="158ec-125">Quando si esegue la ricerca del driver, il sistema tenta di trovare una corrispondenza tra i codici di quattro caratteri specificati per il tipo di driver e il gestore di dati con quelli specificati nella voce del driver.</span><span class="sxs-lookup"><span data-stu-id="158ec-125">When searching for the driver, the system tries to match the four-character codes specified for the driver type and data handler with those specified in the driver entry.</span></span> <span data-ttu-id="158ec-126">Se, ad esempio, in un'applicazione viene specificato il compressore MSSQ, il sistema cerca nel registro di sistema la voce di driver VIDC. MSSQ.</span><span class="sxs-lookup"><span data-stu-id="158ec-126">For example, if an application specifies the compressor MSSQ, the system searches the registry for the driver entry VIDC.MSSQ.</span></span> <span data-ttu-id="158ec-127">Se non riesce a trovare una corrispondenza, apre ogni driver corrispondente al tipo di driver e ne individua uno in grado di gestire il tipo di dati specificato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="158ec-127">If it cannot find a match, it opens each driver corresponding to the driver type and locates one that can handle the type of data your application specifies.</span></span> <span data-ttu-id="158ec-128">Nell'esempio precedente, se il sistema non è stato in grado di trovare VIDC. MSSQ, apre tutti i driver con il codice a quattro caratteri "VIDC" e ne individua uno in grado di gestire i dati.</span><span class="sxs-lookup"><span data-stu-id="158ec-128">In the previous example, if the system could not find VIDC.MSSQ, it would open all drivers with the "VIDC" four-character code and locate one that can handle the data.</span></span>

 

 




