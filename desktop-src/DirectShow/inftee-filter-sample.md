---
description: Esempio di filtro InfTee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Esempio di filtro InfTee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304179"
---
# <a name="inftee-filter-sample"></a><span data-ttu-id="0f7f5-103">Esempio di filtro InfTee</span><span class="sxs-lookup"><span data-stu-id="0f7f5-103">InfTee Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="0f7f5-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f7f5-104">Description</span></span>

<span data-ttu-id="0f7f5-105">Il filtro InfTee fornisce un'implementazione di esempio del filtro del [Pin Tee infinito](infinite-pin-tee-filter.md) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0f7f5-105">The InfTee filter provides a sample implementation of the DirectShow [Infinite Pin Tee](infinite-pin-tee-filter.md) filter.</span></span> <span data-ttu-id="0f7f5-106">Il filtro ha un pin di input e un numero dinamico di pin di output.</span><span class="sxs-lookup"><span data-stu-id="0f7f5-106">The filter has one input pin and a dynamic number of output pins.</span></span> <span data-ttu-id="0f7f5-107">Tutti gli esempi di supporti inviati al filtro vengono distribuiti simultaneamente da tutti i pin di output.</span><span class="sxs-lookup"><span data-stu-id="0f7f5-107">All media samples sent to the filter are delivered simultaneously from all of the output pins.</span></span>

<span data-ttu-id="0f7f5-108">Questo filtro viene visualizzato in GraphEdit sotto il nome "Sample uninfinito Pin Tee" per distinguerlo dal filtro standard infinito Pin Tee fornito in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0f7f5-108">This filter appears in GraphEdit under the name "Sample Infinite Pin Tee," to distinguish it from the standard Infinite Pin Tee filter that is provided in DirectShow.</span></span>

## <a name="usage"></a><span data-ttu-id="0f7f5-109">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0f7f5-109">Usage</span></span>

<span data-ttu-id="0f7f5-110">Poiché questo filtro non modifica i dati ricevuti, tutti i pin devono accettare lo stesso tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="0f7f5-110">Because this filter does not change the data that it receives, all pins must agree to the same media type.</span></span> <span data-ttu-id="0f7f5-111">Durante il processo di connessione, il filtro potrebbe riconnettere alcuni pin per fare in modo che i tipi di supporto corrispondano.</span><span class="sxs-lookup"><span data-stu-id="0f7f5-111">During the connection process, the filter might reconnect some pins in order to make the media types match.</span></span>

<span data-ttu-id="0f7f5-112">I dati che arrivano al pin di input non vengono copiati prima di essere inviati ai pin di output.</span><span class="sxs-lookup"><span data-stu-id="0f7f5-112">Data arriving at the input pin is not copied before it is sent to the output pins.</span></span> <span data-ttu-id="0f7f5-113">Il filtro garantisce inoltre che i dati vengano recapitati ai filtri downstream, per garantire che entrambi gli output ricevano un servizio tempestivo.</span><span class="sxs-lookup"><span data-stu-id="0f7f5-113">The filter also ensures that the data is delivered to the downstream filters, to guarantee that both outputs receive timely service.</span></span> <span data-ttu-id="0f7f5-114">In particolare, se uno degli output può essere bloccato nella funzione membro [**COutputQueue:: Receive**](coutputqueue-receive.md) , il tee gira un thread per recapitare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="0f7f5-114">In particular, if one of the outputs can block in the [**COutputQueue::Receive**](coutputqueue-receive.md) member function, then the tee spins off a thread to deliver the sample.</span></span> <span data-ttu-id="0f7f5-115">Se non è presente alcun thread per recapitare l'esempio, il thread che recapita l'esempio al pin di input Tee potrebbe passare i dati a un filtro downstream; a questo punto, potrebbe bloccarsi, mantenendo i dati dall'altro filtro downstream per lunghi periodi di tempo.</span><span class="sxs-lookup"><span data-stu-id="0f7f5-115">If there were no thread to deliver the sample, then the thread that delivers the sample to the tee input pin might pass the data to a downstream filter; at that point, it might block, keeping data from the other downstream filter for long periods of time.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="0f7f5-116">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="0f7f5-116">Downloading the Sample</span></span>

<span data-ttu-id="0f7f5-117">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0f7f5-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="0f7f5-118">Questo esempio viene installato nel percorso seguente: esempi *\[ radice \] SDK* \\ \\ \\ filtri DirectShow multimediali \\ \\ InfTee.</span><span class="sxs-lookup"><span data-stu-id="0f7f5-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\InfTee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f7f5-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f7f5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f7f5-120">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="0f7f5-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



