---
description: Introduzione (linee guida per WIC per i formati di immagini RAW della fotocamera)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introduzione (linee guida per WIC per i formati di immagini RAW della fotocamera)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232876"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a><span data-ttu-id="7eaa7-103">Introduzione (linee guida per WIC per i formati di immagini RAW della fotocamera)</span><span class="sxs-lookup"><span data-stu-id="7eaa7-103">Introduction (WIC Guidelines for Camera RAW Image Formats)</span></span>

<span data-ttu-id="7eaa7-104">Windows Imaging Component (WIC) fornisce un framework estensibile per l'utilizzo di immagini e metadati di immagini.</span><span class="sxs-lookup"><span data-stu-id="7eaa7-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="7eaa7-105">WIC consente ai fornitori di software e hardware di sviluppare codec in modo che i propri formati di immagine possano ottenere lo stesso supporto della piattaforma dei formati di immagine nativi, ad esempio il formato TIFF (Tagged Image File Format), il Joint Photographic Experts Group (JPEG) o la foto HD.</span><span class="sxs-lookup"><span data-stu-id="7eaa7-105">WIC makes it possible for software and hardware vendors to develop codecs so that their own image formats can obtain the same platform support as native image formats such as tagged image file format (TIFF), Joint Photographic Experts Group (JPEG), or HD Photo.</span></span>

<span data-ttu-id="7eaa7-106">WIC fornisce un unico set coerente di interfacce per tutte le operazioni di elaborazione delle immagini, indipendentemente dal formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="7eaa7-106">WIC provides a single, consistent set of interfaces for all image processing, regardless of image format.</span></span> <span data-ttu-id="7eaa7-107">Pertanto, qualsiasi applicazione che utilizza WIC riceve il supporto automatico per i nuovi formati di immagine non appena viene installato il codec.</span><span class="sxs-lookup"><span data-stu-id="7eaa7-107">Therefore, any application that uses WIC receives automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="7eaa7-108">WIC fornisce anche un Framework di metadati estendibile che consente alle applicazioni di leggere e scrivere i propri metadati proprietari direttamente nei file di immagine, in modo che i metadati non vengano mai persi o separati dall'immagine.</span><span class="sxs-lookup"><span data-stu-id="7eaa7-108">WIC also provides an extensible metadata framework that makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata is never lost or separated from the image.</span></span>

<span data-ttu-id="7eaa7-109">WIC è incluso in Windows Presentation Foundation (WPF) ed è integrato in Windows Vista e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="7eaa7-109">WIC is included with Windows Presentation Foundation (WPF) and is built into Windows Vista and later Windows versions.</span></span> <span data-ttu-id="7eaa7-110">È inoltre disponibile come componente ridistribuibile autonomo per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7eaa7-110">It is also available as a stand-alone redistributable component for Windows XP.</span></span>

<span data-ttu-id="7eaa7-111">Queste linee guida sono progettate per aiutare i produttori di formati RAW a sviluppare codec WIC.</span><span class="sxs-lookup"><span data-stu-id="7eaa7-111">These guidelines are designed to help RAW format manufacturers in their development of WIC codecs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eaa7-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7eaa7-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7eaa7-113">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7eaa7-113">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7eaa7-114">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="7eaa7-114">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="7eaa7-115">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="7eaa7-115">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="7eaa7-116">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="7eaa7-116">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



