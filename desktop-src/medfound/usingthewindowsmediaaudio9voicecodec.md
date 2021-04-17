---
description: Uso del codec Windows Media Audio Voice
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Uso del codec Windows Media Audio Voice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530468"
---
# <a name="using-the-windows-media-audio-voice-codec"></a><span data-ttu-id="4e405-103">Uso del codec Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="4e405-103">Using the Windows Media Audio Voice Codec</span></span>

<span data-ttu-id="4e405-104">Il codec Windows Media Audio Voice fornisce una compressione a bassa velocità in bit ottimizzata per l'audio che contiene la sintesi vocale.</span><span class="sxs-lookup"><span data-stu-id="4e405-104">The Windows Media Audio Voice codec provides low bit-rate compression optimized for audio containing speech.</span></span> <span data-ttu-id="4e405-105">La possibilità che il codec produca questi piccoli esempi è dovuto alla gamma di frequenze limitata dei suoni della voce umana.</span><span class="sxs-lookup"><span data-stu-id="4e405-105">The ability of the codec to produce such small samples is due to the limited frequency range of the sounds of the human voice.</span></span> <span data-ttu-id="4e405-106">Questa ottimizzazione significa che un codificatore vocale dedicato crea output di scarsa qualità per contenuti che contengono suoni più complessi, come la musica.</span><span class="sxs-lookup"><span data-stu-id="4e405-106">This optimization means that a dedicated voice encoder creates poor-quality output for content that contains more complicated sounds, like music.</span></span> <span data-ttu-id="4e405-107">Tuttavia, il codec Windows Media Audio Voice compensa questo potenziale problema di qualità fornendo modalità separate per la voce, la musica e il contenuto misto.</span><span class="sxs-lookup"><span data-stu-id="4e405-107">However, the Windows Media Audio Voice codec compensates for this potential quality issue by providing separate modes for voice, music, and mixed content.</span></span> <span data-ttu-id="4e405-108">Il codec analizza il contenuto misto per determinare la modalità da usare per ogni parte del file.</span><span class="sxs-lookup"><span data-stu-id="4e405-108">The codec analyzes mixed content to determine which mode to use for each portion of the file.</span></span>

<span data-ttu-id="4e405-109">Il codec Windows Media Audio Voice viene implementato nell'oggetto Encoder identificato dall'identificatore di classe CLSID \_ CWMSPEncMediaObject2 e nell'oggetto decodificatore identificato dall'identificatore di classe CLSID \_ CWMSPDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="4e405-109">The Windows Media Audio Voice codec is implemented in the encoder object identified by the class identifier CLSID\_CWMSPEncMediaObject2, and in the decoder object identified by the class identifier CLSID\_CWMSPDecMediaObject.</span></span> <span data-ttu-id="4e405-110">Il tag di formato dei tipi di supporto che usano questo codec è 0x00A.</span><span class="sxs-lookup"><span data-stu-id="4e405-110">The format tag of media types using this codec is 0x00A.</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="4e405-111">Configurazione del codificatore</span><span class="sxs-lookup"><span data-stu-id="4e405-111">Configuring the Encoder</span></span>

<span data-ttu-id="4e405-112">Il codificatore vocale supporta tre modalità: sintesi vocale, musica e mista.</span><span class="sxs-lookup"><span data-stu-id="4e405-112">The voice encoder supports three modes: speech, music, and mixed.</span></span> <span data-ttu-id="4e405-113">Ogni modalità è ottimizzata per ottenere i risultati migliori per quel tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="4e405-113">Each mode is optimized to get the best results for that type of content.</span></span> <span data-ttu-id="4e405-114">È possibile configurare la modalità del codificatore vocale usando i metodi di **IPropertyStore** per impostare la proprietà [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="4e405-114">You can configure the mode of the voice encoder by using the methods of **IPropertyStore** to set the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property.</span></span>

<span data-ttu-id="4e405-115">Quando è configurato per il contenuto misto, il codec Windows Media Audio Voice rileverà automaticamente i passaggi di musica nel contenuto.</span><span class="sxs-lookup"><span data-stu-id="4e405-115">When configured for mixed content, the Windows Media Audio Voice codec will automatically detect passages of music in the content.</span></span> <span data-ttu-id="4e405-116">Se non si è soddisfatti dei risultati, è possibile specificare la posizione della musica nel contenuto usando un elenco di decisioni di modifica (EDL).</span><span class="sxs-lookup"><span data-stu-id="4e405-116">If you are not satisfied with the results, you can specify the location of music in the content using an editing decision list (EDL).</span></span> <span data-ttu-id="4e405-117">Per ulteriori informazioni, vedere [utilizzo di un elenco di decisioni di modifica per la codifica di Voice](usingavoiceeditingdecisionlist.md).</span><span class="sxs-lookup"><span data-stu-id="4e405-117">For more information, see [Using an Editing Decision List for Encoding Voice](usingavoiceeditingdecisionlist.md).</span></span>

<span data-ttu-id="4e405-118">Diversamente dagli altri codificatori audio, è possibile impostare il valore della finestra del buffer per il contenuto vocale usando la proprietà [MFPKEY \_ WMAVOICE \_ enc \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="4e405-118">Unlike the other audio encoders, you can set the buffer window value for voice content by using the [MFPKEY\_WMAVOICE\_ENC\_BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) property.</span></span> <span data-ttu-id="4e405-119">Tuttavia, i valori predefiniti dovrebbero funzionare correttamente nella maggior parte dei casi.</span><span class="sxs-lookup"><span data-stu-id="4e405-119">However, the default values should work fine in most cases.</span></span>

> [!Note]  
>    <span data-ttu-id="4e405-120">Quando si configura il codificatore vocale, è molto importante impostare il tipo di output prima di impostare il tipo di input.</span><span class="sxs-lookup"><span data-stu-id="4e405-120">When configuring the voice encoder, it is very important that you set the output type before you set the input type.</span></span> <span data-ttu-id="4e405-121">Si tratta dell'ordine delle operazioni consigliato per tutti i codec audio, ma il codificatore vocale può segnalare tipi di output errati se viene impostato un input quando si chiama **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="4e405-121">This is the recommended order of operations for all of the audio codecs, but the voice encoder can report erroneous output types if an input is set when you call **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

 

## <a name="decoding"></a><span data-ttu-id="4e405-122">Decodifica</span><span class="sxs-lookup"><span data-stu-id="4e405-122">Decoding</span></span>

<span data-ttu-id="4e405-123">Non sono previsti requisiti speciali per la decodifica dell'audio vocale.</span><span class="sxs-lookup"><span data-stu-id="4e405-123">There are no special requirements for decoding voice audio.</span></span> <span data-ttu-id="4e405-124">Per ulteriori informazioni, vedere [configurazione della decodifica audio](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="4e405-124">Form more information, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e405-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4e405-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e405-126">Utilizzo di audio</span><span class="sxs-lookup"><span data-stu-id="4e405-126">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



