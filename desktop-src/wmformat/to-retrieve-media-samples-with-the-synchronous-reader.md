---
title: Per recuperare esempi di supporti con il lettore sincrono
description: Per recuperare esempi di supporti con il lettore sincrono
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Formato di sistemi avanzati (ASF), recupero di esempi di supporti
- ASF (Advanced Systems Format), recupero di esempi di supporti
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- lettori sincroni, recupero di esempi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398579"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a><span data-ttu-id="02c08-108">Per recuperare esempi di supporti con il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="02c08-108">To Retrieve Media Samples with the Synchronous Reader</span></span>

<span data-ttu-id="02c08-109">È necessario richiedere ogni campione uno alla volta dal lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="02c08-109">You must request each sample one at a time from the synchronous reader.</span></span> <span data-ttu-id="02c08-110">In questo modo si ottiene un maggiore controllo sugli esempi ricevuti e quando vengono ricevuti.</span><span class="sxs-lookup"><span data-stu-id="02c08-110">This gives you more control over the samples you receive and when you receive them.</span></span>

<span data-ttu-id="02c08-111">Usare il metodo [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) per recuperare un esempio.</span><span class="sxs-lookup"><span data-stu-id="02c08-111">Use the [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) method to retrieve a sample.</span></span> <span data-ttu-id="02c08-112">È necessario passare per lo più i puntatori alle variabili che verranno compilate con informazioni sull'esempio recuperato come parametri.</span><span class="sxs-lookup"><span data-stu-id="02c08-112">You need to pass mostly pointers to variables that will be filled with information about the sample retrieved as parameters.</span></span> <span data-ttu-id="02c08-113">L'unico parametro di input è *wStreamNum*.</span><span class="sxs-lookup"><span data-stu-id="02c08-113">The only input parameter is *wStreamNum*.</span></span> <span data-ttu-id="02c08-114">Se si passa un numero di flusso, **GetNextSample** recupererà l'esempio successivo con il numero di flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="02c08-114">If you pass a stream number, **GetNextSample** will retrieve the next sample with the specified stream number.</span></span> <span data-ttu-id="02c08-115">Se si passa zero per *wStreamNum*, viene recuperato il seguente esempio che si verifica in ordine cronologico nel file.</span><span class="sxs-lookup"><span data-stu-id="02c08-115">If you pass zero for *wStreamNum*, the next sample that occurs chronologically in the file is retrieved.</span></span>

<span data-ttu-id="02c08-116">Per impostazione predefinita, il lettore sincrono recupera tutti gli esempi dagli output in un file in ordine cronologico.</span><span class="sxs-lookup"><span data-stu-id="02c08-116">By default, the synchronous reader retrieves all of the samples from the outputs in a file in chronological order.</span></span> <span data-ttu-id="02c08-117">Se si chiama **GetNextSample** e non sono disponibili altri esempi da ottenere, viene restituito NS \_ e \_ nessun \_ altro \_ campione, ovvero un codice di errore non riuscito.</span><span class="sxs-lookup"><span data-stu-id="02c08-117">If you call **GetNextSample** and there are no more samples to get, it will return NS\_E\_NO\_MORE\_SAMPLES, which is a failed error code.</span></span> <span data-ttu-id="02c08-118">Quando si esegue la codifica, è possibile semplicemente scorrere gli esempi fino a quando il metodo non ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="02c08-118">When coding therefore, you can simply loop through samples until the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="02c08-119">Per assicurarsi che il lettore sincrono fornisca durate di esempio corrette per i flussi video, è necessario innanzitutto configurare l'output del flusso.</span><span class="sxs-lookup"><span data-stu-id="02c08-119">To ensure that the synchronous reader delivers correct sample durations for video streams, you must first configure the stream output.</span></span> <span data-ttu-id="02c08-120">Chiamare il metodo [**IWMSyncReader:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) per impostare l' \_ impostazione g wszVideoSampleDurations su **true**.</span><span class="sxs-lookup"><span data-stu-id="02c08-120">Call the [**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) method to set the g\_wszVideoSampleDurations setting to **TRUE**.</span></span>

 

<span data-ttu-id="02c08-121">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="02c08-121">Example Code</span></span>

<span data-ttu-id="02c08-122">Nell'esempio di codice seguente viene illustrato come utilizzare **GetNextSample** per recuperare tutti gli esempi in un file.</span><span class="sxs-lookup"><span data-stu-id="02c08-122">The following example code shows how to use **GetNextSample** to retrieve all samples in a file.</span></span>


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a><span data-ttu-id="02c08-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02c08-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02c08-124">**Interfaccia IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="02c08-124">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="02c08-125">**Lettura di file con il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="02c08-125">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




