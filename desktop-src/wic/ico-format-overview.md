---
description: Questo argomento fornisce informazioni sul codec ICO nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Panoramica del formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329a53a3b5d386c5e5386141162c608dc9db1ec0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444471"
---
# <a name="ico-format-overview"></a><span data-ttu-id="3daf4-103">Panoramica del formato ICO</span><span class="sxs-lookup"><span data-stu-id="3daf4-103">ICO Format Overview</span></span>

<span data-ttu-id="3daf4-104">Questo argomento fornisce informazioni sul codec ICO nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="3daf4-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="3daf4-105">Codec Identity</span><span class="sxs-lookup"><span data-stu-id="3daf4-105">Codec Identity</span></span>

<span data-ttu-id="3daf4-106">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="3daf4-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="3daf4-107">Componente</span><span class="sxs-lookup"><span data-stu-id="3daf4-107">Component</span></span>            | <span data-ttu-id="3daf4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3daf4-108">Description</span></span>       |
|------------------------|-------------------|
| <span data-ttu-id="3daf4-109">Nomi formali</span><span class="sxs-lookup"><span data-stu-id="3daf4-109">Formal Name(s)</span></span>         | <span data-ttu-id="3daf4-110">Formato icona (ICO)</span><span class="sxs-lookup"><span data-stu-id="3daf4-110">Icon Format (ICO)</span></span> |
| <span data-ttu-id="3daf4-111">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="3daf4-111">File Name Extension(s)</span></span> | <span data-ttu-id="3daf4-112">Ico</span><span class="sxs-lookup"><span data-stu-id="3daf4-112">ico</span></span>               |
| <span data-ttu-id="3daf4-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="3daf4-113">MIME type</span></span>              | <span data-ttu-id="3daf4-114">image/ico</span><span class="sxs-lookup"><span data-stu-id="3daf4-114">image/ico</span></span>         |
| <span data-ttu-id="3daf4-115">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="3daf4-115">Specification Support</span></span>  |                   |



 

<span data-ttu-id="3daf4-116">Nella tabella seguente sono elencati i GUID usati per identificare i componenti nativi del codec ICO.</span><span class="sxs-lookup"><span data-stu-id="3daf4-116">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="3daf4-117">Componente</span><span class="sxs-lookup"><span data-stu-id="3daf4-117">Component</span></span>        | <span data-ttu-id="3daf4-118">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="3daf4-118">Friendly Name</span></span>            | <span data-ttu-id="3daf4-119">GUID</span><span class="sxs-lookup"><span data-stu-id="3daf4-119">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="3daf4-120">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="3daf4-120">Container Format</span></span> | <span data-ttu-id="3daf4-121">GUID \_ ContainerFormatIco</span><span class="sxs-lookup"><span data-stu-id="3daf4-121">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="3daf4-122">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="3daf4-122">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="3daf4-123">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="3daf4-123">Decoder</span></span>          | <span data-ttu-id="3daf4-124">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="3daf4-124">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="3daf4-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="3daf4-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="3daf4-126">Codificatore</span><span class="sxs-lookup"><span data-stu-id="3daf4-126">Encoder</span></span>          | <span data-ttu-id="3daf4-127">NON DISPONIBILE</span><span class="sxs-lookup"><span data-stu-id="3daf4-127">NOT AVAILABLE</span></span>            | <span data-ttu-id="3daf4-128">NON DISPONIBILE</span><span class="sxs-lookup"><span data-stu-id="3daf4-128">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="3daf4-129">Codifica</span><span class="sxs-lookup"><span data-stu-id="3daf4-129">Encoding</span></span>

<span data-ttu-id="3daf4-130">WIC non fornisce un codificatore di immagini ICO nativo.</span><span class="sxs-lookup"><span data-stu-id="3daf4-130">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="3daf4-131">Decodifica</span><span class="sxs-lookup"><span data-stu-id="3daf4-131">Decoding</span></span>

<span data-ttu-id="3daf4-132">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="3daf4-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="3daf4-133">Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="3daf4-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="3daf4-134">Per altre informazioni sull'uso di dati di immagine decodificati, vedere Cenni [preliminari sulle origini bitmap.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="3daf4-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



