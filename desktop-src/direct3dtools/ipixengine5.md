---
description: Estensioni per l'interfaccia IPixEngine4 contenente aggiunte per la visualizzazione di trame.
MS-HAID: vspixengine.IPixEngine5
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPixEngine5
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8995B617-6830-4A07-8C83-B5925E033967
api_name:
- IPixEngine5
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 300ed31eae5d8ff4009f28691c5348db7cd89d6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521385"
---
# <a name="span-idvspixengineipixengine5spanipixengine5-interface"></a><span data-ttu-id="17e34-103"><span id="vspixengine.ipixengine5"></span>Interfaccia IPixEngine5</span><span class="sxs-lookup"><span data-stu-id="17e34-103"><span id="vspixengine.ipixengine5"></span>IPixEngine5 interface</span></span>

<span data-ttu-id="17e34-104">Estensioni per l'interfaccia IPixEngine4 contenente aggiunte per la visualizzazione di trame.</span><span class="sxs-lookup"><span data-stu-id="17e34-104">Extensions to the IPixEngine4 interface containing additions for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="17e34-105">Membri</span><span class="sxs-lookup"><span data-stu-id="17e34-105">Members</span></span>

<span data-ttu-id="17e34-106">L'interfaccia **IPixEngine5** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="17e34-106">The **IPixEngine5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="17e34-107">**IPixEngine5** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="17e34-107">**IPixEngine5** also has these types of members:</span></span>

-   [<span data-ttu-id="17e34-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="17e34-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="17e34-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="17e34-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="17e34-110">L'interfaccia **IPixEngine5** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="17e34-110">The **IPixEngine5** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="17e34-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="17e34-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="17e34-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17e34-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="17e34-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="17e34-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="17e34-114">Libera una trama e notifica l'host in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="17e34-114">Frees a texture and notifies the host asynchronously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="17e34-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="17e34-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="17e34-116">Richiesta asincrona di caricamento dei dati dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="17e34-116">An asynchronous request to load histogram data.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="17e34-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="17e34-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="17e34-118">Carica una trama da un file e notifica l'host in modo asincrono quando viene completato.</span><span class="sxs-lookup"><span data-stu-id="17e34-118">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="17e34-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="17e34-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="17e34-120">Carica una sezione di trama e notifica all'host asynchrnously quando viene completato.</span><span class="sxs-lookup"><span data-stu-id="17e34-120">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="17e34-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="17e34-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="17e34-122">Legge un valore Texel e restituisce il risultato al asynchrnously host.</span><span class="sxs-lookup"><span data-stu-id="17e34-122">Reads a texel value and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="17e34-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="17e34-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="17e34-124">Esegue il rendering di una trama in un file e restituisce il risultato al asynchrnously host.</span><span class="sxs-lookup"><span data-stu-id="17e34-124">Renders a texture to a file and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="17e34-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="17e34-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="17e34-126">Salva una trama.</span><span class="sxs-lookup"><span data-stu-id="17e34-126">Saves a texture.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="17e34-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17e34-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="17e34-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17e34-128">Header</span></span></p></td><td><span data-ttu-id="17e34-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="17e34-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
