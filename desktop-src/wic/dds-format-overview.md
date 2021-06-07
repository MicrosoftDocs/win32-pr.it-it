---
description: Fornisce informazioni sul codec DDS nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Panoramica del formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f860a5759218575acb53be5f2142e71aa34e9554
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444952"
---
# <a name="dds-format-overview"></a><span data-ttu-id="569e1-103">Panoramica del formato DDS</span><span class="sxs-lookup"><span data-stu-id="569e1-103">DDS Format Overview</span></span>

<span data-ttu-id="569e1-104">In questo argomento vengono fornite informazioni sul codec DDS nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="569e1-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="569e1-105">Identità codec</span><span class="sxs-lookup"><span data-stu-id="569e1-105">Codec Identity</span></span>

<span data-ttu-id="569e1-106">Nella tabella seguente vengono fornite informazioni di identificazione dei codec.</span><span class="sxs-lookup"><span data-stu-id="569e1-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="569e1-107">Componente</span><span class="sxs-lookup"><span data-stu-id="569e1-107">Component</span></span>              | <span data-ttu-id="569e1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="569e1-108">Description</span></span>        |
|------------------------|--------------------|
| <span data-ttu-id="569e1-109">Nomi formali</span><span class="sxs-lookup"><span data-stu-id="569e1-109">Formal Name(s)</span></span>         | <span data-ttu-id="569e1-110">Superficie DirectDraw</span><span class="sxs-lookup"><span data-stu-id="569e1-110">DirectDraw Surface</span></span> |
| <span data-ttu-id="569e1-111">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="569e1-111">File Name Extension(s)</span></span> | <span data-ttu-id="569e1-112">Dds</span><span class="sxs-lookup"><span data-stu-id="569e1-112">dds</span></span>                |
| <span data-ttu-id="569e1-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="569e1-113">MIME type</span></span>              | <span data-ttu-id="569e1-114">image/vnd-ms.dds</span><span class="sxs-lookup"><span data-stu-id="569e1-114">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="569e1-115">Nella tabella seguente sono elencati i GUID usati per identificare i componenti nativi del codec DDS.</span><span class="sxs-lookup"><span data-stu-id="569e1-115">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="569e1-116">Componente</span><span class="sxs-lookup"><span data-stu-id="569e1-116">Component</span></span>        | <span data-ttu-id="569e1-117">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="569e1-117">Friendly Name</span></span>            | <span data-ttu-id="569e1-118">GUID</span><span class="sxs-lookup"><span data-stu-id="569e1-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="569e1-119">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="569e1-119">Container Format</span></span> | <span data-ttu-id="569e1-120">GUID \_ ContainerFormatDds</span><span class="sxs-lookup"><span data-stu-id="569e1-120">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="569e1-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="569e1-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="569e1-122">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="569e1-122">Decoder</span></span>          | <span data-ttu-id="569e1-123">CLSID \_ WICDdsDecoder</span><span class="sxs-lookup"><span data-stu-id="569e1-123">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="569e1-124">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="569e1-124">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="569e1-125">Codificatore</span><span class="sxs-lookup"><span data-stu-id="569e1-125">Encoder</span></span>          | <span data-ttu-id="569e1-126">CLSID \_ WICDdsEncoder</span><span class="sxs-lookup"><span data-stu-id="569e1-126">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="569e1-127">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="569e1-127">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="569e1-128">Supporto del formato pixel</span><span class="sxs-lookup"><span data-stu-id="569e1-128">Pixel Format Support</span></span>

<span data-ttu-id="569e1-129">Si noti che il formato DDS supporta qualsiasi valore [**DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valido.</span><span class="sxs-lookup"><span data-stu-id="569e1-129">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="569e1-130">Tuttavia, il codec WIC DDS supporta solo file di decodifica e codifica contenenti i formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="569e1-130">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="569e1-131">DXGI \_ FORMAT \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="569e1-131">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="569e1-132">DXGI \_ FORMAT \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="569e1-132">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="569e1-133">DXGI \_ FORMAT \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="569e1-133">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="569e1-134">Codifica</span><span class="sxs-lookup"><span data-stu-id="569e1-134">Encoding</span></span>

<span data-ttu-id="569e1-135">Le API di codifica WIC sono progettate per essere indipendenti dai codec e pertanto la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="569e1-135">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="569e1-136">Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="569e1-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="569e1-137">Il formato di file DDS presenta requisiti univoci che derivano dal supporto per concetti come mipmap e matrici di trame.</span><span class="sxs-lookup"><span data-stu-id="569e1-137">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="569e1-138">Per esercitare completamente il controllo sulla codifica delle immagini DDS, è necessario usare [**l'interfaccia IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) per impostare i parametri di codifica specifici di DDS.</span><span class="sxs-lookup"><span data-stu-id="569e1-138">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="569e1-139">Decodifica</span><span class="sxs-lookup"><span data-stu-id="569e1-139">Decoding</span></span>

<span data-ttu-id="569e1-140">Le API di decodifica WIC sono progettate per essere indipendenti dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="569e1-140">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="569e1-141">Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="569e1-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="569e1-142">Per altre informazioni sull'uso di dati immagine decodificati, vedere Panoramica [delle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="569e1-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="569e1-143">Bloccare l'accesso ai dati compressi</span><span class="sxs-lookup"><span data-stu-id="569e1-143">Block compressed data access</span></span>

<span data-ttu-id="569e1-144">Oltre a supportare le interfacce codec WIC standard, il decodificatore DDS fornisce l'accesso diretto ai dati compressi in blocchi nativi usando le interfacce specifiche di DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) e [**IWICDdsFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode)</span><span class="sxs-lookup"><span data-stu-id="569e1-144">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="569e1-145">Per usare queste interfacce, chiamare QueryInterface rispettivamente da [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="569e1-145">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
