---
title: Funzioni di base (grafica Direct3D 12)
description: Le funzioni seguenti sono dichiarate in d3d12. h.
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: 99ec8516634a0a59262df9862e03732c9d6d579a
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "106299281"
---
# <a name="core-functions"></a><span data-ttu-id="9a2a8-103">Funzioni di base</span><span class="sxs-lookup"><span data-stu-id="9a2a8-103">Core functions</span></span>

<span data-ttu-id="9a2a8-104">Le funzioni seguenti sono dichiarate in d3d12. h.</span><span class="sxs-lookup"><span data-stu-id="9a2a8-104">The following functions are declared in d3d12.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9a2a8-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="9a2a8-105">In this section</span></span>

| <span data-ttu-id="9a2a8-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="9a2a8-106">Topic</span></span> | <span data-ttu-id="9a2a8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a2a8-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="9a2a8-108">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-108">**D3D12CreateDevice**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | <span data-ttu-id="9a2a8-109">Crea un dispositivo che rappresenta l'adattatore di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a2a8-109">Creates a device that represents the display adapter.</span></span> |
| [<span data-ttu-id="9a2a8-110">**D3D12CreateRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-110">**D3D12CreateRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | <span data-ttu-id="9a2a8-111">Deserializza una firma radice per poter determinare la definizione del layout ([**D3D12 \_ root \_ Signature \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)).</span><span class="sxs-lookup"><span data-stu-id="9a2a8-111">Deserializes a root signature so you can determine the layout definition ([**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)).</span></span> |
| [<span data-ttu-id="9a2a8-112">**D3D12CreateVersionedRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-112">**D3D12CreateVersionedRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | <span data-ttu-id="9a2a8-113">Genera un'interfaccia che può restituire la struttura dei dati deserializzati tramite [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).</span><span class="sxs-lookup"><span data-stu-id="9a2a8-113">Generates an interface that can return the deserialized data structure, via [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).</span></span> |
| [<span data-ttu-id="9a2a8-114">**D3D12EnableExperimentalFeatures**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-114">**D3D12EnableExperimentalFeatures**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | <span data-ttu-id="9a2a8-115">Consente un elenco di funzionalità sperimentali.</span><span class="sxs-lookup"><span data-stu-id="9a2a8-115">Enables a list of experimental features.</span></span> |
| [<span data-ttu-id="9a2a8-116">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-116">**D3D12GetDebugInterface**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | <span data-ttu-id="9a2a8-117">Ottiene un'interfaccia di debug.</span><span class="sxs-lookup"><span data-stu-id="9a2a8-117">Gets a debug interface.</span></span> |
| [<span data-ttu-id="9a2a8-118">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-118">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | <span data-ttu-id="9a2a8-119">Serializza una firma radice versione 1,0 che può essere passata a [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="9a2a8-119">Serializes a root signature version 1.0 that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |
| [<span data-ttu-id="9a2a8-120">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-120">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | <span data-ttu-id="9a2a8-121">Serializza una firma radice di qualsiasi versione che può essere passata a [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="9a2a8-121">Serializes a root signature of any version that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="9a2a8-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a2a8-122">Related topics</span></span>

* [<span data-ttu-id="9a2a8-123">Riferimento principale</span><span class="sxs-lookup"><span data-stu-id="9a2a8-123">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="9a2a8-124">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9a2a8-124">Direct3D 12 reference</span></span>](direct3d-12-reference.md)






