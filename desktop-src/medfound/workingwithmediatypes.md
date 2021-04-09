---
description: Utilizzo dei tipi di supporto DMO
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Utilizzo dei tipi di supporto DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968877"
---
# <a name="working-with-dmo-media-types"></a><span data-ttu-id="ac0ee-103">Utilizzo dei tipi di supporto DMO</span><span class="sxs-lookup"><span data-stu-id="ac0ee-103">Working with DMO Media Types</span></span>

<span data-ttu-id="ac0ee-104">I tipi di supporto di input e di output utilizzati dal codec DMOs vengono definiti utilizzando la struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="ac0ee-104">The input and output media types that are used by the codec DMOs are defined using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="ac0ee-105">Questa struttura è identica a entrambi [**i \_ \_ tipi di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), che è definito in Windows Media Format SDK e il [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type), definito in Microsoft DirectShow®.</span><span class="sxs-lookup"><span data-stu-id="ac0ee-105">This structure is identical to both [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), which is defined in the Windows Media Format SDK, and [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), which is defined in Microsoft DirectShow®.</span></span> <span data-ttu-id="ac0ee-106">A seconda dell'applicazione, è possibile utilizzare le variabili definite come uno di questi tre tipi.</span><span class="sxs-lookup"><span data-stu-id="ac0ee-106">Depending upon your application, you may use variables defined as any one of these three types.</span></span> <span data-ttu-id="ac0ee-107">È possibile eseguire il cast di un puntatore a una delle strutture del tipo di supporto come un altro.</span><span class="sxs-lookup"><span data-stu-id="ac0ee-107">It is safe to cast a pointer to one of the media type structures as another.</span></span> <span data-ttu-id="ac0ee-108">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="ac0ee-108">For example:</span></span>


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



<span data-ttu-id="ac0ee-109">I tipi di formato usati dai codec sono generalmente limitati a quelli descritti dalle strutture **VIDEOINFOHEADER** e **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="ac0ee-109">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span> <span data-ttu-id="ac0ee-110">Per praticità, le costanti per questi tipi di formato sono incluse nel file di intestazione wmcodecconst. h.</span><span class="sxs-lookup"><span data-stu-id="ac0ee-110">For convenience, constants for these format types are included in the wmcodecconst.h header file.</span></span> <span data-ttu-id="ac0ee-111">I nomi delle costanti sono \_ rispettivamente WMCFORMAT videoinfo e WMCFORMAT \_ WAVEFORMATEX.</span><span class="sxs-lookup"><span data-stu-id="ac0ee-111">The constant names are WMCFORMAT\_VideoInfo and WMCFORMAT\_WaveFormatEx respectively.</span></span> <span data-ttu-id="ac0ee-112">In alcune circostanze, i codec audio possono funzionare con la struttura **WAVEFORMATEXTENSIBLE** e devono essere usati in altri.</span><span class="sxs-lookup"><span data-stu-id="ac0ee-112">The audio codecs can work with the **WAVEFORMATEXTENSIBLE** structure in some circumstances, and must use it in others.</span></span> <span data-ttu-id="ac0ee-113">Tuttavia, **DMO \_ media \_ Type. formatType** è impostato sullo stesso valore di **WAVEFORMATEX**.</span><span class="sxs-lookup"><span data-stu-id="ac0ee-113">However, **DMO\_MEDIA\_TYPE.formattype** is set to the same value as it is for **WAVEFORMATEX**.</span></span> <span data-ttu-id="ac0ee-114">Per altre informazioni sull'uso di **WAVEFORMATEXTENSIBLE**, vedere [uso di High-Definition audio](usinghighdefinitionaudio.md).</span><span class="sxs-lookup"><span data-stu-id="ac0ee-114">For more information about using **WAVEFORMATEXTENSIBLE**, see [Using High-Definition Audio](usinghighdefinitionaudio.md).</span></span>

> [!Note]  
>    <span data-ttu-id="ac0ee-115">È necessario includere la struttura del tipo di formato usata come output del codificatore in qualsiasi contenitore usato per archiviare i dati compressi.</span><span class="sxs-lookup"><span data-stu-id="ac0ee-115">You must include the format type structure used as the encoder output in whatever container you use to store the compressed data.</span></span> <span data-ttu-id="ac0ee-116">I decodificatori richiedono la struttura del formato originale per decomprimere il contenuto.</span><span class="sxs-lookup"><span data-stu-id="ac0ee-116">The decoders require the original format structure to decompress the content.</span></span> <span data-ttu-id="ac0ee-117">Oltre ai membri della struttura, i tipi compressi Windows Media Audio e video richiedono informazioni aggiuntive sul formato, che vengono aggiunte alla struttura.</span><span class="sxs-lookup"><span data-stu-id="ac0ee-117">In addition to the members of the structure, compressed Windows Media Audio and Video types require additional format information, which is appended to the structure.</span></span> <span data-ttu-id="ac0ee-118">Per ulteriori informazioni, vedere [utilizzo di audio](workingwithaudio.md) e [utilizzo di video](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="ac0ee-118">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ac0ee-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ac0ee-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac0ee-120">Uso di codec DMOs</span><span class="sxs-lookup"><span data-stu-id="ac0ee-120">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
