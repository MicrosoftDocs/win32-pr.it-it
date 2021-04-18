---
description: Uso del codec della schermata Windows Media Video 9
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Uso del codec Windows Media Video 9 screen (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320457"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a><span data-ttu-id="e5609-103">Uso del codec Windows Media Video 9 screen (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="e5609-103">Using the Windows Media Video 9 Screen Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="e5609-104">Il codec Windows Media Video 9 screen è ottimizzato per comprimere il *video dell'applicazione*, che è costituito da screenshot consecutivi per lo schermo di un computer.</span><span class="sxs-lookup"><span data-stu-id="e5609-104">The Windows Media Video 9 Screen codec is optimized for compressing *application video*, which consists of consecutive screen shots for a computer display.</span></span> <span data-ttu-id="e5609-105">Il codec sfrutta la semplicità tipica delle immagini (relativamente pochi colori, molte linee rette e così via) e la mancanza di movimento relativa per ottenere un rapporto di compressione molto elevato.</span><span class="sxs-lookup"><span data-stu-id="e5609-105">The codec takes advantage of the typical image simplicity (relatively few colors, lots of straight lines, and so on) and relative lack of motion to achieve a very high compression ratio.</span></span> <span data-ttu-id="e5609-106">Lo svantaggio di questa ottimizzazione è che il video non conforme alle caratteristiche previste del video dell'applicazione può essere difficile da comprimere con un livello di qualità accettabile.</span><span class="sxs-lookup"><span data-stu-id="e5609-106">The disadvantage of this optimization is that video that doesn't conform to the expected characteristics of application video can be difficult to compress with an acceptable level of quality.</span></span>

<span data-ttu-id="e5609-107">Il codificatore di schermata Windows Media Video 9 è identificato dall'identificatore di classe CLSID \_ CMSSEncMediaObject2 e il decodificatore è identificato dall'identificatore di classe CLSID \_ CMSSDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="e5609-107">The Windows Media Video 9 Screen encoder is identified by the class identifier CLSID\_CMSSEncMediaObject2, and the decoder is identified the class identifier CLSID\_CMSSDecMediaObject.</span></span> <span data-ttu-id="e5609-108">Il valore di FOURCC per i tipi di supporto che usano questo codec è "MSS2".</span><span class="sxs-lookup"><span data-stu-id="e5609-108">The FOURCC value for media types using this codec is "MSS2".</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="e5609-109">Configurazione del codificatore</span><span class="sxs-lookup"><span data-stu-id="e5609-109">Configuring the Encoder</span></span>

<span data-ttu-id="e5609-110">Il codificatore del codec Windows Media Video 9 screen viene configurato esattamente come il decoder video standard.</span><span class="sxs-lookup"><span data-stu-id="e5609-110">The encoder of the Windows Media Video 9 Screen codec is configured in the same way as the standard video decoder.</span></span>

> [!Note]  
> <span data-ttu-id="e5609-111">Il codificatore dello schermo supporta solo la codifica con un solo passaggio.</span><span class="sxs-lookup"><span data-stu-id="e5609-111">The screen encoder supports only one-pass encoding.</span></span> <span data-ttu-id="e5609-112">È possibile impostare la proprietà [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) su 2 ed elaborare gli input due volte senza errori, ma non vi è alcun vantaggio.</span><span class="sxs-lookup"><span data-stu-id="e5609-112">You can set the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2 and process the inputs twice without error, but there is no benefit to doing so.</span></span> <span data-ttu-id="e5609-113">Si tratta di un problema noto che può essere corretto nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="e5609-113">This is a known issue and may be corrected in future releases.</span></span>

 

## <a name="getting-the-best-results"></a><span data-ttu-id="e5609-114">Ottenere risultati ottimali</span><span class="sxs-lookup"><span data-stu-id="e5609-114">Getting the Best Results</span></span>

<span data-ttu-id="e5609-115">Se si scopre che la qualità desiderata nel contenuto di acquisizione schermo richiede una velocità in bit superiore rispetto a quella che è possibile usare per lo scenario di distribuzione, è possibile provare le tecniche seguenti per ottenere maggiore efficienza dal codec:</span><span class="sxs-lookup"><span data-stu-id="e5609-115">If you discover that the quality you want in your screen capture content requires a higher bit rate than you can use for your delivery scenario, you can try the following techniques to get more efficiency from the codec:</span></span>

-   <span data-ttu-id="e5609-116">Usare una risoluzione più piccola per l'acquisizione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="e5609-116">Use a smaller resolution for the screen capture.</span></span> <span data-ttu-id="e5609-117">L'acquisizione di una risoluzione dello schermo superiore a quella necessaria può confondere il Visualizzatore presentando informazioni non necessarie.</span><span class="sxs-lookup"><span data-stu-id="e5609-117">Capturing a larger screen resolution than needed can confuse the viewer by presenting unnecessary information.</span></span>
-   <span data-ttu-id="e5609-118">Usare una frequenza di fotogrammi più lenta.</span><span class="sxs-lookup"><span data-stu-id="e5609-118">Use a slower frame rate.</span></span> <span data-ttu-id="e5609-119">Le acquisizioni di schermate possono spesso essere efficaci a frequenze di frame molto ridotte (a volte con un minimo di 4 o 5 fotogrammi al secondo).</span><span class="sxs-lookup"><span data-stu-id="e5609-119">Screen captures can often be effective at very low frame rates (sometimes as low as 4 or 5 frames per second).</span></span>
-   <span data-ttu-id="e5609-120">Usare un minor numero di elementi grafici nell'acquisizione schermo.</span><span class="sxs-lookup"><span data-stu-id="e5609-120">Use fewer graphics in the screen capture.</span></span> <span data-ttu-id="e5609-121">Il codec Windows Media Video 9 screen è ottimizzato per codificare primitive e testo di Windows con qualità elevata.</span><span class="sxs-lookup"><span data-stu-id="e5609-121">The Windows Media Video 9 Screen codec is optimized to encode Windows primitives and text with high quality.</span></span> <span data-ttu-id="e5609-122">In genere si verificano problemi a causa di immagini bitmap, che spesso contengono migliaia di colori singoli.</span><span class="sxs-lookup"><span data-stu-id="e5609-122">Usually problems occur because of bitmapped graphics, which often contain thousands of individual colors.</span></span> <span data-ttu-id="e5609-123">Il minor numero di bitmap visualizzate sullo schermo quando si acquisisce, migliore sarà il risultato.</span><span class="sxs-lookup"><span data-stu-id="e5609-123">The fewer bitmaps that are on the screen when you capture, the better your results will be.</span></span> <span data-ttu-id="e5609-124">Se non è possibile eliminare grafica dall'acquisizione schermo, esistono diversi modi per ridurre al minimo l'effetto di una bitmap sulla qualità dell'immagine:</span><span class="sxs-lookup"><span data-stu-id="e5609-124">If you cannot eliminate graphics from your screen capture, there are several ways to minimize the impact that a bitmap has on image quality:</span></span>
    -   <span data-ttu-id="e5609-125">Ridurre le dimensioni dell'elemento grafico.</span><span class="sxs-lookup"><span data-stu-id="e5609-125">Reduce the size of the graphic.</span></span>
    -   <span data-ttu-id="e5609-126">Ridurre il numero di singoli elementi grafici visualizzati sullo schermo nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="e5609-126">Reduce the number of individual graphics that appear on the screen at the same time.</span></span>
    -   <span data-ttu-id="e5609-127">Ridurre la quantità di movimento del grafico.</span><span class="sxs-lookup"><span data-stu-id="e5609-127">Reduce the amount of movement of the graphic.</span></span> <span data-ttu-id="e5609-128">Se, ad esempio, l'immagine si trova in una finestra, conservarla nel modo più stazionale possibile.</span><span class="sxs-lookup"><span data-stu-id="e5609-128">For example, if the graphic is in a window, keep the window as stationary as possible.</span></span>
    -   <span data-ttu-id="e5609-129">Evitare di spostare il puntatore del mouse sul grafico o di trascinare finestre o altri elementi sul grafico.</span><span class="sxs-lookup"><span data-stu-id="e5609-129">Avoid moving the mouse pointer over the graphic, or dragging windows or other elements over the graphic.</span></span>

## <a name="decoding"></a><span data-ttu-id="e5609-130">Decodifica</span><span class="sxs-lookup"><span data-stu-id="e5609-130">Decoding</span></span>

<span data-ttu-id="e5609-131">Non sono previsti requisiti speciali per la decodifica del video di acquisizione schermo.</span><span class="sxs-lookup"><span data-stu-id="e5609-131">There are no special requirements for decoding screen capture video.</span></span> <span data-ttu-id="e5609-132">Tuttavia, come con tutti i Windows Media Video 9 codec, il decodificatore di acquisizione schermo non può decomprimere correttamente il contenuto codificato senza i dati privati del codec.</span><span class="sxs-lookup"><span data-stu-id="e5609-132">However, as with all Windows Media Video 9 codecs, the screen capture decoder cannot properly decompress the encoded content without the codec private data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5609-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5609-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5609-134">Configurazione della codifica video</span><span class="sxs-lookup"><span data-stu-id="e5609-134">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="e5609-135">Uso di dati privati del codec video</span><span class="sxs-lookup"><span data-stu-id="e5609-135">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="e5609-136">Codificatore dello schermo Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e5609-136">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> <dt>

[<span data-ttu-id="e5609-137">Uso dei video</span><span class="sxs-lookup"><span data-stu-id="e5609-137">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



