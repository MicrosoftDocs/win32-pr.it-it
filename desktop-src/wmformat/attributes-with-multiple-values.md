---
title: Attributi con più valori (Windows Media Format 11 SDK)
description: Informazioni sugli attributi con più valori in Windows Media Format 11 SDK. Alcuni attributi degli elementi multimediali possono avere più valori.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK,attributi
- Advanced Systems Format (ASF), attributi
- ASF (Advanced Systems Format),attributi
- attributi, più valori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262693"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="d6b5a-108">Attributi con più valori (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="d6b5a-108">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="d6b5a-109">Ad alcuni attributi predefiniti possono essere assegnati più valori.</span><span class="sxs-lookup"><span data-stu-id="d6b5a-109">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="d6b5a-110">Ad esempio, **Artista** è un attributo che può avere più valori.</span><span class="sxs-lookup"><span data-stu-id="d6b5a-110">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="d6b5a-111">È possibile chiamare [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) più volte per aggiungere tutti i valori **di Artista** necessari.</span><span class="sxs-lookup"><span data-stu-id="d6b5a-111">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="d6b5a-112">Se si effettuano più chiamate ad **AddAttribute** per attributi che non supportano più valori, il metodo può restituire un codice di errore o semplicemente ignorare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d6b5a-112">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="d6b5a-113">Nella tabella seguente sono elencati gli attributi che supportano più valori.</span><span class="sxs-lookup"><span data-stu-id="d6b5a-113">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="d6b5a-114">Alcuni attributi possono avere più valori solo nei file ASF, mentre altri possono avere più valori nei file ASF e MP3.</span><span class="sxs-lookup"><span data-stu-id="d6b5a-114">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="d6b5a-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="d6b5a-115">Attribute</span></span>                                                 | <span data-ttu-id="d6b5a-116">Supporto per più valori</span><span class="sxs-lookup"><span data-stu-id="d6b5a-116">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="d6b5a-117">**Autore**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-117">**Author**</span></span>](author.md)                                  | <span data-ttu-id="d6b5a-118">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="d6b5a-118">ASF, MP3</span></span>                    |
| [<span data-ttu-id="d6b5a-119">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="d6b5a-120">ASF</span><span class="sxs-lookup"><span data-stu-id="d6b5a-120">ASF</span></span>                         |
| [<span data-ttu-id="d6b5a-121">**WM/AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-121">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="d6b5a-122">ASF</span><span class="sxs-lookup"><span data-stu-id="d6b5a-122">ASF</span></span>                         |
| [<span data-ttu-id="d6b5a-123">**WM/Category**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-123">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="d6b5a-124">ASF</span><span class="sxs-lookup"><span data-stu-id="d6b5a-124">ASF</span></span>                         |
| [<span data-ttu-id="d6b5a-125">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-125">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="d6b5a-126">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="d6b5a-126">ASF, MP3</span></span>                    |
| [<span data-ttu-id="d6b5a-127">**WM/Sistema di controllo**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-127">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="d6b5a-128">ASF</span><span class="sxs-lookup"><span data-stu-id="d6b5a-128">ASF</span></span>                         |
| [<span data-ttu-id="d6b5a-129">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-129">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="d6b5a-130">ASF</span><span class="sxs-lookup"><span data-stu-id="d6b5a-130">ASF</span></span>                         |
| [<span data-ttu-id="d6b5a-131">**WM/Genre**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-131">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="d6b5a-132">ASF</span><span class="sxs-lookup"><span data-stu-id="d6b5a-132">ASF</span></span>                         |
| [<span data-ttu-id="d6b5a-133">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-133">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="d6b5a-134">ASF</span><span class="sxs-lookup"><span data-stu-id="d6b5a-134">ASF</span></span>                         |
| [<span data-ttu-id="d6b5a-135">**WM/Language**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-135">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="d6b5a-136">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="d6b5a-136">ASF, MP3</span></span>                    |
| [<span data-ttu-id="d6b5a-137">**WM/Lyrics \_ Synchronised**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-137">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="d6b5a-138">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="d6b5a-138">ASF, MP3</span></span>                    |
| [<span data-ttu-id="d6b5a-139">**WM/Wm/Wm**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-139">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="d6b5a-140">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="d6b5a-140">ASF, MP3</span></span>                    |
| [<span data-ttu-id="d6b5a-141">**WM/Picture**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-141">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="d6b5a-142">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="d6b5a-142">ASF, MP3</span></span>                    |
| [<span data-ttu-id="d6b5a-143">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-143">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="d6b5a-144">ASF</span><span class="sxs-lookup"><span data-stu-id="d6b5a-144">ASF</span></span>                         |
| [<span data-ttu-id="d6b5a-145">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-145">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="d6b5a-146">ASF</span><span class="sxs-lookup"><span data-stu-id="d6b5a-146">ASF</span></span>                         |
| [<span data-ttu-id="d6b5a-147">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-147">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="d6b5a-148">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="d6b5a-148">ASF, MP3</span></span>                    |
| [<span data-ttu-id="d6b5a-149">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-149">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="d6b5a-150">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="d6b5a-150">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="d6b5a-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d6b5a-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6b5a-152">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="d6b5a-152">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




