---
description: In questo argomento vengono fornite informazioni sul codec ICO nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Panoramica sul formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317866"
---
# <a name="ico-format-overview"></a><span data-ttu-id="c96af-103">Panoramica sul formato ICO</span><span class="sxs-lookup"><span data-stu-id="c96af-103">ICO Format Overview</span></span>

<span data-ttu-id="c96af-104">In questo argomento vengono fornite informazioni sul codec ICO nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="c96af-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="c96af-105">Identità codec</span><span class="sxs-lookup"><span data-stu-id="c96af-105">Codec Identity</span></span>

<span data-ttu-id="c96af-106">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="c96af-106">The following table provides codec identification information.</span></span>



|                        |                   |
|------------------------|-------------------|
| <span data-ttu-id="c96af-107">Nome/i formale/i</span><span class="sxs-lookup"><span data-stu-id="c96af-107">Formal Name(s)</span></span>         | <span data-ttu-id="c96af-108">Formato dell'icona (ICO)</span><span class="sxs-lookup"><span data-stu-id="c96af-108">Icon Format (ICO)</span></span> |
| <span data-ttu-id="c96af-109">Estensioni del nome di file</span><span class="sxs-lookup"><span data-stu-id="c96af-109">File Name Extension(s)</span></span> | <span data-ttu-id="c96af-110">ico</span><span class="sxs-lookup"><span data-stu-id="c96af-110">ico</span></span>               |
| <span data-ttu-id="c96af-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="c96af-111">MIME type</span></span>              | <span data-ttu-id="c96af-112">immagine/ICO</span><span class="sxs-lookup"><span data-stu-id="c96af-112">image/ico</span></span>         |
| <span data-ttu-id="c96af-113">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="c96af-113">Specification Support</span></span>  |                   |



 

<span data-ttu-id="c96af-114">La tabella seguente elenca i GUID usati per identificare i componenti del codec ICO nativi.</span><span class="sxs-lookup"><span data-stu-id="c96af-114">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="c96af-115">Componente</span><span class="sxs-lookup"><span data-stu-id="c96af-115">Component</span></span>        | <span data-ttu-id="c96af-116">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="c96af-116">Friendly Name</span></span>            | <span data-ttu-id="c96af-117">GUID</span><span class="sxs-lookup"><span data-stu-id="c96af-117">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="c96af-118">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="c96af-118">Container Format</span></span> | <span data-ttu-id="c96af-119">GUID \_ ContainerFormatIco</span><span class="sxs-lookup"><span data-stu-id="c96af-119">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="c96af-120">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="c96af-120">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="c96af-121">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="c96af-121">Decoder</span></span>          | <span data-ttu-id="c96af-122">\_WICICODECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="c96af-122">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="c96af-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="c96af-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="c96af-124">Codificatore</span><span class="sxs-lookup"><span data-stu-id="c96af-124">Encoder</span></span>          | <span data-ttu-id="c96af-125">NON DISPONIBILE</span><span class="sxs-lookup"><span data-stu-id="c96af-125">NOT AVAILABLE</span></span>            | <span data-ttu-id="c96af-126">NON DISPONIBILE</span><span class="sxs-lookup"><span data-stu-id="c96af-126">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="c96af-127">Codifica</span><span class="sxs-lookup"><span data-stu-id="c96af-127">Encoding</span></span>

<span data-ttu-id="c96af-128">WIC non fornisce un codificatore di immagini ICO nativo.</span><span class="sxs-lookup"><span data-stu-id="c96af-128">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="c96af-129">Decodifica</span><span class="sxs-lookup"><span data-stu-id="c96af-129">Decoding</span></span>

<span data-ttu-id="c96af-130">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="c96af-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="c96af-131">Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="c96af-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="c96af-132">Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="c96af-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



