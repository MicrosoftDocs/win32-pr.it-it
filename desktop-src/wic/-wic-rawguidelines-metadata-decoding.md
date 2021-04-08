---
description: Decodifica
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Decodifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883962"
---
# <a name="decoding"></a><span data-ttu-id="b0d7a-103">Decodifica</span><span class="sxs-lookup"><span data-stu-id="b0d7a-103">Decoding</span></span>

<span data-ttu-id="b0d7a-104">Per supportare correttamente i metadati, gli autori del decodificatore devono eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0d7a-104">To properly support metadata, decoder authors must do the following:</span></span>

-   <span data-ttu-id="b0d7a-105">Implementare le interfacce [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="b0d7a-105">Implement [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interfaces.</span></span>
-   <span data-ttu-id="b0d7a-106">Implementare [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) nel decodificatore di frame.</span><span class="sxs-lookup"><span data-stu-id="b0d7a-106">Implement [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on the frame decoder.</span></span> <span data-ttu-id="b0d7a-107">Se il codec supporta i metadati a livello di contenitore, questa interfaccia deve essere implementata nel decodificatore a livello di contenitore e nel decodificatore di frame.</span><span class="sxs-lookup"><span data-stu-id="b0d7a-107">If the codec supports container-level metadata, this interface must be implemented on the container-level decoder as well as on the frame decoder.</span></span>
-   <span data-ttu-id="b0d7a-108">Durante la decodifica del flusso di immagini, chiamare [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) per creare un'istanza di un lettore di metadati per ogni blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="b0d7a-108">While decoding the image stream, call [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) to instantiate a metadata reader for each metadata block.</span></span> <span data-ttu-id="b0d7a-109">(Tutti i nuovi lettori di metadati implementati dal codec devono essere registrati con WIC).</span><span class="sxs-lookup"><span data-stu-id="b0d7a-109">(Any new metadata readers that the codec implements must be registered with WIC.)</span></span>

    <span data-ttu-id="b0d7a-110">Il decodificatore non deve creare i lettori di metadati in modo autonomo, bensì utilizzare WIC per crearli in base ai blocchi di metadati nel flusso.</span><span class="sxs-lookup"><span data-stu-id="b0d7a-110">The decoder should not create metadata readers on its own, but rather use WIC to create them based on the metadata blocks in the stream.</span></span> <span data-ttu-id="b0d7a-111">Il decodificatore deve eseguire questa operazione su tutti i blocchi che trova, anche se non sono noti in modo nativo a docoder, perché i lettori di metadati futuri potrebbero essere installati nel sistema in grado di gestire questi blocchi di metadati.</span><span class="sxs-lookup"><span data-stu-id="b0d7a-111">The decoder must do this on all blocks that it finds, even if they are not natively known to the docoder, because future metadata readers might be installed on the system that do understand how to handle these metadata blocks.</span></span>

-   <span data-ttu-id="b0d7a-112">Se non è presente alcun gestore di metadati per un blocco, creare un'istanza del lettore di metadati sconosciuti usando le opzioni di creazione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="b0d7a-112">If there is no metadata handler for a block, instantiate the unknown metadata reader by using the metadata creation options.</span></span>
-   <span data-ttu-id="b0d7a-113">Esporre la raccolta di Reader di metadati tramite l'interfaccia [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="b0d7a-113">Expose the collection of metadata readers through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0d7a-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0d7a-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b0d7a-115">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b0d7a-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b0d7a-116">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="b0d7a-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="b0d7a-117">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="b0d7a-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="b0d7a-118">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="b0d7a-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



