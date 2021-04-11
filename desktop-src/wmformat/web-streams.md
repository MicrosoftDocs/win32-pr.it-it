---
title: Flussi Web
description: Flussi Web
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- Windows Media Format SDK, flussi Web
- Formati di sistemi avanzati (ASF), flussi Web
- ASF (formato avanzato dei sistemi), flussi Web
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- Flussi Web, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044643"
---
# <a name="web-streams"></a><span data-ttu-id="9cf81-110">Flussi Web</span><span class="sxs-lookup"><span data-stu-id="9cf81-110">Web Streams</span></span>

<span data-ttu-id="9cf81-111">Un flusso Web è simile a un flusso di file in quanto contiene file di dati.</span><span class="sxs-lookup"><span data-stu-id="9cf81-111">A Web stream is like a file stream in that it contains data files.</span></span> <span data-ttu-id="9cf81-112">In un flusso Web, questi file sono in genere pagine HTML e grafica associata in formato GIF o JPEG.</span><span class="sxs-lookup"><span data-stu-id="9cf81-112">In a Web stream, these files are typically HTML pages and associated graphics in GIF or JPEG format.</span></span>

<span data-ttu-id="9cf81-113">I flussi Web possono essere particolarmente utili per i file ASF usati come presentazioni.</span><span class="sxs-lookup"><span data-stu-id="9cf81-113">Web streams can be particularly useful for ASF files that are used as presentations.</span></span> <span data-ttu-id="9cf81-114">Prima del supporto dei flussi Web, le presentazioni avrebbero URL nei flussi di script all'interno di un file, in modo da consentire il caricamento di una pagina Web in un momento predeterminato.</span><span class="sxs-lookup"><span data-stu-id="9cf81-114">Prior to the support of Web streams, presentations would have URLs in script streams within a file so that a Web page would load at a predetermined time.</span></span> <span data-ttu-id="9cf81-115">La difficoltà era che la congestione della rete poteva causare ritardi e creare un'esperienza di visualizzazione scadente.</span><span class="sxs-lookup"><span data-stu-id="9cf81-115">The difficulty was that network congestion could cause delays and create a poor viewing experience.</span></span>

<span data-ttu-id="9cf81-116">Con i flussi Web, le parti costitutive di pagine Web possono essere incluse nel file ASF come flusso.</span><span class="sxs-lookup"><span data-stu-id="9cf81-116">With Web streams, the constituent parts of Web pages can be included in the ASF file as a stream.</span></span> <span data-ttu-id="9cf81-117">Man mano che vengono ricevuti, i file possono essere memorizzati nella cache in modo che, quando il comando per visualizzare o eseguire il rendering di un URL venga recapitato, è possibile accedervi immediatamente da un browser.</span><span class="sxs-lookup"><span data-stu-id="9cf81-117">As the files are received, they can be cached so that, when the command to display (or render) a URL is delivered, they can be instantly accessed by a browser.</span></span> <span data-ttu-id="9cf81-118">Ciò consente una riproduzione uniforme e uniforme.</span><span class="sxs-lookup"><span data-stu-id="9cf81-118">This enables smooth, consistent playback.</span></span> <span data-ttu-id="9cf81-119">Il comando Render viene recapitato nel flusso Web, non come comando script in un flusso separato.</span><span class="sxs-lookup"><span data-stu-id="9cf81-119">The render command is delivered in the Web stream itself, not as a script command in a separate stream.</span></span>

<span data-ttu-id="9cf81-120">È consigliabile che i flussi Web creati usando Windows Media Format 9 Series SDK o versione successiva abbiano il numero di versione 1.</span><span class="sxs-lookup"><span data-stu-id="9cf81-120">It is recommended that Web streams created by using the Windows Media Format 9 Series SDK, or later be given the version number 1.</span></span> <span data-ttu-id="9cf81-121">Questo valore viene specificato nella struttura [**del \_ \_ formato webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) nel membro **wVersion** .</span><span class="sxs-lookup"><span data-stu-id="9cf81-121">This value is specified in the [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure in the **wVersion** member.</span></span> <span data-ttu-id="9cf81-122">L'SDK non esegue alcuna operazione per applicare questa versione.</span><span class="sxs-lookup"><span data-stu-id="9cf81-122">The SDK itself does nothing to enforce this version.</span></span>

> [!Note]  
> <span data-ttu-id="9cf81-123">Quando ci si connette a flussi broadcast live con flussi Web, è possibile che l'utente riceva un comando Render prima che il file specificato sia effettivamente nella cache locale.</span><span class="sxs-lookup"><span data-stu-id="9cf81-123">When connecting to live broadcast streams that have Web streams, it is possible that the user may receive a render command before the specified file is actually in the local cache.</span></span> <span data-ttu-id="9cf81-124">A meno che l'applicazione non gestisca questa condizione, nel browser verrà visualizzato l'errore "pagina non trovata".</span><span class="sxs-lookup"><span data-stu-id="9cf81-124">Unless your application handles this condition, the browser will display a "Page not found" error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9cf81-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9cf81-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cf81-126">**Flussi arbitrari**</span><span class="sxs-lookup"><span data-stu-id="9cf81-126">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="9cf81-127">**Configurazione di flussi Web**</span><span class="sxs-lookup"><span data-stu-id="9cf81-127">**Configuring Web Streams**</span></span>](configuring-web-streams.md)
</dt> </dl>

 

 




