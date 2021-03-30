---
title: Enumerazioni di livelli
description: Questa sezione contiene informazioni sulle enumerazioni dei livelli.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- enumerazioni, livello Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976919"
---
# <a name="layer-enumerations"></a><span data-ttu-id="6cd0a-104">Enumerazioni di livelli</span><span class="sxs-lookup"><span data-stu-id="6cd0a-104">Layer Enumerations</span></span>

<span data-ttu-id="6cd0a-105">Questa sezione contiene informazioni sulle enumerazioni dei livelli.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-105">This section contains information about the layer enumerations.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="6cd0a-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6cd0a-106">In this section</span></span>



| <span data-ttu-id="6cd0a-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="6cd0a-107">Topic</span></span>                                                                                             | <span data-ttu-id="6cd0a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cd0a-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cd0a-109">**\_Categoria del messaggio d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="6cd0a-109">**D3D11\_MESSAGE\_CATEGORY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | <span data-ttu-id="6cd0a-110">Categorie di messaggi di debug.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-110">Categories of debug messages.</span></span> <span data-ttu-id="6cd0a-111">Questa operazione identificherà la categoria di un messaggio quando si recupera un messaggio con [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) e quando si aggiunge un messaggio con [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span><span class="sxs-lookup"><span data-stu-id="6cd0a-111">This will identify the category of a message when retrieving a message with [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) and when adding a message with [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <span data-ttu-id="6cd0a-112">Quando si crea un [**filtro coda informazioni**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), questi valori possono essere usati per consentire o negare a qualsiasi categoria di messaggi di passare attraverso i filtri di archiviazione e recupero.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-112">When creating an [**info queue filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.</span></span><br/> |
| [<span data-ttu-id="6cd0a-113">**\_ID messaggio \_ d3d11**</span><span class="sxs-lookup"><span data-stu-id="6cd0a-113">**D3D11\_MESSAGE\_ID**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | <span data-ttu-id="6cd0a-114">Messaggi di debug per la configurazione di un filtro di Accodamento informazioni (vedere [**d3d11 \_ info \_ Queue \_ Filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); usare questi messaggi per consentire o negare alle categorie di messaggi di passare attraverso i filtri di archiviazione e recupero.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-114">Debug messages for setting up an info-queue filter (see [**D3D11\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); use these messages to allow or deny message categories to pass through the storage and retrieval filters.</span></span> <span data-ttu-id="6cd0a-115">Questi ID vengono usati da metodi quali [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) o [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span><span class="sxs-lookup"><span data-stu-id="6cd0a-115">These IDs are used by methods such as [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) or [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <br/>                                                             |
| [<span data-ttu-id="6cd0a-116">**\_Gravità del messaggio d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="6cd0a-116">**D3D11\_MESSAGE\_SEVERITY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | <span data-ttu-id="6cd0a-117">Livelli di gravità dei messaggi di debug per una coda di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-117">Debug message severity levels for an information queue.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="6cd0a-118">**\_Flag RLDO \_ d3d11**</span><span class="sxs-lookup"><span data-stu-id="6cd0a-118">**D3D11\_RLDO\_FLAGS**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | <span data-ttu-id="6cd0a-119">Opzioni per la quantità di informazioni per segnalare la durata di un oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-119">Options for the amount of information to report about a device object's lifetime.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="6cd0a-120">**\_ \_ Opzioni di rilevamento Shader \_ d3d11**</span><span class="sxs-lookup"><span data-stu-id="6cd0a-120">**D3D11\_SHADER\_TRACKING\_OPTIONS**</span></span>](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | <span data-ttu-id="6cd0a-121">Opzioni che specificano come eseguire il rilevamento del debug dello shader.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-121">Options that specify how to perform shader debug tracking.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="6cd0a-122">**\_Tipo di risorsa di rilevamento Shader d3d11 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6cd0a-122">**D3D11\_SHADER\_TRACKING\_RESOURCE\_TYPE**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | <span data-ttu-id="6cd0a-123">Indica i tipi di risorse da rilevare.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-123">Indicates which resource types to track.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="6cd0a-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6cd0a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cd0a-125">Riferimento al livello</span><span class="sxs-lookup"><span data-stu-id="6cd0a-125">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





