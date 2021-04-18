---
description: Uso di maniglie
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Uso di maniglie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d3a1c43703ac662d44854b0fc6bad8b280c368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318671"
---
# <a name="working-with-crossbars"></a><span data-ttu-id="4815f-103">Uso di maniglie</span><span class="sxs-lookup"><span data-stu-id="4815f-103">Working with Crossbars</span></span>

<span data-ttu-id="4815f-104">Se una scheda di acquisizione video ha più di un input fisico o supporta più di un percorso hardware per i dati, il grafico del filtro può contenere il [filtro della traversa video analogo](analog-video-crossbar-filter.md).</span><span class="sxs-lookup"><span data-stu-id="4815f-104">If a video capture card has more than one physical input, or supports more than one hardware path for data, then the filter graph may contain the [Analog Video Crossbar Filter](analog-video-crossbar-filter.md).</span></span> <span data-ttu-id="4815f-105">Il generatore del grafico di acquisizione aggiunge automaticamente questo filtro quando necessario; sarà upstream dal filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4815f-105">The Capture Graph Builder automatically adds this filter when needed; it will be upstream from the capture filter.</span></span> <span data-ttu-id="4815f-106">A seconda dell'hardware, il grafico del filtro potrebbe contenere più di un'istanza del filtro traversa.</span><span class="sxs-lookup"><span data-stu-id="4815f-106">Depending on the hardware, the filter graph might contain more than one instance of the crossbar filter.</span></span>

<span data-ttu-id="4815f-107">Il filtro traversa espone l'interfaccia [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) , che può essere usata per indirizzare un particolare input a un determinato output.</span><span class="sxs-lookup"><span data-stu-id="4815f-107">The crossbar filter exposes the [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) interface, which you can use to route a particular input to a particular output.</span></span> <span data-ttu-id="4815f-108">Ad esempio, una scheda video potrebbe avere un connettore coassiale e un input S-video.</span><span class="sxs-lookup"><span data-stu-id="4815f-108">For example, a video card might have a coaxial connector and an S-Video input.</span></span> <span data-ttu-id="4815f-109">Questi verranno rappresentati come pin di input sul filtro traversa.</span><span class="sxs-lookup"><span data-stu-id="4815f-109">These would be represented as input pins on the crossbar filter.</span></span> <span data-ttu-id="4815f-110">Per selezionare un input, indirizzare il pin di input corrispondente al pin di output della traversa, usando il metodo [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .</span><span class="sxs-lookup"><span data-stu-id="4815f-110">To select an input, route the corresponding input pin to the crossbar's output pin, using the [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) method.</span></span>

<span data-ttu-id="4815f-111">Per individuare i filtri traversa nel grafico, è possibile usare il metodo [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) per cercare i filtri che supportano **IAMCrossbar**.</span><span class="sxs-lookup"><span data-stu-id="4815f-111">To locate crossbar filters in the graph, you can use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to search for filters that support **IAMCrossbar**.</span></span> <span data-ttu-id="4815f-112">Il codice seguente, ad esempio, consente di cercare due maniglie:</span><span class="sxs-lookup"><span data-stu-id="4815f-112">For example, the following code searches for two crossbars:</span></span>


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



<span data-ttu-id="4815f-113">Per un approccio più generalizzato, vedere la classe CCrossbar nell' [esempio AMCap](amcap-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4815f-113">For a more generalized approach, see the CCrossbar class in the [AmCap Sample](amcap-sample.md).</span></span>

<span data-ttu-id="4815f-114">Quando si dispone di un puntatore all'interfaccia **IAMCrossbar** , è possibile ottenere informazioni sul filtro traversa, incluso il tipo fisico di ogni pin e la matrice di cui è possibile indirizzare i pin di input ai pin di output.</span><span class="sxs-lookup"><span data-stu-id="4815f-114">Once you have a pointer to the **IAMCrossbar** interface, you can get information about the crossbar filter, including the physical type of each pin, and the matrix of which input pins can be routed to which output pins.</span></span>

-   <span data-ttu-id="4815f-115">Per determinare il tipo di connettore fisico a cui corrisponde un PIN, chiamare il metodo [**IAMCrossbar:: Get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) .</span><span class="sxs-lookup"><span data-stu-id="4815f-115">To determine the type of physical connector to which a pin corresponds, call the [**IAMCrossbar::get\_CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) method.</span></span> <span data-ttu-id="4815f-116">Il metodo restituisce un membro dell'enumerazione [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) .</span><span class="sxs-lookup"><span data-stu-id="4815f-116">The method returns a member of the [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) enumeration.</span></span> <span data-ttu-id="4815f-117">Un pin S-video, ad esempio, restituisce il valore PhysConn \_ video \_ SVIDEO.</span><span class="sxs-lookup"><span data-stu-id="4815f-117">For example, an S-Video pin returns the value PhysConn\_Video\_SVideo.</span></span>

    <span data-ttu-id="4815f-118">Il metodo **get \_ CrossbarInfo** indica inoltre se due pin sono correlati tra loro.</span><span class="sxs-lookup"><span data-stu-id="4815f-118">The **get\_CrossbarInfo** method also indicates whether two pins are related to each other.</span></span> <span data-ttu-id="4815f-119">Ad esempio, un pin del sintonizzatore video potrebbe essere correlato a un pin del sintonizzatore audio.</span><span class="sxs-lookup"><span data-stu-id="4815f-119">For example, a video tuner pin might be related to an audio tuner pin.</span></span> <span data-ttu-id="4815f-120">I pin correlati hanno la stessa direzione del PIN e fanno in genere parte dello stesso connettore o connettore fisico della scheda.</span><span class="sxs-lookup"><span data-stu-id="4815f-120">Related pins have the same pin direction, and are typically part of the same physical jack or connector on the card.</span></span>

-   <span data-ttu-id="4815f-121">Per determinare se è possibile instradare un pin di input a un pin di output specifico, chiamare il metodo [**IAMCrossbar:: CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) .</span><span class="sxs-lookup"><span data-stu-id="4815f-121">To determine whether you can route an input pin to a particular output pin, call the [**IAMCrossbar::CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) method.</span></span>
-   <span data-ttu-id="4815f-122">Per determinare il routing corrente tra i pin, chiamare il metodo [**IAMCrossbar:: Get \_ IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) .</span><span class="sxs-lookup"><span data-stu-id="4815f-122">To determine the current routing between pins, call the [**IAMCrossbar::get\_IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) method.</span></span>

<span data-ttu-id="4815f-123">I metodi precedenti specificano tutti i pin in base al numero di indice, con i pin di output e i pin di input entrambi indicizzati da zero.</span><span class="sxs-lookup"><span data-stu-id="4815f-123">The previous methods all specify pins by index number, with output pins and input pins both indexed from zero.</span></span> <span data-ttu-id="4815f-124">Chiamare il metodo **IAMCrossbar:: Get \_ PinCounts** per trovare il numero di pin sul filtro.</span><span class="sxs-lookup"><span data-stu-id="4815f-124">Call the **IAMCrossbar::get\_PinCounts** method to find the number of pins on the filter.</span></span>

<span data-ttu-id="4815f-125">Il codice seguente, ad esempio, Visualizza le informazioni su un filtro traversa per la finestra della console:</span><span class="sxs-lookup"><span data-stu-id="4815f-125">For example, the following code displays information about a crossbar filter to the console window:</span></span>


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



<span data-ttu-id="4815f-126">Per una scheda ipotetica, questa funzione potrebbe produrre l'output seguente:</span><span class="sxs-lookup"><span data-stu-id="4815f-126">For a hypothetical card, this function might produce the following output:</span></span>


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



<span data-ttu-id="4815f-127">Sul lato output, il video S e il sintonizzatore video sono entrambi correlati al decodificatore audio.</span><span class="sxs-lookup"><span data-stu-id="4815f-127">On the output side, the S-Video and the video tuner are both related to the audio decoder.</span></span> <span data-ttu-id="4815f-128">Sul lato input, il sintonizzatore video è correlato al sintonizzatore audio e il video S è correlato alla riga audio in.</span><span class="sxs-lookup"><span data-stu-id="4815f-128">On the input side, the video tuner is related to the audio tuner, and the S-Video is related to the audio line in.</span></span> <span data-ttu-id="4815f-129">L'input S-video viene indirizzato all'output S-video; e l'input del sintonizzatore video viene indirizzato all'output del sintonizzatore video.</span><span class="sxs-lookup"><span data-stu-id="4815f-129">The S-Video input is routed to the S-Video output; and the video tuner input is routed to the video tuner output.</span></span> <span data-ttu-id="4815f-130">Attualmente nessun elemento viene indirizzato al decoder audio, ma è possibile instradare la riga audio in o il sintonizzatore audio.</span><span class="sxs-lookup"><span data-stu-id="4815f-130">Currently nothing is routed to the audio decoder, but either the audio line in or the audio tuner could be routed to it.</span></span>

<span data-ttu-id="4815f-131">È possibile modificare il routing esistente chiamando il metodo [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .</span><span class="sxs-lookup"><span data-stu-id="4815f-131">You can change the existing routing by calling the [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) method.</span></span>

 

 



