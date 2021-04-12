---
description: Il set di argomenti seguente fornisce indicazioni su come implementare i formati di immagine RAW della fotocamera che funzioneranno all'interno del Framework di Windows Imaging Component (WIC).
ms.assetid: 145459fe-8ef4-41ba-b062-00f435c982e5
title: Linee guida per WIC per i formati di immagine RAW della fotocamera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09405f0f57aaa075678127d5d08bafcd28ecc6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232313"
---
# <a name="wic-guidelines-for-camera-raw-image-formats"></a><span data-ttu-id="8513c-103">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="8513c-103">WIC Guidelines for Camera RAW Image Formats</span></span>

<span data-ttu-id="8513c-104">Il set di argomenti seguente fornisce indicazioni su come implementare i formati di immagine RAW della fotocamera che funzioneranno all'interno del Framework di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="8513c-104">The following set of topics provide guidance on how to implement camera RAW image formats that will function within the Windows Imaging Component (WIC) framework.</span></span>

<dl>

[<span data-ttu-id="8513c-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="8513c-105">Introduction</span></span>](-wic-rawguidelines-intro.md)  
<dl>

[<span data-ttu-id="8513c-106">Formati di immagini non ELABORAte in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8513c-106">RAW Image Formats in Windows Vista</span></span>](-wic-rawguidelines-intro-vista.md)  
[<span data-ttu-id="8513c-107">Linee guida generali per l'implementazione di codec non ELABORAti</span><span class="sxs-lookup"><span data-stu-id="8513c-107">General Guidelines for Implementing RAW Codecs</span></span>](-wic-rawguidelines-intro-implement.md)  
<span data-ttu-id="8513c-108"></dl> </dd> <a href="-wic-rawguidelines-feature-complete.md">Completezza delle funzionalità:</a> [requisiti del metodo di interfaccia](-wic-rawguidelines-iface-reqs.md) delle interfacce consigliate</span><span class="sxs-lookup"><span data-stu-id="8513c-108"></dl> </dd> <a href="-wic-rawguidelines-feature-complete.md">Feature Completeness: Recommended Interfaces</a> [Interface Method Requirements](-wic-rawguidelines-iface-reqs.md)</span></span>  
<span data-ttu-id="8513c-109">[Supporto dei metadati](-wic-rawguidelines-metadata.md)  
</span><span class="sxs-lookup"><span data-stu-id="8513c-109">[Metadata Support](-wic-rawguidelines-metadata.md)  
</span></span><dl>

[<span data-ttu-id="8513c-110">Decodifica</span><span class="sxs-lookup"><span data-stu-id="8513c-110">Decoding</span></span>](-wic-rawguidelines-metadata-decoding.md)  
[<span data-ttu-id="8513c-111">Encoding</span><span class="sxs-lookup"><span data-stu-id="8513c-111">Encoding</span></span>](-wic-rawguidelines-metadata-encoding.md)  
<span data-ttu-id="8513c-112"></dl> </dd> <a href="/windows/desktop/wic/-wic-rawguidelines-iwicdevelopraw">Supporto per</a> [le linee guida di implementazione di IWICDevelopRaw per la serializzazione delle impostazioni di IWICDevelopRaw](-wic-rawguidelines-iwicdevelopraw-serializing.md)</span><span class="sxs-lookup"><span data-stu-id="8513c-112"></dl> </dd> <a href="/windows/desktop/wic/-wic-rawguidelines-iwicdevelopraw">Support for IWICDevelopRaw</a> [Implementing Guidelines for Serializing IWICDevelopRaw Settings](-wic-rawguidelines-iwicdevelopraw-serializing.md)</span></span>  
[<span data-ttu-id="8513c-113">Prestazioni</span><span class="sxs-lookup"><span data-stu-id="8513c-113">Performance</span></span>](-wic-rawguidelines-performance.md)  
[<span data-ttu-id="8513c-114">Formati pixel con intervallo dinamico elevato</span><span class="sxs-lookup"><span data-stu-id="8513c-114">High Dynamic Range Pixel Formats</span></span>](-wic-rawguidelines-hdr-formats.md)  
[<span data-ttu-id="8513c-115">Anteprime e anteprime</span><span class="sxs-lookup"><span data-stu-id="8513c-115">Thumbnails and Previews</span></span>](-wic-rawguidelines-thumbnail-previews.md)  
[<span data-ttu-id="8513c-116">Affidabilità e sicurezza</span><span class="sxs-lookup"><span data-stu-id="8513c-116">Reliability and Security</span></span>](-wic-rawguidelines-reliability-security.md)  
<span data-ttu-id="8513c-117">[Disponibilità di codec e supporto della piattaforma](-wic-rawguidelines-availability.md)  
</span><span class="sxs-lookup"><span data-stu-id="8513c-117">[Codec Availability and Platform Support](-wic-rawguidelines-availability.md)  
</span></span><dl>

[<span data-ttu-id="8513c-118">Individuazione codec</span><span class="sxs-lookup"><span data-stu-id="8513c-118">Codec Discovery</span></span>](-wic-rawguidelines-availability.md)  
[<span data-ttu-id="8513c-119">Supporto della piattaforma Windows XP</span><span class="sxs-lookup"><span data-stu-id="8513c-119">Windows XP Platform Support</span></span>](-wic-rawguidelines-availability.md)  
<span data-ttu-id="8513c-120"></dl> </dd> <a href="-wic-rawguidelines-win7.md">Requisiti dei codec RAW per Windows 7</a> [per ulteriori informazioni](-wic-rawguidelines-moreinfo.md)  
</span><span class="sxs-lookup"><span data-stu-id="8513c-120"></dl> </dd> <a href="-wic-rawguidelines-win7.md">RAW Codec Requirements for Windows 7</a> [For More Information](-wic-rawguidelines-moreinfo.md)  
</span></span></dl>

## <a name="related-topics"></a><span data-ttu-id="8513c-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8513c-121">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8513c-122">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8513c-122">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8513c-123">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="8513c-123">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="8513c-124">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="8513c-124">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="8513c-125">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="8513c-125">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
