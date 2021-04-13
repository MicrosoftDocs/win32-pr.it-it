---
title: Guida per programmatori WIC
description: Viene descritto come utilizzare le API WIC.
ms.assetid: ed7987f0-5983-4bb5-8640-0830a87c8f2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb6675ef7f5c065d2d3e00ab470cb334af25525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401738"
---
# <a name="wic-programming-guide"></a><span data-ttu-id="c6735-103">Guida per programmatori WIC</span><span class="sxs-lookup"><span data-stu-id="c6735-103">WIC programming guide</span></span>

<span data-ttu-id="c6735-104">In questa sezione sono inclusi argomenti concettuali che descrivono come utilizzare le API di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="c6735-104">This section contains conceptual topics that describe how to use the Windows Imaging Component (WIC) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c6735-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c6735-105">In this section</span></span>



| <span data-ttu-id="c6735-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="c6735-106">Topic</span></span>                                                                                 | <span data-ttu-id="c6735-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6735-107">Description</span></span>                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6735-108">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="c6735-108">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)<br/> | <span data-ttu-id="c6735-109">WIC fornisce un framework estensibile per l'utilizzo di immagini e metadati di immagini.</span><span class="sxs-lookup"><span data-stu-id="c6735-109">The WIC provides an extensible framework for working with images and image metadata.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="c6735-110">Panoramica dell'API WIC</span><span class="sxs-lookup"><span data-stu-id="c6735-110">WIC API Overview</span></span>](-wic-api.md)<br/>                                           | <span data-ttu-id="c6735-111">WIC fornisce un'API basata su Component Object Model (COM) per l'utilizzo in C e C++.</span><span class="sxs-lookup"><span data-stu-id="c6735-111">The WIC provides a Component Object Model (COM) based API for use in C and C++.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="c6735-112">Decodifica di immagini digitali</span><span class="sxs-lookup"><span data-stu-id="c6735-112">Decoding Digital Images</span></span>](-wic-decoder-portal.md)<br/>                         | <span data-ttu-id="c6735-113">Questa sezione contiene argomenti concettuali e procedure che descrivono i decodificatori di bitmap WIC usati nella decodifica delle immagini digitali.</span><span class="sxs-lookup"><span data-stu-id="c6735-113">This section contains conceptual and how-to topics that describe WIC bitmap decoders which are used in decoding digital images.</span></span><br/>                                                                            |
| [<span data-ttu-id="c6735-114">Utilizzo di dati immagine</span><span class="sxs-lookup"><span data-stu-id="c6735-114">Using Image Data</span></span>](-wic-bitmapsources-portal.md)<br/>                          | <span data-ttu-id="c6735-115">Questa sezione contiene argomenti concettuali e procedure che descrivono le origini bitmap di WIC e come modificarle.</span><span class="sxs-lookup"><span data-stu-id="c6735-115">This section contains conceptual and how-to topics that describe WIC bitmap sources and how to manipulate them.</span></span><br/>                                                                                            |
| [<span data-ttu-id="c6735-116">Codifica dei dati dell'immagine</span><span class="sxs-lookup"><span data-stu-id="c6735-116">Encoding Image Data</span></span>](encoding-bitmaps-to-digital-images.md)<br/>              | <span data-ttu-id="c6735-117">Questa sezione contiene argomenti concettuali e procedure che descrivono codificatori bitmap WIC che vengono usati per codificare le immagini digitali.</span><span class="sxs-lookup"><span data-stu-id="c6735-117">This section contains conceptual and how-to topics that describe WIC bitmap encoders which are used to encode digital images.</span></span><br/>                                                                              |
| [<span data-ttu-id="c6735-118">Codec WIC nativi</span><span class="sxs-lookup"><span data-stu-id="c6735-118">Native WIC Codecs</span></span>](native-wic-codecs.md)<br/>                                 | <span data-ttu-id="c6735-119">In questa sezione sono contenute informazioni sui codec di imaging nativi disponibili in WIC.</span><span class="sxs-lookup"><span data-stu-id="c6735-119">This section contains information about the native imaging codecs available in WIC.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="c6735-120">Elaborazione dei metadati delle immagini</span><span class="sxs-lookup"><span data-stu-id="c6735-120">Processing Image Metadata</span></span>](-wic-metadata-portal.md)<br/>                      | <span data-ttu-id="c6735-121">Questa sezione contiene argomenti concettuali che descrivono il sistema di metadati WIC.</span><span class="sxs-lookup"><span data-stu-id="c6735-121">This section contains conceptual topics that describe the WIC metadata system.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="c6735-122">Supporto di YCbCr JPEG</span><span class="sxs-lookup"><span data-stu-id="c6735-122">JPEG YCbCr Support</span></span>](jpeg-ycbcr-support.md)<br/>                               | <span data-ttu-id="c6735-123">A partire da Windows 8.1, il codec JPEG di [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) supporta la lettura e la scrittura di dati immagine nel formato nativo YC<sub>b</sub>C<sub>r</sub> .</span><span class="sxs-lookup"><span data-stu-id="c6735-123">Starting with Windows 8.1, the [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG codec supports reading and writing image data in its native YC<sub>b</sub>C<sub>r</sub> form.</span></span> <br/> |
| [<span data-ttu-id="c6735-124">Gestione dei colori</span><span class="sxs-lookup"><span data-stu-id="c6735-124">Color Management</span></span>](-wic-colormanagement.md)<br/>                               | <span data-ttu-id="c6735-125">WIC semplifica la gestione dei colori fornendo l'interfaccia [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) e l'interfaccia [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) .</span><span class="sxs-lookup"><span data-stu-id="c6735-125">WIC simplifies color management by providing the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) interface and the [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) interface.</span></span><br/>          |
| [<span data-ttu-id="c6735-126">Sviluppo di componenti</span><span class="sxs-lookup"><span data-stu-id="c6735-126">Component Development</span></span>](-wic-component-development.md)<br/>                    | <span data-ttu-id="c6735-127">WIC è una piattaforma estendibile che fornisce un'API di basso livello per le immagini digitali.</span><span class="sxs-lookup"><span data-stu-id="c6735-127">The WIC is an extensible platform that provides low-level API for digital images.</span></span><br/>                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="c6735-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c6735-128">See Also</span></span>

[<span data-ttu-id="c6735-129">Informazioni di riferimento su WIC</span><span class="sxs-lookup"><span data-stu-id="c6735-129">WIC Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="c6735-130">Esempi WIC</span><span class="sxs-lookup"><span data-stu-id="c6735-130">WIC Samples</span></span>](-wic-samples.md)


 

 




