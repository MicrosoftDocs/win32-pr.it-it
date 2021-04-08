---
title: Attributo AltHRef (ImageData) (la)
description: Attributo AltHRef (ImageData) (la)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046930"
---
# <a name="althref-attribute-imagedatavml"></a><span data-ttu-id="804d7-103">Attributo AltHRef (ImageData) (la)</span><span class="sxs-lookup"><span data-stu-id="804d7-103">AltHRef Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="804d7-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="804d7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="804d7-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="804d7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="804d7-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="804d7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="804d7-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="804d7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="804d7-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="804d7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="804d7-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="804d7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="804d7-110">Specifica un riferimento alternativo per un'immagine.</span><span class="sxs-lookup"><span data-stu-id="804d7-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="804d7-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="804d7-111">Read/write.</span></span> <span data-ttu-id="804d7-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="804d7-112">**String**.</span></span>

<span data-ttu-id="804d7-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="804d7-113">**Applies To**</span></span>

[<span data-ttu-id="804d7-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="804d7-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="804d7-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="804d7-115">**Tag Syntax**</span></span>

<span data-ttu-id="804d7-116"><v: *element* o:althref = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="804d7-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="804d7-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="804d7-117">**Script Syntax**</span></span>

<span data-ttu-id="804d7-118">*element* . althref = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="804d7-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="804d7-119">*espressione* = *elemento*. althref</span><span class="sxs-lookup"><span data-stu-id="804d7-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="804d7-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="804d7-120">**Remarks**</span></span>

<span data-ttu-id="804d7-121">Supporta la conservazione dei dati PICT tramite Roundtripping HTML.</span><span class="sxs-lookup"><span data-stu-id="804d7-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="804d7-122">Nella scrittura HTML la rappresentazione alternativa, ovvero i dati PICT originali se il file proviene da Macintosh, viene salvata.</span><span class="sxs-lookup"><span data-stu-id="804d7-122">On HTML write, the alternate representation (that is, the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="804d7-123">In una lettura HTML, **AltHRef** è favorito tramite **src**.</span><span class="sxs-lookup"><span data-stu-id="804d7-123">On an HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="804d7-124">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="804d7-124">*Microsoft Office Extensions Attribute*</span></span>

 

 