---
title: Per forzare l'inserimento di Key-Frame
description: Per forzare l'inserimento di Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Formato di sistemi avanzati (ASF), forzatura degli inserimenti di fotogrammi chiave
- ASF (Advanced Systems Format), forzando gli inserimenti di fotogrammi chiave
- ASF (Advanced Systems Format), inserimento di fotogrammi chiave
- ASF (formato avanzato dei sistemi), inserimento di fotogrammi chiave
- fotogrammi chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23006eef1e51d8bc63f2d55cac22e09a2052d83e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104472390"
---
# <a name="to-force-key-frame-insertion"></a><span data-ttu-id="5aefd-108">Per forzare l'inserimento di Key-Frame</span><span class="sxs-lookup"><span data-stu-id="5aefd-108">To Force Key-Frame Insertion</span></span>

<span data-ttu-id="5aefd-109">Il codec Windows Media Video 9 supporta l'inserimento di fotogrammi chiave forzato.</span><span class="sxs-lookup"><span data-stu-id="5aefd-109">The Windows Media Video 9 codec supports forced key-frame insertion.</span></span> <span data-ttu-id="5aefd-110">Quando si passa un campione al writer, è possibile specificare che deve essere codificato come [*fotogramma chiave*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5aefd-110">When you pass a sample to the writer, you can specify that it must be encoded as a [*key frame*](wmformat-glossary.md).</span></span>

<span data-ttu-id="5aefd-111">Per forzare l'inserimento di fotogrammi chiave per un esempio, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="5aefd-111">To force key-frame insertion for a sample, perform the following steps.</span></span>

1.  <span data-ttu-id="5aefd-112">Allocare un buffer per contenere l'esempio e recuperare un puntatore all'interfaccia [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) contenente il buffer chiamando [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span><span class="sxs-lookup"><span data-stu-id="5aefd-112">Allocate a buffer to hold the sample, and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface containing the buffer by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="5aefd-113">Recuperare il percorso e le dimensioni del buffer creato nel passaggio 1 chiamando [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span><span class="sxs-lookup"><span data-stu-id="5aefd-113">Retrieve the location and size of the buffer created in step 1 by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span></span>
3.  <span data-ttu-id="5aefd-114">Copiare i dati di esempio nella posizione del buffer, assicurandosi che l'esempio passato venga inserito nel buffer allocato.</span><span class="sxs-lookup"><span data-stu-id="5aefd-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="5aefd-115">A seconda dell'origine degli esempi, è possibile usare un'ampia gamma di funzioni per copiare i dati.</span><span class="sxs-lookup"><span data-stu-id="5aefd-115">Depending upon the source of your samples, you can use a variety of functions to copy the data.</span></span> <span data-ttu-id="5aefd-116">Ad esempio, se si copia un flusso da un file AVI, è possibile usare la funzione AVI **AVIStreamRead**.</span><span class="sxs-lookup"><span data-stu-id="5aefd-116">For example, if you are copying a stream from an AVI file, you can use the AVI function, **AVIStreamRead**.</span></span>
4.  <span data-ttu-id="5aefd-117">Aggiornare la quantità di dati utilizzati nel buffer in modo da riflettere le dimensioni effettive dell'esempio chiamando [**INSSBuffer:: selength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span><span class="sxs-lookup"><span data-stu-id="5aefd-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="5aefd-118">Ottenere un puntatore all'interfaccia [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) chiamando **INSSBuffer:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="5aefd-118">Obtain a pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface by calling **INSSBuffer::QueryInterface**.</span></span>
6.  <span data-ttu-id="5aefd-119">Impostare l'esempio come fotogramma chiave forzata chiamando il metodo [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) per impostare la \_ Proprietà WM SampleExtensionGUID \_ OutputCleanPoint.</span><span class="sxs-lookup"><span data-stu-id="5aefd-119">Set the sample as a forced key frame by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the WM\_SampleExtensionGUID\_OutputCleanPoint property.</span></span> <span data-ttu-id="5aefd-120">Questa proprietà è un valore booleano. impostarla su **true**.</span><span class="sxs-lookup"><span data-stu-id="5aefd-120">This property is a Boolean value; set it to **TRUE**.</span></span>
7.  <span data-ttu-id="5aefd-121">Passare l'interfaccia del buffer al writer insieme al numero di input e all'ora del campione usando il metodo [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="5aefd-121">Pass the buffer interface to the writer along with the input number and sample time by using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aefd-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5aefd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aefd-123">**IWMWriter::WriteSample**</span><span class="sxs-lookup"><span data-stu-id="5aefd-123">**IWMWriter::WriteSample**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[<span data-ttu-id="5aefd-124">**Per scrivere esempi**</span><span class="sxs-lookup"><span data-stu-id="5aefd-124">**To Write Samples**</span></span>](to-write-samples.md)
</dt> <dt>

[<span data-ttu-id="5aefd-125">**Codifica della velocità in bit variabile (VBR)**</span><span class="sxs-lookup"><span data-stu-id="5aefd-125">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="5aefd-126">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="5aefd-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




