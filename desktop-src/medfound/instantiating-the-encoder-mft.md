---
description: Creazione di un'istanza di un codificatore MFT
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Creazione di un'istanza di un codificatore MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5344c19a3a00c659efbbfd88d42176b876528380
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232536"
---
# <a name="instantiating-an-encoder-mft"></a><span data-ttu-id="3ba0f-103">Creazione di un'istanza di un codificatore MFT</span><span class="sxs-lookup"><span data-stu-id="3ba0f-103">Instantiating an Encoder MFT</span></span>

<span data-ttu-id="3ba0f-104">In Microsoft Media Foundation i codificatori vengono implementati come [trasformazioni di Media Foundation](media-foundation-transforms.md) (MFTS).</span><span class="sxs-lookup"><span data-stu-id="3ba0f-104">In Microsoft Media Foundation, encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs).</span></span> <span data-ttu-id="3ba0f-105">Prima di creare un codificatore, è necessario innanzitutto trovare il codificatore più adatto alle proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="3ba0f-105">Before creating an encoder, you must first find the encoder that is most suited to your needs.</span></span>

-   <span data-ttu-id="3ba0f-106">Codec audio Windows Media</span><span class="sxs-lookup"><span data-stu-id="3ba0f-106">Windows Media audio codecs</span></span>

    <span data-ttu-id="3ba0f-107">Categoria: **\_ \_ \_ codificatore audio della categoria MFT**</span><span class="sxs-lookup"><span data-stu-id="3ba0f-107">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="3ba0f-108">Tipo principale: MFMediaType \_ audio</span><span class="sxs-lookup"><span data-stu-id="3ba0f-108">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="3ba0f-109">Sottotipo: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF</span><span class="sxs-lookup"><span data-stu-id="3ba0f-109">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="3ba0f-110">Codec video di Windows Media</span><span class="sxs-lookup"><span data-stu-id="3ba0f-110">Windows Media video codecs</span></span>

    <span data-ttu-id="3ba0f-111">Categoria: **\_ \_ \_ codificatore video della categoria MFT**</span><span class="sxs-lookup"><span data-stu-id="3ba0f-111">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="3ba0f-112">Tipo principale: video di MFMediaType \_</span><span class="sxs-lookup"><span data-stu-id="3ba0f-112">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="3ba0f-113">Sottotipo: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat WMV2 \_ , MFVideoFormat \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="3ba0f-113">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="3ba0f-114">Media Foundation offre diverse funzioni che l'applicazione può chiamare per enumerare i vari codificatori disponibili nel sistema.</span><span class="sxs-lookup"><span data-stu-id="3ba0f-114">Media Foundation provides several functions that your application can call to enumerate the various encoders available in your system.</span></span> <span data-ttu-id="3ba0f-115">I codificatori sono registrati come oggetti COM e la voce del registro di sistema segue il formato standard per le class factory COM.</span><span class="sxs-lookup"><span data-stu-id="3ba0f-115">Encoders are registered as COM objects and the registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="3ba0f-116">Il registro di sistema gestisce i CLSID per i codificatori, classificati in base al formato multimediale (audio o video).</span><span class="sxs-lookup"><span data-stu-id="3ba0f-116">The registry maintains the CLSIDs for the encoders, which are categorized by the media format (audio or video).</span></span> <span data-ttu-id="3ba0f-117">Gli identificatori di classe dei codificatori Windows Media sono definiti come costanti nel file di intestazione wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="3ba0f-117">The class identifiers of the Windows Media encoders are defined as constants in the wmcodecdsp.h header file.</span></span> <span data-ttu-id="3ba0f-118">In Media Foundation, i codificatori possono essere registrati tramite chiamate a [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) specificando pullula, i tipi di input supportati e i tipi di output supportati.</span><span class="sxs-lookup"><span data-stu-id="3ba0f-118">In Media Foundation, the encoders can be registered through calls to [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) by specifying the catergory, the supported input types, and the supported output types.</span></span> <span data-ttu-id="3ba0f-119">Una volta completata la registrazione tramite queste funzioni, i MFTs vengono considerati dalle funzioni di enumerazione Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3ba0f-119">Upon successful registration through these functions, the MFTs are considered by the Media Foundation enumeration functions.</span></span>

<span data-ttu-id="3ba0f-120">Per creare un'istanza di un codificatore MFT, un'applicazione ha le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3ba0f-120">For creating an instance of an encoder MFT, an application has the following choices.</span></span>

-   <span data-ttu-id="3ba0f-121">Creare direttamente il codificatore MFT e ricevere un puntatore all'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="3ba0f-121">Create the encoder MFT directly and receive a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="3ba0f-122">Per ulteriori informazioni, vedere [creazione di un codificatore tramite CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span><span class="sxs-lookup"><span data-stu-id="3ba0f-122">For more information, see [Creating an Encoder by Using CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span></span>
-   <span data-ttu-id="3ba0f-123">Creare un'istanza dell'oggetto Activation per il codificatore MFT e ricevere un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="3ba0f-123">Create an instance of the activation object for the encoder MFT and receive a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="3ba0f-124">Per ulteriori informazioni, vedere [utilizzo degli oggetti di attivazione di un codificatore](using-an-encoder-s-activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3ba0f-124">For more information, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="3ba0f-125">Se l'applicazione usa [componenti ASF di livello pipeline](pipeline-layer-asf-components.md) per codificare un file in formato ASF, è necessario inserire il codificatore MFT nella pipeline come nodo di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="3ba0f-125">If your application is using [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) to encode a file to ASF format, you must insert the encoder MFT into the pipeline as a transform node.</span></span> <span data-ttu-id="3ba0f-126">Durante la creazione del nodo Transform nella topologia di codifica, è possibile impostare il tipo di oggetto come puntatore all'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) o all'oggetto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="3ba0f-126">While creating the transform node in the encoding topology, you can either set the object type as a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface or the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object.</span></span> <span data-ttu-id="3ba0f-127">Media Foundation fornisce oggetti attivazione per codificatori Windows Media, in modo che possano essere impostati comodamente come nodo di trasformazione nella topologia di codifica.</span><span class="sxs-lookup"><span data-stu-id="3ba0f-127">Media Foundation provides activation objects for Windows Media encoders so that they can be conveniently set as the transform node in the encoding topology.</span></span> <span data-ttu-id="3ba0f-128">Quando la topologia viene risolta, la sessione multimediale usa l'oggetto attivazione per creare un'istanza del codificatore MFT.</span><span class="sxs-lookup"><span data-stu-id="3ba0f-128">When the topology is resolved, the Media Session uses the activation object to create an instance of the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ba0f-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3ba0f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ba0f-130">Codificatori Windows Media</span><span class="sxs-lookup"><span data-stu-id="3ba0f-130">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



