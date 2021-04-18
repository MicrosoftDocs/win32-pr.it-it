---
description: Codifica
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codifica (componente Windows Imaging)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6d15b983b7455d0fe0c406cbad64dbbb77588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315943"
---
# <a name="encoding-windows-imaging-component"></a><span data-ttu-id="8c19b-103">Codifica (componente Windows Imaging)</span><span class="sxs-lookup"><span data-stu-id="8c19b-103">Encoding (Windows Imaging Component)</span></span>

<span data-ttu-id="8c19b-104">L'autore del codificatore deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8c19b-104">The encoder author must do the following:</span></span>

-   <span data-ttu-id="8c19b-105">Implementare le interfacce [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="8c19b-105">Implement [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) interfaces.</span></span>
-   <span data-ttu-id="8c19b-106">Implementare [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) nel codificatore di frame.</span><span class="sxs-lookup"><span data-stu-id="8c19b-106">Implement [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on the frame encoder.</span></span> <span data-ttu-id="8c19b-107">Se il codec supporta i metadati a livello di contenitore, questa interfaccia deve essere implementata nel codificatore a livello di contenitore e nel codificatore di frame.</span><span class="sxs-lookup"><span data-stu-id="8c19b-107">If the codec supports container-level metadata, this interface must be implemented on the container-level encoder as well as on the frame encoder.</span></span>
-   <span data-ttu-id="8c19b-108">Se il formato del contenitore contiene implicitamente eventuali blocchi di metadati obbligatori, creare un'istanza di un writer di metadati per ogni blocco di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="8c19b-108">If the container format implicitly contains any mandatory metadata blocks, instantiate a metadata writer for each such block.</span></span> <span data-ttu-id="8c19b-109">Il formato TIFF, ad esempio, richiede un dispositivo di interfaccia (IFD) per ogni fotogramma, quindi il writer IFD deve sempre essere esposto.</span><span class="sxs-lookup"><span data-stu-id="8c19b-109">For example, the TIFF format requires an interface device (IFD) for each frame, so the IFD writer must always be exposed.</span></span>
-   <span data-ttu-id="8c19b-110">Implementare il supporto per la gestione della raccolta di writer di metadati.</span><span class="sxs-lookup"><span data-stu-id="8c19b-110">Implement support for managing the collection of metadata writers.</span></span> <span data-ttu-id="8c19b-111">Il writer del blocco gestisce tutti i requisiti dell'ordine o le restrizioni del contenitore sui tipi di blocchi di metadati che possono essere codificati.</span><span class="sxs-lookup"><span data-stu-id="8c19b-111">The block writer manages any order requirements or container restrictions on the kinds of metadata blocks that can be encoded.</span></span> <span data-ttu-id="8c19b-112">Il writer del blocco deve verificare che tutti i nuovi writer di metadati possano essere incorporati nel formato del contenitore.</span><span class="sxs-lookup"><span data-stu-id="8c19b-112">The block writer must verify that any new metadata writers can be embedded within the container format.</span></span>
-   <span data-ttu-id="8c19b-113">Quando si codifica il flusso di immagini, chiamare [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) per serializzare il contenuto di ogni writer di metadati nel flusso.</span><span class="sxs-lookup"><span data-stu-id="8c19b-113">When encoding the image stream, call [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) to serialize each metadata writer’s content into the stream.</span></span> <span data-ttu-id="8c19b-114">Se il blocco di metadati contiene metadati "critici", il codificatore deve impostare gli elementi di metadati critici prima di chiedere al writer dei metadati di serializzare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="8c19b-114">If the metadata block contains "critical" metadata the encoder must set the critical metadata items before asking the metadata writer to serialize content.</span></span>
-   <span data-ttu-id="8c19b-115">Verificare la presenza di gestori di metadati sconosciuti per assicurarsi che i blocchi di metadati ridondanti non siano presenti.</span><span class="sxs-lookup"><span data-stu-id="8c19b-115">Check for any unknown metadata handlers to ensure that redundant metadata blocks are not present.</span></span> <span data-ttu-id="8c19b-116">Questo è importante perché, mantenendo i metadati in uno scenario di decodifica o codifica, i blocchi sconosciuti potrebbero essere un duplicato di blocchi di metadati obbligatori.</span><span class="sxs-lookup"><span data-stu-id="8c19b-116">This is important because, while preserving metadata in a decode or encode scenario, unknown blocks might be a duplicate of mandatory metadata blocks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c19b-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c19b-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8c19b-118">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8c19b-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8c19b-119">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="8c19b-119">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="8c19b-120">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="8c19b-120">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="8c19b-121">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="8c19b-121">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



