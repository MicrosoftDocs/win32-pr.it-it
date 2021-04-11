---
title: Interfaccia IDWriteFontFallbackBuilder
description: Consente di creare mapping di fallback dei tipi di carattere Unicode e di creare un oggetto del tipo di carattere che esegue il fallback da tali mapping.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Scrittura diretta dell'interfaccia IDWriteFontFallbackBuilder
- Scrittura diretta dell'interfaccia IDWriteFontFallbackBuilder, descritta
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964456"
---
# <a name="idwritefontfallbackbuilder-interface"></a><span data-ttu-id="41c66-105">Interfaccia IDWriteFontFallbackBuilder</span><span class="sxs-lookup"><span data-stu-id="41c66-105">IDWriteFontFallbackBuilder interface</span></span>

<span data-ttu-id="41c66-106">Consente di creare mapping di fallback dei tipi di carattere Unicode e di creare un oggetto del tipo di carattere che esegue il fallback da tali mapping.</span><span class="sxs-lookup"><span data-stu-id="41c66-106">Allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.</span></span>

## <a name="members"></a><span data-ttu-id="41c66-107">Membri</span><span class="sxs-lookup"><span data-stu-id="41c66-107">Members</span></span>

<span data-ttu-id="41c66-108">L'interfaccia **IDWriteFontFallbackBuilder** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="41c66-108">The **IDWriteFontFallbackBuilder** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="41c66-109">**IDWriteFontFallbackBuilder** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="41c66-109">**IDWriteFontFallbackBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="41c66-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="41c66-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="41c66-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="41c66-111">Methods</span></span>

<span data-ttu-id="41c66-112">L'interfaccia **IDWriteFontFallbackBuilder** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="41c66-112">The **IDWriteFontFallbackBuilder** interface has these methods.</span></span>



| <span data-ttu-id="41c66-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="41c66-113">Method</span></span>                                                                      | <span data-ttu-id="41c66-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41c66-114">Description</span></span>                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41c66-115">**AddMapping**</span><span class="sxs-lookup"><span data-stu-id="41c66-115">**AddMapping**</span></span>](idwritefontfallbackbuilder-addmapping.md)                 | <span data-ttu-id="41c66-116">Accoda un singolo mapping all'elenco.</span><span class="sxs-lookup"><span data-stu-id="41c66-116">Appends a single mapping to the list.</span></span> <span data-ttu-id="41c66-117">Chiamare questa volta per ogni mapping aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="41c66-117">Call this once for each additional mapping.</span></span><br/> |
| [<span data-ttu-id="41c66-118">**AddMappings**</span><span class="sxs-lookup"><span data-stu-id="41c66-118">**AddMappings**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | <span data-ttu-id="41c66-119">Aggiungere tutti i mapping da un oggetto fallback del tipo di carattere esistente.</span><span class="sxs-lookup"><span data-stu-id="41c66-119">Add all the mappings from an existing font fallback object.</span></span><br/>                       |
| [<span data-ttu-id="41c66-120">**CreateFontFallback**</span><span class="sxs-lookup"><span data-stu-id="41c66-120">**CreateFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | <span data-ttu-id="41c66-121">Crea l'oggetto fallback finalizzato dai mapping aggiunti.</span><span class="sxs-lookup"><span data-stu-id="41c66-121">Creates the finalized fallback object from the mappings added.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="41c66-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41c66-122">Requirements</span></span>



| <span data-ttu-id="41c66-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c66-123">Requirement</span></span> | <span data-ttu-id="41c66-124">Valore</span><span class="sxs-lookup"><span data-stu-id="41c66-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41c66-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41c66-125">Minimum supported client</span></span><br/> | <span data-ttu-id="41c66-126">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="41c66-126">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="41c66-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41c66-127">Minimum supported server</span></span><br/> | <span data-ttu-id="41c66-128">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="41c66-128">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="41c66-129">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41c66-129">Minimum supported phone</span></span><br/>  | <span data-ttu-id="41c66-130">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="41c66-130">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="41c66-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="41c66-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="41c66-132"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41c66-132"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="41c66-133">DLL</span><span class="sxs-lookup"><span data-stu-id="41c66-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41c66-134"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c66-134"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

