---
title: Configurazione comune a tutti i flussi
description: Configurazione comune a tutti i flussi
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- profili, configurazioni comuni a tutti i flussi
- flussi, configurazioni comuni
- flussi, nomi
- flussi, nomi di connessione
- flussi, numeri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104398786"
---
# <a name="configuration-common-to-all-streams"></a><span data-ttu-id="12acf-108">Configurazione comune a tutti i flussi</span><span class="sxs-lookup"><span data-stu-id="12acf-108">Configuration Common to All Streams</span></span>

<span data-ttu-id="12acf-109">A tutti i flussi, indipendentemente dal tipo, è necessario assegnare un nome di flusso, un nome di connessione e un numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="12acf-109">All streams, regardless of type, should be assigned a stream name, a connection name, and a stream number.</span></span>

<span data-ttu-id="12acf-110">Il nome del flusso è semplicemente un nome descrittivo assegnato al flusso.</span><span class="sxs-lookup"><span data-stu-id="12acf-110">The stream name is simply a descriptive name you assign to the stream.</span></span> <span data-ttu-id="12acf-111">Un flusso non deve avere un nome di flusso, ma consente di identificare il flusso quando si modifica il profilo in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="12acf-111">A stream does not need to have a stream name, but it helps you to identify the stream when editing the profile at a later time.</span></span> <span data-ttu-id="12acf-112">È possibile impostare un nome per il flusso chiamando [**IWMStreamConfig:: Sestreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span><span class="sxs-lookup"><span data-stu-id="12acf-112">You can set a name for the stream by calling [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span></span>

<span data-ttu-id="12acf-113">Ogni flusso deve avere un nome di connessione, detto anche nome di input.</span><span class="sxs-lookup"><span data-stu-id="12acf-113">Every stream should have a connection name, also called an input name.</span></span> <span data-ttu-id="12acf-114">Quando si imposta il profilo nell'oggetto writer per scrivere un file, il writer associa ogni nome di connessione a un input.</span><span class="sxs-lookup"><span data-stu-id="12acf-114">When you set the profile in the writer object to write a file, the writer will associate each connection name with an input.</span></span> <span data-ttu-id="12acf-115">Per identificare gli input, è necessario chiamare [**IWMInputMediaProps:: Getconnectname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) per recuperare il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="12acf-115">To identify the inputs, you must call [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) to retrieve the connection name.</span></span> <span data-ttu-id="12acf-116">I nomi di connessione tipici sono semplici descrizioni del contenuto, ad esempio "audio".</span><span class="sxs-lookup"><span data-stu-id="12acf-116">Typical connection names are simple descriptions of the content, such as "audio".</span></span> <span data-ttu-id="12acf-117">Se il profilo contiene flussi che si escludono a vicenda in base alla velocità in bit, ognuno dei flussi che si escludono a vicenda deve avere lo stesso nome di connessione.</span><span class="sxs-lookup"><span data-stu-id="12acf-117">If your profile contains streams that are mutually exclusive by bit rate, each of the mutually exclusive streams must have the same connection name.</span></span> <span data-ttu-id="12acf-118">In caso contrario, il profilo non è valido e verrà rifiutato dal writer.</span><span class="sxs-lookup"><span data-stu-id="12acf-118">If they do not, the profile is invalid and will be rejected by the writer.</span></span> <span data-ttu-id="12acf-119">È possibile impostare un nome di connessione chiamando [**IWMStreamConfig:: Seconnectname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span><span class="sxs-lookup"><span data-stu-id="12acf-119">You can set a connection name by calling [**IWMStreamConfig::SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span></span>

<span data-ttu-id="12acf-120">Il numero di flusso identifica il flusso all'interno del file.</span><span class="sxs-lookup"><span data-stu-id="12acf-120">The stream number identifies the stream within the file.</span></span> <span data-ttu-id="12acf-121">A differenza dei numeri di input e dei numeri di output, i numeri di flusso iniziano da 1, non da 0.</span><span class="sxs-lookup"><span data-stu-id="12acf-121">Unlike input numbers and output numbers, stream numbers start at 1, not 0.</span></span> <span data-ttu-id="12acf-122">Un numero di flusso è diverso da un indice del flusso, che è possibile usare quando si recuperano i flussi in un profilo usando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span><span class="sxs-lookup"><span data-stu-id="12acf-122">A stream number is different than a stream index, which you use when getting streams in a profile by using [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span> <span data-ttu-id="12acf-123">L'indice del flusso è un numero assegnato al flusso dall'oggetto profilo.</span><span class="sxs-lookup"><span data-stu-id="12acf-123">The stream index is a number assigned to the stream by the profile object.</span></span> <span data-ttu-id="12acf-124">Gli indici di flusso sono compresi tra 0 e uno inferiore al numero di flussi recuperato da [**IWMProfile:: GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span><span class="sxs-lookup"><span data-stu-id="12acf-124">Stream indexes range between 0 and one less than the number of streams retrieved by [**IWMProfile::GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span></span> <span data-ttu-id="12acf-125">I numeri di flusso non devono essere sequenziali, anche se in genere sono e possono variare da 1 a 63.</span><span class="sxs-lookup"><span data-stu-id="12acf-125">Stream numbers need not be sequential, though they usually are, and can range from 1 to 63.</span></span> <span data-ttu-id="12acf-126">È possibile impostare un numero di flusso chiamando [**IWMStreamConfig:: SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span><span class="sxs-lookup"><span data-stu-id="12acf-126">You can set a stream number by calling [**IWMStreamConfig::SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12acf-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12acf-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12acf-128">**Configurazione di flussi**</span><span class="sxs-lookup"><span data-stu-id="12acf-128">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="12acf-129">**Input, flussi e output**</span><span class="sxs-lookup"><span data-stu-id="12acf-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




