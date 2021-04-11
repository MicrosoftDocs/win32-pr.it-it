---
title: Attributi con più valori (Windows Media Format 11 SDK)
description: Attributi con più valori
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK, attributi
- ASF (Advanced Systems Format), attributi
- ASF (formato avanzato dei sistemi), attributi
- attributi, più valori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047708"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="93aeb-107">Attributi con più valori (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="93aeb-107">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="93aeb-108">Alcuni degli attributi predefiniti possono avere più valori assegnati.</span><span class="sxs-lookup"><span data-stu-id="93aeb-108">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="93aeb-109">Ad esempio, **Artist** è un attributo che può avere più valori.</span><span class="sxs-lookup"><span data-stu-id="93aeb-109">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="93aeb-110">È possibile chiamare [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) più volte per aggiungere tutti i valori degli **artisti** necessari.</span><span class="sxs-lookup"><span data-stu-id="93aeb-110">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="93aeb-111">Se si eseguono più chiamate a **AddAttribute** per gli attributi che non supportano più valori, il metodo può restituire un codice di errore o semplicemente ignorare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="93aeb-111">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="93aeb-112">Nella tabella seguente sono elencati gli attributi che supportano più valori.</span><span class="sxs-lookup"><span data-stu-id="93aeb-112">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="93aeb-113">Alcuni attributi possono avere più valori solo nei file ASF, mentre altri possono avere più valori sia nei file ASF che in quelli MP3.</span><span class="sxs-lookup"><span data-stu-id="93aeb-113">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="93aeb-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="93aeb-114">Attribute</span></span>                                                 | <span data-ttu-id="93aeb-115">Supporto per più valori</span><span class="sxs-lookup"><span data-stu-id="93aeb-115">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="93aeb-116">**Autore**</span><span class="sxs-lookup"><span data-stu-id="93aeb-116">**Author**</span></span>](author.md)                                  | <span data-ttu-id="93aeb-117">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="93aeb-117">ASF, MP3</span></span>                    |
| [<span data-ttu-id="93aeb-118">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="93aeb-118">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="93aeb-119">ASF</span><span class="sxs-lookup"><span data-stu-id="93aeb-119">ASF</span></span>                         |
| [<span data-ttu-id="93aeb-120">**WM/AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="93aeb-120">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="93aeb-121">ASF</span><span class="sxs-lookup"><span data-stu-id="93aeb-121">ASF</span></span>                         |
| [<span data-ttu-id="93aeb-122">**WM/categoria**</span><span class="sxs-lookup"><span data-stu-id="93aeb-122">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="93aeb-123">ASF</span><span class="sxs-lookup"><span data-stu-id="93aeb-123">ASF</span></span>                         |
| [<span data-ttu-id="93aeb-124">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="93aeb-124">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="93aeb-125">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="93aeb-125">ASF, MP3</span></span>                    |
| [<span data-ttu-id="93aeb-126">**WM/conduttore**</span><span class="sxs-lookup"><span data-stu-id="93aeb-126">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="93aeb-127">ASF</span><span class="sxs-lookup"><span data-stu-id="93aeb-127">ASF</span></span>                         |
| [<span data-ttu-id="93aeb-128">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="93aeb-128">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="93aeb-129">ASF</span><span class="sxs-lookup"><span data-stu-id="93aeb-129">ASF</span></span>                         |
| [<span data-ttu-id="93aeb-130">**WM/genre**</span><span class="sxs-lookup"><span data-stu-id="93aeb-130">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="93aeb-131">ASF</span><span class="sxs-lookup"><span data-stu-id="93aeb-131">ASF</span></span>                         |
| [<span data-ttu-id="93aeb-132">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="93aeb-132">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="93aeb-133">ASF</span><span class="sxs-lookup"><span data-stu-id="93aeb-133">ASF</span></span>                         |
| [<span data-ttu-id="93aeb-134">**WM/lingua**</span><span class="sxs-lookup"><span data-stu-id="93aeb-134">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="93aeb-135">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="93aeb-135">ASF, MP3</span></span>                    |
| [<span data-ttu-id="93aeb-136">**WM/lyrics \_ sincronizzati**</span><span class="sxs-lookup"><span data-stu-id="93aeb-136">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="93aeb-137">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="93aeb-137">ASF, MP3</span></span>                    |
| [<span data-ttu-id="93aeb-138">**WM/umore**</span><span class="sxs-lookup"><span data-stu-id="93aeb-138">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="93aeb-139">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="93aeb-139">ASF, MP3</span></span>                    |
| [<span data-ttu-id="93aeb-140">**WM/immagine**</span><span class="sxs-lookup"><span data-stu-id="93aeb-140">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="93aeb-141">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="93aeb-141">ASF, MP3</span></span>                    |
| [<span data-ttu-id="93aeb-142">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="93aeb-142">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="93aeb-143">ASF</span><span class="sxs-lookup"><span data-stu-id="93aeb-143">ASF</span></span>                         |
| [<span data-ttu-id="93aeb-144">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="93aeb-144">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="93aeb-145">ASF</span><span class="sxs-lookup"><span data-stu-id="93aeb-145">ASF</span></span>                         |
| [<span data-ttu-id="93aeb-146">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="93aeb-146">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="93aeb-147">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="93aeb-147">ASF, MP3</span></span>                    |
| [<span data-ttu-id="93aeb-148">**WM/writer**</span><span class="sxs-lookup"><span data-stu-id="93aeb-148">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="93aeb-149">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="93aeb-149">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="93aeb-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="93aeb-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93aeb-151">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="93aeb-151">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




