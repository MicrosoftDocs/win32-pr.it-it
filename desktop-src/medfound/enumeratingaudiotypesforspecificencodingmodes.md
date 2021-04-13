---
description: Enumerazione dei tipi audio per modalità di codifica specifiche
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Enumerazione dei tipi audio per modalità di codifica specifiche (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401533"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a><span data-ttu-id="a02ea-103">Enumerazione dei tipi audio per modalità di codifica specifiche (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="a02ea-103">Enumerating Audio Types for Specific Encoding Modes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="a02ea-104">I tipi di supporto di input e di output accettati dal codificatore audio sono molto strutturati.</span><span class="sxs-lookup"><span data-stu-id="a02ea-104">The input and output media types accepted by the audio encoder are very structured.</span></span> <span data-ttu-id="a02ea-105">È necessario ottenere i tipi di output supportati chiamando il metodo **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="a02ea-105">You must obtain supported output types by calling **IMediaObject::GetOutputType** method or **IMFTransform::GetOutputType**.</span></span> <span data-ttu-id="a02ea-106">Una volta ottenuto un tipo di output, non è necessario modificarlo.</span><span class="sxs-lookup"><span data-stu-id="a02ea-106">After you get an output type, you must not alter it.</span></span>

<span data-ttu-id="a02ea-107">Se si vuole usare una modalità di codifica diversa da un CBR a un passaggio, è necessario impostare la modalità e quindi enumerare i tipi di output per tale modalità; il codificatore modifica i tipi di output supportati a seconda della modalità impostata.</span><span class="sxs-lookup"><span data-stu-id="a02ea-107">If you want to use an encoding mode other than one-pass CBR, you must set the mode and then enumerate the output types for that mode; the encoder changes the supported output types depending upon the mode set.</span></span> <span data-ttu-id="a02ea-108">Le proprietà che controllano la modalità di codifica sono [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) e [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a02ea-108">The properties that control the encoding mode are [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) and [**MFPKEY\_PASSESUSED**](mfpkey-passesusedproperty.md).</span></span> <span data-ttu-id="a02ea-109">Quando la modalità è impostata nel codificatore, è necessario enumerare e selezionare un tipo di output, usandolo senza modifiche, come per CBR.</span><span class="sxs-lookup"><span data-stu-id="a02ea-109">When the mode is set in the encoder, you must enumerate and select an output type, using it without alteration, just as with CBR.</span></span>

## <a name="identifying-quality-based-vbr-types"></a><span data-ttu-id="a02ea-110">Identificazione di tipi VBR basati sulla qualità</span><span class="sxs-lookup"><span data-stu-id="a02ea-110">Identifying Quality Based VBR Types</span></span>

<span data-ttu-id="a02ea-111">La procedura per identificare i tipi VBR basati sulla qualità varia a seconda che il codificatore funga da oggetto DMO (DirectX Media Object) o funga da Media Foundation Transform (MFT).</span><span class="sxs-lookup"><span data-stu-id="a02ea-111">The procedure for identifying quality based VBR types depends on whether the encoder is acting as a DirectX Media Object (DMO) or acting as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="a02ea-112">Per informazioni su quando un codificatore funge da DMO o da un MFT, vedere le pagine di riferimento del singolo codec in [oggetti codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="a02ea-112">For information on when an encoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="a02ea-113">Quando un codificatore audio funge da DMO e si configura il codificatore per l'uso di un VBR con un solo passaggio, vengono enumerati tutti i tipi di output supportati.</span><span class="sxs-lookup"><span data-stu-id="a02ea-113">When an audio encoder is acting as a DMO and you configure the encoder to use one-pass VBR, it enumerates all of the supported output types.</span></span> <span data-ttu-id="a02ea-114">Tuttavia, in genere si vuole selezionare un tipo VBR a un passaggio basato sul parametro Quality.</span><span class="sxs-lookup"><span data-stu-id="a02ea-114">However, you will typically want to select a one-pass VBR type based on the quality parameter.</span></span> <span data-ttu-id="a02ea-115">Il codificatore inserisce il valore di qualità per i tipi di output VBR a un passaggio nel membro **nAvgBytesPerSec** della struttura **WAVEFORMATEX** a cui fa riferimento **DMO \_ media \_ Type. pbFormat**.</span><span class="sxs-lookup"><span data-stu-id="a02ea-115">The encoder puts the quality value for one-pass VBR output types in the **nAvgBytesPerSec** member of the **WAVEFORMATEX** structure pointed to by **DMO\_MEDIA\_TYPE.pbFormat**.</span></span>

<span data-ttu-id="a02ea-116">Questo valore viene archiviato nel formato seguente: 0x7FFFFFXX, dove XX è il valore qualitativo (compreso tra 0 e 100).</span><span class="sxs-lookup"><span data-stu-id="a02ea-116">This value is stored in the following format: 0x7FFFFFXX, where XX is the quality value (from 0 to 100).</span></span> <span data-ttu-id="a02ea-117">Il valore **nAvgBytesPerSec** di 0x7FFFFF62, ad esempio, specifica il livello di qualità 98 (0x62 = 98).</span><span class="sxs-lookup"><span data-stu-id="a02ea-117">For example, the **nAvgBytesPerSec** value of 0x7FFFFF62 specifies quality level 98 (0x62 = 98).</span></span>

<span data-ttu-id="a02ea-118">Nell'esempio seguente viene illustrato come controllare il livello di qualità di un formato quando il codificatore funge da DMO.</span><span class="sxs-lookup"><span data-stu-id="a02ea-118">The following example shows how to check the quality level of a format when the encoder is acting as a DMO.</span></span>


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



<span data-ttu-id="a02ea-119">Quando il codificatore funge da MFT ed enumera un tipo di output in una chiamata a **GetAvailableOutputType**, è possibile eseguire una query su MFT per la **proprietà \_ \_ \_ \_ VBRQUALITY enumerata più di recente MFPKEY** .</span><span class="sxs-lookup"><span data-stu-id="a02ea-119">When the encoder is acting as an MFT and it enumerates an output type on a call to **GetAvailableOutputType**, you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="a02ea-120">Il valore restituito indica la qualità VBR del tipo di supporto di output restituito più di recente.</span><span class="sxs-lookup"><span data-stu-id="a02ea-120">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="a02ea-121">È quindi possibile usare tale valore per impostare la [**proprietà \_ \_ VBRQUALITY desiderata MFPKEY**](mfpkey-desired-vbrqualityproperty.md) del codificatore.</span><span class="sxs-lookup"><span data-stu-id="a02ea-121">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="setting-peak-constraints"></a><span data-ttu-id="a02ea-122">Impostazione di vincoli di picco</span><span class="sxs-lookup"><span data-stu-id="a02ea-122">Setting Peak Constraints</span></span>

<span data-ttu-id="a02ea-123">Per la qualità VBR (One-Pass) e il VBR con due passaggi non vincolati, non sono necessarie impostazioni aggiuntive dopo il recupero del tipo di output.</span><span class="sxs-lookup"><span data-stu-id="a02ea-123">For quality based VBR (one-pass) and unconstrained two-pass VBR, no additional settings are required after retrieving the output type.</span></span> <span data-ttu-id="a02ea-124">Per usare un VBR con vincoli di picco, recuperare un tipo di output con VBR abilitato e due set di sessioni.</span><span class="sxs-lookup"><span data-stu-id="a02ea-124">To use peak-constrained VBR, retrieve an output type with VBR enabled and two passes set.</span></span> <span data-ttu-id="a02ea-125">Questo tipo, senza modifiche, descrive le impostazioni VBR non vincolate.</span><span class="sxs-lookup"><span data-stu-id="a02ea-125">This type, without alteration, describes unconstrained VBR settings.</span></span> <span data-ttu-id="a02ea-126">Per impostare i vincoli di picco, impostare le proprietà [MFPKEY \_ Rmax](mfpkey-rmaxproperty.md) e [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="a02ea-126">To set peak constraints, set the [MFPKEY\_RMAX](mfpkey-rmaxproperty.md) and [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a02ea-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a02ea-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a02ea-128">Configurazione della codifica audio</span><span class="sxs-lookup"><span data-stu-id="a02ea-128">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="a02ea-129">Ricerca di tipi di output del codificatore audio</span><span class="sxs-lookup"><span data-stu-id="a02ea-129">Finding Audio Encoder Output Types</span></span>](findingaudioencoderoutputtypes.md)
</dt> <dt>

[<span data-ttu-id="a02ea-130">Uso della codifica Two-Pass</span><span class="sxs-lookup"><span data-stu-id="a02ea-130">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="a02ea-131">Uso della codifica VBR</span><span class="sxs-lookup"><span data-stu-id="a02ea-131">Using VBR Encoding</span></span>](usingvbrencoding.md)
</dt> </dl>

 

 



