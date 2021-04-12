---
description: Implementazione di un codificatore di WIC-Enabled
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implementazione di un codificatore di WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232472"
---
# <a name="implementing-a-wic-enabled-encoder"></a><span data-ttu-id="81cd8-103">Implementazione di un codificatore di WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="81cd8-103">Implementing a WIC-Enabled Encoder</span></span>

## <a name="introduction"></a><span data-ttu-id="81cd8-104">Introduzione</span><span class="sxs-lookup"><span data-stu-id="81cd8-104">Introduction</span></span>

<span data-ttu-id="81cd8-105">L'implementazione di un codificatore Windows Imaging Component (WIC) richiede la scrittura di due classi, come accade anche per l'implementazione di un decodificatore WIC.</span><span class="sxs-lookup"><span data-stu-id="81cd8-105">Implementing a Windows Imaging Component (WIC) encoder requires writing two classes, as is also true for implementing a WIC decoder.</span></span> <span data-ttu-id="81cd8-106">Le interfacce di queste classi corrispondono direttamente alle responsabilità del codificatore descritte nella sezione relativa alla [codifica](-wic-howwicworks.md) del funzionamento del componente Windows Imaging.</span><span class="sxs-lookup"><span data-stu-id="81cd8-106">The interfaces on these classes correspond directly to the encoder responsibilities outlined in the [Encoding](-wic-howwicworks.md) section of How The Windows Imaging Component Works.</span></span>

<span data-ttu-id="81cd8-107">Una delle classi fornisce servizi a livello di contenitore e gestisce la serializzazione dei singoli frame di immagine all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="81cd8-107">One of the classes provides container-level services and manages the serialization of the individual image frames within the container.</span></span> <span data-ttu-id="81cd8-108">Questa classe implementa l'interfaccia [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="81cd8-108">This class implements the [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) interface.</span></span> <span data-ttu-id="81cd8-109">Se il formato dell'immagine supporta i metadati a livello di contenitore, è necessario implementare anche l'interfaccia [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) in questa classe.</span><span class="sxs-lookup"><span data-stu-id="81cd8-109">If your image format supports container-level metadata, you must also implement the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface on this class.</span></span>

<span data-ttu-id="81cd8-110">L'altra classe fornisce servizi a livello di frame ed esegue la codifica effettiva dei bit dell'immagine per ogni fotogramma nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="81cd8-110">The other class provides frame-level services and does the actual encoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="81cd8-111">Scorre inoltre i blocchi di metadati per ogni frame e richiede ai writer di metadati appropriati di serializzare i blocchi.</span><span class="sxs-lookup"><span data-stu-id="81cd8-111">It also iterates through the metadata blocks for each frame and requests the appropriate metadata writers to serialize the blocks.</span></span> <span data-ttu-id="81cd8-112">Questa classe implementa l'interfaccia **IWICBitmapFrameEncode** e l'interfaccia [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) .</span><span class="sxs-lookup"><span data-stu-id="81cd8-112">This class implements the **IWICBitmapFrameEncode** interface and the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface.</span></span> <span data-ttu-id="81cd8-113">Questa classe deve avere un membro IStream che la classe a livello di contenitore Inizializza durante la creazione dell'istanza, in cui il metodo **commit** serializza i dati del frame.</span><span class="sxs-lookup"><span data-stu-id="81cd8-113">This class should have an IStream member that the container-level class initializes on instantiation, into which the **Commit** method will serialize the frame data.</span></span>

<span data-ttu-id="81cd8-114">In alcuni casi, ad esempio formati non elaborati, è possibile che l'autore del codec non desideri che le applicazioni siano in grado di codificare o ricodificare nel formato non elaborato, perché lo scopo di un file non elaborato è quello di contenere i dati del sensore esattamente come provengono dalla fotocamera.</span><span class="sxs-lookup"><span data-stu-id="81cd8-114">In some cases, such as raw formats, the codec author may not want applications to be able to encode or re-encode to the raw format, because the purpose of a raw file is to contain the sensor data exactly as it came from the camera.</span></span> <span data-ttu-id="81cd8-115">Nei casi in cui l'autore del codec non vuole abilitare la codifica, è comunque necessario implementare un codificatore rudimentale solo per consentire l'aggiunta di metadati.</span><span class="sxs-lookup"><span data-stu-id="81cd8-115">In cases where the codec author doesn’t want to enable encoding, it is still necessary to implement a rudimentary encoder just to enable adding metadata.</span></span> <span data-ttu-id="81cd8-116">In tal caso, il codificatore deve supportare solo questi metodi necessari per la scrittura dei metadati e può copiare i bit dell'immagine non modificati dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="81cd8-116">In that case, the encoder need only support those methods necessary for writing metadata, and can copy the image bits untouched from the decoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81cd8-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81cd8-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="81cd8-118">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="81cd8-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81cd8-119">**IWICBitmapEncoder**</span><span class="sxs-lookup"><span data-stu-id="81cd8-119">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

<span data-ttu-id="81cd8-120">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="81cd8-120">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="81cd8-121">Implementazione di IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="81cd8-121">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="81cd8-122">Interfacce del codificatore</span><span class="sxs-lookup"><span data-stu-id="81cd8-122">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="81cd8-123">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="81cd8-123">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="81cd8-124">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="81cd8-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



