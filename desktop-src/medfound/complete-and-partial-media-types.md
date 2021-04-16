---
description: In questo argomento viene descritta la differenza tra i tipi di supporto completi e i tipi di supporti parziali.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Tipi di supporti completi e parziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530523"
---
# <a name="complete-and-partial-media-types"></a><span data-ttu-id="79466-103">Tipi di supporti completi e parziali</span><span class="sxs-lookup"><span data-stu-id="79466-103">Complete and Partial Media Types</span></span>

<span data-ttu-id="79466-104">In questo argomento viene descritta la differenza tra i tipi di supporto completi e i tipi di supporti parziali.</span><span class="sxs-lookup"><span data-stu-id="79466-104">This topic describes the difference between complete media types and partial media types.</span></span>

## <a name="complete-media-types"></a><span data-ttu-id="79466-105">Tipi di supporto completi</span><span class="sxs-lookup"><span data-stu-id="79466-105">Complete Media Types</span></span>

<span data-ttu-id="79466-106">Un tipo di supporto *completo* è uno che definisce completamente il formato del flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="79466-106">A *complete* media type is one that fully defines the format of the media stream.</span></span> <span data-ttu-id="79466-107">Dato un tipo di supporto completo, un componente della pipeline può analizzare i dati del flusso associati al tipo di supporto senza ambiguità.</span><span class="sxs-lookup"><span data-stu-id="79466-107">Given a complete media type, a pipeline component can parse the stream data associated with the media type, with no ambiguity.</span></span>

<span data-ttu-id="79466-108">Per i formati non compressi, gli argomenti seguenti definiscono gli attributi necessari per un tipo di supporto completo:</span><span class="sxs-lookup"><span data-stu-id="79466-108">For uncompressed formats, the following topics define the attributes that are required for a complete media type:</span></span>

-   <span data-ttu-id="79466-109">Audio: [tipi di supporti audio non compressi](uncompressed-audio-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="79466-109">Audio: [Uncompressed Audio Media Types](uncompressed-audio-media-types.md)</span></span>
-   <span data-ttu-id="79466-110">Video: [tipi di supporti video non compressi](uncompressed-video-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="79466-110">Video: [Uncompressed Video Media Types](uncompressed-video-media-types.md)</span></span>

<span data-ttu-id="79466-111">Per i flussi compressi (o *codificati*), la definizione di un tipo di supporto completo è definita dal codec.</span><span class="sxs-lookup"><span data-stu-id="79466-111">For compressed (or *encoded*) streams, the definition of a complete media type is defined by the codec.</span></span> <span data-ttu-id="79466-112">Tuttavia, se sono noti attributi di tipo non compressi per il flusso compresso, questi valori devono essere inclusi nel tipo di supporto per il flusso compresso.</span><span class="sxs-lookup"><span data-stu-id="79466-112">However, if any uncompressed type attributes are known for the compressed stream, these values should be included in the media type for the compressed stream.</span></span> <span data-ttu-id="79466-113">Se, ad esempio, le dimensioni del frame sono note, impostare l'attributo [**MF \_ mt \_ frame \_ size**](mf-mt-frame-size-attribute.md) sul tipo di supporto, anche se tecnicamente un flusso compresso non ha una dimensione del frame.</span><span class="sxs-lookup"><span data-stu-id="79466-113">For example, if the frame size is known, set the [**MF\_MT\_FRAME\_SIZE**](mf-mt-frame-size-attribute.md) attribute on the media type, even though technically a compressed stream does not have a frame size.</span></span>

## <a name="partial-media-types"></a><span data-ttu-id="79466-114">Tipi di supporti parziali</span><span class="sxs-lookup"><span data-stu-id="79466-114">Partial Media Types</span></span>

<span data-ttu-id="79466-115">Un tipo di supporto *parziale* non dispone di uno o più attributi necessari per un tipo di supporto completo.</span><span class="sxs-lookup"><span data-stu-id="79466-115">A *partial* media type is lacks one or more of the attributes needed for a complete media type.</span></span> <span data-ttu-id="79466-116">Quando si enumerano i tipi di supporti possibili, un componente Microsoft Media Foundation può lasciare un valore non impostato, per indicare che è in grado di gestire qualsiasi valore.</span><span class="sxs-lookup"><span data-stu-id="79466-116">When enumerating possible media types, a Microsoft Media Foundation component may leave a value unset, to indicate that it can handle any value.</span></span> <span data-ttu-id="79466-117">Ad esempio, un processore video potrebbe lasciare invariato l'attributo della [**\_ \_ \_ frequenza dei fotogrammi MF mt**](mf-mt-frame-rate-attribute.md) per indicare che è in grado di gestire qualsiasi frequenza dei fotogrammi e di eseguire una conversione della frequenza dei fotogrammi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="79466-117">For example, a video processor might leave the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute unset, to indicate that it can handle any frame rate, and will perform a frame-rate conversion if necessary.</span></span>

<span data-ttu-id="79466-118">Se si crea un tipo di supporto parziale, è comunque necessario includere tutte le informazioni che si conoscono.</span><span class="sxs-lookup"><span data-stu-id="79466-118">If you create a partial media type, you should still include as much information as you know.</span></span> <span data-ttu-id="79466-119">Tuttavia, un tipo di supporto non deve includere informazioni non sicure.</span><span class="sxs-lookup"><span data-stu-id="79466-119">However, a media type must not include information that is uncertain.</span></span> <span data-ttu-id="79466-120">È preferibile che le informazioni siano mancanti rispetto a quelle errate.</span><span class="sxs-lookup"><span data-stu-id="79466-120">It is better for information to be missing than wrong.</span></span>

<span data-ttu-id="79466-121">Come minimo, un tipo di supporto parziale deve includere solo due attributi: [**il \_ \_ \_ tipo principale MF mt**](mf-mt-major-type-attribute.md) e il [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="79466-121">At a minimum, a partial media type should include just two attributes: [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) and [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md).</span></span>

<span data-ttu-id="79466-122">A volte Media Foundation componenti deve fornire tipi di supporto completi:</span><span class="sxs-lookup"><span data-stu-id="79466-122">Sometimes Media Foundation components must provide complete media types:</span></span>

-   <span data-ttu-id="79466-123">Le origini multimediali devono fornire tipi di output completi.</span><span class="sxs-lookup"><span data-stu-id="79466-123">Media sources must provide complete output types.</span></span>
-   <span data-ttu-id="79466-124">I decodificatori devono fornire tipi di output completi, dopo l'impostazione del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="79466-124">Decoders must provide complete output types, after the input type is set.</span></span> <span data-ttu-id="79466-125">Prima di impostare il tipo di input, un decodificatore potrebbe fornire un tipo di output parziale.</span><span class="sxs-lookup"><span data-stu-id="79466-125">Before the input type is set, a decoder might provide a partial output type.</span></span>
-   <span data-ttu-id="79466-126">I codificatori devono fornire tipi di input completi, dopo che è stato impostato il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="79466-126">Encoders must provide complete input types, after the output type is set.</span></span> <span data-ttu-id="79466-127">Prima di impostare il tipo di output, è possibile che un codificatore fornisca un tipo di input parziale.</span><span class="sxs-lookup"><span data-stu-id="79466-127">Before the output type is set, an encoder might provide a partial input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79466-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79466-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79466-129">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="79466-129">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



