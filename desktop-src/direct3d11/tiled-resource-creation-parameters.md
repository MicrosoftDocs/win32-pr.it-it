---
title: Parametri per la creazione di risorse affiancate
description: Esistono alcuni vincoli sul tipo di risorse Direct3D che è possibile creare con il flag di varie risorse di D3D11 \_ \_ \_ . In questa sezione vengono forniti i parametri validi per la creazione di risorse affiancate.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b912325371c59bd46a6cc4245289b2fe5d32a924
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/13/2019
ms.locfileid: "103719330"
---
# <a name="tiled-resource-creation-parameters"></a><span data-ttu-id="f54dd-104">Parametri per la creazione di risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="f54dd-104">Tiled resource creation parameters</span></span>

<span data-ttu-id="f54dd-105">Esistono alcuni vincoli sul tipo di risorse Direct3D che è possibile creare con il flag di [**\_ \_ varie \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) risorse di d3d11.</span><span class="sxs-lookup"><span data-stu-id="f54dd-105">There are some constraints on the type of Direct3D resources that you can create with the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> <span data-ttu-id="f54dd-106">In questa sezione vengono forniti i parametri validi per la creazione di risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="f54dd-106">This section provides the valid parameters for creating tiled resources.</span></span>

<dl> <dt>

<span data-ttu-id="f54dd-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Tipo di risorsa supportato**</span><span class="sxs-lookup"><span data-stu-id="f54dd-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Supported Resource Type**</span></span>
</dt> <dd>

<span data-ttu-id="f54dd-108">\[Matrice Texture2D \] (inclusa \[ la matrice TextureCube \] , che è una variante della \[ matrice Texture2D \] ) o un buffer.</span><span class="sxs-lookup"><span data-stu-id="f54dd-108">Texture2D\[Array\] (including TextureCube\[Array\], which is a variant of Texture2D\[Array\]) or Buffer.</span></span>

<span data-ttu-id="f54dd-109">**Non supportato:** Texture1D \[ array \] o Texture3D, ma Texture3D potrebbe essere supportato in futuro.</span><span class="sxs-lookup"><span data-stu-id="f54dd-109">**NOT supported:** Texture1D\[Array\] or Texture3D, but Texture3D might be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="f54dd-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Utilizzo risorse supportato**</span><span class="sxs-lookup"><span data-stu-id="f54dd-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="f54dd-111">\_ \_ Impostazione predefinita utilizzo d3d11.</span><span class="sxs-lookup"><span data-stu-id="f54dd-111">D3D11\_USAGE\_DEFAULT.</span></span>

<span data-ttu-id="f54dd-112">**Non supportato:** D3D11 \_ utilizzo \_ dinamico, \_ \_ gestione temporanea utilizzo D3D11 o utilizzo d3d11 non \_ \_ modificabile.</span><span class="sxs-lookup"><span data-stu-id="f54dd-112">**NOT supported:** D3D11\_USAGE\_DYNAMIC, D3D11\_USAGE\_STAGING, or D3D11\_USAGE\_IMMUTABLE.</span></span>

</dd> <dt>

<span data-ttu-id="f54dd-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Flag varie delle risorse supportate**</span><span class="sxs-lookup"><span data-stu-id="f54dd-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="f54dd-114">\_Risorse d3d11 \_ varie \_ affiancate (per definizione), \_ varie \_ TEXTURECUBE, argomenti di \_ DRAWINDIRECT \_ , \_ buffer \_ consentono viste non \_ elaborate \_ , struttura del \_ buffer \_ , clamp di \_ risorse \_ o \_ genera \_ MIPS.</span><span class="sxs-lookup"><span data-stu-id="f54dd-114">D3D11\_RESOURCE\_MISC\_TILED (by definition), \_MISC\_TEXTURECUBE, \_DRAWINDIRECT\_ARGS, \_BUFFER\_ALLOW\_RAW\_VIEWS, \_BUFFER\_STRUCTURED, \_RESOURCE\_CLAMP, or \_GENERATE\_MIPS.</span></span>

<span data-ttu-id="f54dd-115">**Non supportato:** \_ SHARED, \_ Shared \_ KEYEDMUTEX, \_ GDI \_ compatible, \_ Shared \_ NTHANDLE, \_ Restricted \_ Content, \_ Restrict \_ Shared \_ Resource, \_ Restrict \_ Shared \_ Resource \_ driver, \_ guarded o \_ tile \_ pool.</span><span class="sxs-lookup"><span data-stu-id="f54dd-115">**NOT supported:** \_SHARED, \_SHARED\_KEYEDMUTEX, \_GDI\_COMPATIBLE, \_SHARED\_NTHANDLE, \_RESTRICTED\_CONTENT, \_RESTRICT\_SHARED\_RESOURCE, \_RESTRICT\_SHARED\_RESOURCE\_DRIVER, \_GUARDED, or \_TILE\_POOL.</span></span>

</dd> <dt>

<span data-ttu-id="f54dd-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Flag di binding supportati**</span><span class="sxs-lookup"><span data-stu-id="f54dd-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Supported Bind Flags**</span></span>
</dt> <dd>

<span data-ttu-id="f54dd-117">D3D11 \_ associare la \_ \_ risorsa shader, la \_ \_ destinazione di rendering, il \_ Depth \_ stencil o \_ \_ l'accesso non ordinato.</span><span class="sxs-lookup"><span data-stu-id="f54dd-117">D3D11\_BIND\_SHADER\_RESOURCE, \_RENDER\_TARGET, \_DEPTH\_STENCIL, or \_UNORDERED\_ACCESS.</span></span>

<span data-ttu-id="f54dd-118">**Non supportato:** \_ \_Buffer costante, \_ buffer di Vertex \_ \[ Nota che l'associazione di un buffer affiancato come SRV/UAV/RTV è ancora OK \] , buffer di \_ indice \_ , output del \_ flusso \_ , \_ \_ decodificatore di binding o \_ \_ \_ codificatore video bind.</span><span class="sxs-lookup"><span data-stu-id="f54dd-118">**NOT supported:** \_CONSTANT\_BUFFER, \_VERTEX\_BUFFER \[note that binding a tiled Buffer as an SRV/UAV/RTV is still ok\], \_INDEX\_BUFFER, \_STREAM\_OUTPUT, \_BIND\_DECODER, or \_BIND\_VIDEO\_ENCODER.</span></span>

</dd> <dt>

<span data-ttu-id="f54dd-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Formati supportati**</span><span class="sxs-lookup"><span data-stu-id="f54dd-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Supported Formats**</span></span>
</dt> <dd>

<span data-ttu-id="f54dd-120">Tutti i formati che sarebbero disponibili per la configurazione specificata, indipendentemente dal fatto che vengano affiancati, con alcune eccezioni.</span><span class="sxs-lookup"><span data-stu-id="f54dd-120">All formats that would be available for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="f54dd-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**SampleDesc supportati (conteggio multisample, qualità)**</span><span class="sxs-lookup"><span data-stu-id="f54dd-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Supported SampleDesc (Multisample count, quality)**</span></span>
</dt> <dd>

<span data-ttu-id="f54dd-122">Qualunque sia il supporto per la configurazione specificata, indipendentemente dal fatto che venga affiancato, con alcune eccezioni.</span><span class="sxs-lookup"><span data-stu-id="f54dd-122">Whatever would be supported for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="f54dd-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Larghezza/altezza/MipLevels/ArraySize supportati**</span><span class="sxs-lookup"><span data-stu-id="f54dd-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Supported Width/Height/MipLevels/ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="f54dd-124">Extent completi supportati da Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="f54dd-124">Full extents supported by Direct3D 11.</span></span> <span data-ttu-id="f54dd-125">Le risorse affiancate non hanno la restrizione sulla dimensione totale della memoria imposta sulle risorse non affiancate.</span><span class="sxs-lookup"><span data-stu-id="f54dd-125">Tiled resources don't have the restriction on total memory size imposed on non-tiled resources.</span></span> <span data-ttu-id="f54dd-126">Le risorse affiancate sono limitate solo da limiti di spazio degli indirizzi virtuali complessivi.</span><span class="sxs-lookup"><span data-stu-id="f54dd-126">Tiled resources are only constrained by overall virtual address space limits.</span></span> <span data-ttu-id="f54dd-127">Per informazioni, vedere [spazio degli indirizzi disponibile per le risorse affiancate](address-space-available-for-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="f54dd-127">For info, see [Address space available for tiled resources](address-space-available-for-tiled-resources.md).</span></span>

</dd> </dl>

<span data-ttu-id="f54dd-128">Il contenuto iniziale della memoria del pool di riquadri non è definito.</span><span class="sxs-lookup"><span data-stu-id="f54dd-128">The initial contents of tile pool memory are undefined.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f54dd-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f54dd-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f54dd-130">Creazione di risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="f54dd-130">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




