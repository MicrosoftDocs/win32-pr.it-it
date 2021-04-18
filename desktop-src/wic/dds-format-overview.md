---
description: Fornisce informazioni sul codec DDS nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Cenni preliminari sul formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c45222a66d5a250caaf46db465d2359e09b3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312942"
---
# <a name="dds-format-overview"></a><span data-ttu-id="a2c71-103">Cenni preliminari sul formato DDS</span><span class="sxs-lookup"><span data-stu-id="a2c71-103">DDS Format Overview</span></span>

<span data-ttu-id="a2c71-104">In questo argomento vengono fornite informazioni sul codec DDS nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="a2c71-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="a2c71-105">Identità codec</span><span class="sxs-lookup"><span data-stu-id="a2c71-105">Codec Identity</span></span>

<span data-ttu-id="a2c71-106">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="a2c71-106">The following table provides codec identification information.</span></span>



|                        |                    |
|------------------------|--------------------|
| <span data-ttu-id="a2c71-107">Nome/i formale/i</span><span class="sxs-lookup"><span data-stu-id="a2c71-107">Formal Name(s)</span></span>         | <span data-ttu-id="a2c71-108">Superficie DirectDraw</span><span class="sxs-lookup"><span data-stu-id="a2c71-108">DirectDraw Surface</span></span> |
| <span data-ttu-id="a2c71-109">Estensioni del nome di file</span><span class="sxs-lookup"><span data-stu-id="a2c71-109">File Name Extension(s)</span></span> | <span data-ttu-id="a2c71-110">DDS</span><span class="sxs-lookup"><span data-stu-id="a2c71-110">dds</span></span>                |
| <span data-ttu-id="a2c71-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="a2c71-111">MIME type</span></span>              | <span data-ttu-id="a2c71-112">Image/VND-ms. DDS</span><span class="sxs-lookup"><span data-stu-id="a2c71-112">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="a2c71-113">La tabella seguente elenca i GUID usati per identificare i componenti dei codec DDS nativi.</span><span class="sxs-lookup"><span data-stu-id="a2c71-113">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="a2c71-114">Componente</span><span class="sxs-lookup"><span data-stu-id="a2c71-114">Component</span></span>        | <span data-ttu-id="a2c71-115">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="a2c71-115">Friendly Name</span></span>            | <span data-ttu-id="a2c71-116">GUID</span><span class="sxs-lookup"><span data-stu-id="a2c71-116">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="a2c71-117">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="a2c71-117">Container Format</span></span> | <span data-ttu-id="a2c71-118">GUID \_ ContainerFormatDds</span><span class="sxs-lookup"><span data-stu-id="a2c71-118">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="a2c71-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="a2c71-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="a2c71-120">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="a2c71-120">Decoder</span></span>          | <span data-ttu-id="a2c71-121">\_WICDDSDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="a2c71-121">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="a2c71-122">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="a2c71-122">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="a2c71-123">Codificatore</span><span class="sxs-lookup"><span data-stu-id="a2c71-123">Encoder</span></span>          | <span data-ttu-id="a2c71-124">\_WICDDSENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="a2c71-124">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="a2c71-125">a61dde94-66CE-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="a2c71-125">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="a2c71-126">Supporto del formato pixel</span><span class="sxs-lookup"><span data-stu-id="a2c71-126">Pixel Format Support</span></span>

<span data-ttu-id="a2c71-127">Si noti che il formato DDS supporta qualsiasi valore di [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valido.</span><span class="sxs-lookup"><span data-stu-id="a2c71-127">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="a2c71-128">Tuttavia, il codec di WIC DDS supporta solo la decodifica e la codifica di file contenenti i formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2c71-128">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="a2c71-129">\_Formato DXGI \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="a2c71-129">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="a2c71-130">\_Formato DXGI \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="a2c71-130">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="a2c71-131">\_Formato DXGI \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="a2c71-131">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="a2c71-132">Codifica</span><span class="sxs-lookup"><span data-stu-id="a2c71-132">Encoding</span></span>

<span data-ttu-id="a2c71-133">Le API di codifica WIC sono progettate per essere indipendenti dal codec e pertanto la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="a2c71-133">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="a2c71-134">Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="a2c71-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="a2c71-135">Il formato di file DDS presenta requisiti univoci che derivano dal supporto per concetti quali mipmap e matrici di trame.</span><span class="sxs-lookup"><span data-stu-id="a2c71-135">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="a2c71-136">Per esercitare il controllo completo sulla codifica delle immagini DDS, è necessario usare l'interfaccia [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) per impostare i parametri di codifica specifici di DDS.</span><span class="sxs-lookup"><span data-stu-id="a2c71-136">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="a2c71-137">Decodifica</span><span class="sxs-lookup"><span data-stu-id="a2c71-137">Decoding</span></span>

<span data-ttu-id="a2c71-138">Le API di decodifica WIC sono progettate per essere indipendenti dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="a2c71-138">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="a2c71-139">Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="a2c71-139">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="a2c71-140">Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="a2c71-140">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="a2c71-141">Blocca l'accesso ai dati compressi</span><span class="sxs-lookup"><span data-stu-id="a2c71-141">Block compressed data access</span></span>

<span data-ttu-id="a2c71-142">Oltre a supportare le interfacce standard del codec WIC, il decodificatore DDS fornisce l'accesso diretto ai dati compressi in blocchi nativi usando le interfacce specifiche di DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) e [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span><span class="sxs-lookup"><span data-stu-id="a2c71-142">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="a2c71-143">Per usare queste interfacce, chiamare rispettivamente QueryInterface di [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span><span class="sxs-lookup"><span data-stu-id="a2c71-143">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
