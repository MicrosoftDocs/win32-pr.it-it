---
description: Configurazione del writer ASF
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Configurazione del writer ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a6dfc1827743dce946188ebf9e050226b5c484
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304122"
---
# <a name="configuring-the-asf-writer"></a><span data-ttu-id="62807-103">Configurazione del writer ASF</span><span class="sxs-lookup"><span data-stu-id="62807-103">Configuring the ASF Writer</span></span>

<span data-ttu-id="62807-104">Quando il filtro del [writer ASF WM](wm-asf-writer-filter.md) viene creato, viene configurato automaticamente con il \_ profilo WMProfile \_ V80 256Video.</span><span class="sxs-lookup"><span data-stu-id="62807-104">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile.</span></span> <span data-ttu-id="62807-105">Questo profilo usa i codec Windows Media Audio e Windows Media Video versione 8, che non sono recenti come i codec della serie Windows Media 9.</span><span class="sxs-lookup"><span data-stu-id="62807-105">This profile uses the Windows Media Audio and Windows Media Video version 8 codecs, which are not as recent as the Windows Media 9 Series codecs.</span></span> <span data-ttu-id="62807-106">Si consiglia di creare un profilo personalizzato che usa i codec della serie Windows Media 9 e di configurare il writer ASF WM con il profilo personalizzato, come descritto in [configurazione di profili e altre proprietà del file ASF](configuring-profiles-and-other-asf-file-properties.md).</span><span class="sxs-lookup"><span data-stu-id="62807-106">It is recommended to create a custom profile that uses the Windows Media 9 Series codecs, and configure the WM ASF Writer with the custom profile, as described in [Configuring Profiles and Other ASF File Properties](configuring-profiles-and-other-asf-file-properties.md).</span></span> <span data-ttu-id="62807-107">È necessario aggiungere il filtro del writer ASF WM al grafico filtro prima di configurare il filtro e configurare il filtro prima di connetterlo a tutti gli altri filtri.</span><span class="sxs-lookup"><span data-stu-id="62807-107">You must add the WM ASF Writer filter to the filter graph before configuring the filter, and configure the filter before connecting it to any other filters.</span></span>

<span data-ttu-id="62807-108">Tutti i dati di input devono avere un timestamp e tutti i pin di input devono essere connessi prima di poter eseguire o sospendere il filtro.</span><span class="sxs-lookup"><span data-stu-id="62807-108">All input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="62807-109">Se pertanto si configura il filtro con un profilo con un flusso audio e un flusso video, il filtro creerà un pin di input audio e video ed è necessario che entrambi i pin siano connessi prima di poter eseguire il filtro.</span><span class="sxs-lookup"><span data-stu-id="62807-109">Therefore, if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span> <span data-ttu-id="62807-110">Poiché Windows Media Format SDK richiede il funzionamento di un flusso audio, il writer ASF WM deve avere sempre un pin audio di input, anche se è per un flusso fittizio, ovvero un flusso audio a bassa velocità in bit disattivato.</span><span class="sxs-lookup"><span data-stu-id="62807-110">Because the Windows Media Format SDK requires an audio stream to work, the WM ASF Writer must always have an input audio pin, even if it is for a dummy stream—that is, a muted, low-bit-rate audio stream.</span></span>

<span data-ttu-id="62807-111">Aggiunta di estensioni di unità dati</span><span class="sxs-lookup"><span data-stu-id="62807-111">Adding Data Unit Extensions</span></span>

<span data-ttu-id="62807-112">È possibile configurare un flusso del profilo per le estensioni dell'unità dati, ad esempio i codici temporali SMPTE, prima o dopo la connessione del filtro, purché si segua questo ordine di operazioni:</span><span class="sxs-lookup"><span data-stu-id="62807-112">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="62807-113">Aggiungere una o più estensioni di unità dati al flusso usando **IWMStreamConfig2:: AddDataUnitExtension**.</span><span class="sxs-lookup"><span data-stu-id="62807-113">Add one or more data unit extensions to the stream using **IWMStreamConfig2::AddDataUnitExtension**.</span></span>
2.  <span data-ttu-id="62807-114">Chiamare **IWMProfile:: ReconfigStream** per aggiornare il profilo.</span><span class="sxs-lookup"><span data-stu-id="62807-114">Call **IWMProfile::ReconfigStream** to update the profile.</span></span>
3.  <span data-ttu-id="62807-115">Chiamare [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) con l'oggetto profilo aggiornato.</span><span class="sxs-lookup"><span data-stu-id="62807-115">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) with the updated profile object.</span></span>
4.  <span data-ttu-id="62807-116">Trovare il pin di input del video e chiamare il metodo [**IAMWMBufferPass:: senotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) per registrare l'interfaccia [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="62807-116">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="62807-117">Quando si esegue il grafo, viene chiamato il metodo [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) per ogni frame e sarà possibile ottenere e impostare le proprietà nell'esempio usando i relativi metodi di interfaccia **INSSBuffer3** .</span><span class="sxs-lookup"><span data-stu-id="62807-117">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method will be called for each frame, and you will be able to get and set properties on the sample using its **INSSBuffer3** interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="62807-118">In alcuni scenari con utilizzo intensivo del processore, ad esempio la telecine inversa, il writer ASF WM potrebbe richiedere un maggior numero di buffer di output rispetto ad alcuni filtri downstream che possono supportare.</span><span class="sxs-lookup"><span data-stu-id="62807-118">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="62807-119">Il decodificatore DV, ad esempio, non accetterà più di un buffer per il pin di output e lo stesso vale per il decompressore AVI in determinate condizioni.</span><span class="sxs-lookup"><span data-stu-id="62807-119">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="62807-120">Se si verificano problemi durante il tentativo di connessione a questi filtri o quando si esegue il grafo, potrebbe essere necessario scrivere un filtro intermediario che accetti un numero qualsiasi di buffer nel pin di output.</span><span class="sxs-lookup"><span data-stu-id="62807-120">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="62807-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62807-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62807-122">Creazione di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="62807-122">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



