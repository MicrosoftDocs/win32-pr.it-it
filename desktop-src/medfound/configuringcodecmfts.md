---
description: Configurazione del codec MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Configurazione del codec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484100"
---
# <a name="configuring-codec-mfts"></a><span data-ttu-id="fb8de-103">Configurazione del codec MFTs</span><span class="sxs-lookup"><span data-stu-id="fb8de-103">Configuring Codec MFTs</span></span>

<span data-ttu-id="fb8de-104">Questo argomento descrive il processo di configurazione del codec MFTs.</span><span class="sxs-lookup"><span data-stu-id="fb8de-104">This topic describes the process of configuring the codec MFTs.</span></span> <span data-ttu-id="fb8de-105">Ogni codec ha procedure specifiche, ma le informazioni comuni a tutte sono descritte qui.</span><span class="sxs-lookup"><span data-stu-id="fb8de-105">Each codec has specific procedures, but the information common to all is described here.</span></span>

## <a name="configuring-mft-inputs-and-outputs"></a><span data-ttu-id="fb8de-106">Configurazione degli input e degli output di MFT</span><span class="sxs-lookup"><span data-stu-id="fb8de-106">Configuring MFT Inputs and Outputs</span></span>

<span data-ttu-id="fb8de-107">Ogni MFT supporta tipi di input e output specifici.</span><span class="sxs-lookup"><span data-stu-id="fb8de-107">Every MFT supports specific input and output types.</span></span> <span data-ttu-id="fb8de-108">È possibile recuperare i tipi di input supportati chiamando ripetutamente [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementando l'indice del tipo con ogni chiamata.</span><span class="sxs-lookup"><span data-stu-id="fb8de-108">You can retrieve supported input types by repeatedly calling [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementing the type index with each call.</span></span> <span data-ttu-id="fb8de-109">Quando si trova un tipo appropriato, impostare il tipo di input chiamando [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="fb8de-109">When you find an appropriate type, set the input type by calling [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span> <span data-ttu-id="fb8de-110">È quindi possibile ripetere il processo per il tipo di output usando le chiamate a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) e [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="fb8de-110">You can then repeat the process for the output type using the calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) and [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="fb8de-111">È necessario eseguire una query o impostare i tipi di output disponibili solo dopo aver impostato il tipo di input.</span><span class="sxs-lookup"><span data-stu-id="fb8de-111">You must query or set the available output types only after setting the input type.</span></span>

## <a name="configuring-the-codec-mfts-for-encoding"></a><span data-ttu-id="fb8de-112">Configurazione del codec MFTs per la codifica</span><span class="sxs-lookup"><span data-stu-id="fb8de-112">Configuring the Codec MFTs for Encoding</span></span>

<span data-ttu-id="fb8de-113">Tutti i codec Windows Media Audio e video supportano un'ampia gamma di funzionalità di codifica.</span><span class="sxs-lookup"><span data-stu-id="fb8de-113">All of the Windows Media Audio and Video codecs support a variety of encoding features.</span></span> <span data-ttu-id="fb8de-114">Queste funzionalità vengono in genere configurate impostando le proprietà in MFT usando i metodi dell'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="fb8de-114">These features are generally configured by setting properties on the MFT by using the methods of the **IPropertyStore** interface.</span></span> <span data-ttu-id="fb8de-115">Alcune proprietà vengono configurate utilizzando interfacce di codec specializzate.</span><span class="sxs-lookup"><span data-stu-id="fb8de-115">Some properties are configured using specialized codec interfaces.</span></span> <span data-ttu-id="fb8de-116">Queste interfacce sono elencate per ogni codec nella sezione [oggetti codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="fb8de-116">These interfaces are listed for each codec in the section [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="fb8de-117">L'ordine generale delle operazioni per la configurazione di un MFT di codifica è il seguente:</span><span class="sxs-lookup"><span data-stu-id="fb8de-117">The general order of operations for configuring an encoding MFT is as follows:</span></span>

1.  <span data-ttu-id="fb8de-118">Configurare le funzionalità di codec come desiderato usando i metodi di **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="fb8de-118">Configure codec features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="fb8de-119">Usare le interfacce del codec MFT per configurare le funzionalità aggiuntive, se necessario.</span><span class="sxs-lookup"><span data-stu-id="fb8de-119">Use the codec MFT interfaces to configure additional features, if needed.</span></span>
3.  <span data-ttu-id="fb8de-120">Configurare i tipi di input e di output.</span><span class="sxs-lookup"><span data-stu-id="fb8de-120">Configure the input and output types.</span></span> <span data-ttu-id="fb8de-121">L'ordine in cui devono essere configurati i tipi varia per i singoli codec.</span><span class="sxs-lookup"><span data-stu-id="fb8de-121">The order in which the types should be configured varies for individual codecs.</span></span> <span data-ttu-id="fb8de-122">Per ulteriori informazioni, vedere [utilizzo di audio](workingwithaudio.md) e [utilizzo di video](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="fb8de-122">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

## <a name="configuring-the-codec-mfts-for-decoding"></a><span data-ttu-id="fb8de-123">Configurazione del codec MFTs per la decodifica</span><span class="sxs-lookup"><span data-stu-id="fb8de-123">Configuring the Codec MFTs for Decoding</span></span>

<span data-ttu-id="fb8de-124">La decodifica è più semplice della codifica, in quanto sono supportate meno funzionalità di decodificatore.</span><span class="sxs-lookup"><span data-stu-id="fb8de-124">Decoding is simpler than encoding, as fewer decoder features are supported.</span></span>

<span data-ttu-id="fb8de-125">L'ordine generale delle operazioni per la configurazione di un MFT di decodifica è il seguente:</span><span class="sxs-lookup"><span data-stu-id="fb8de-125">The general order of operations for configuring a decoding MFT is as follows:</span></span>

1.  <span data-ttu-id="fb8de-126">Configurare le funzionalità del decodificatore in base alle esigenze usando i metodi di **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="fb8de-126">Configure decoder features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="fb8de-127">Impostare il tipo di input sul tipo usato per l'output del codificatore.</span><span class="sxs-lookup"><span data-stu-id="fb8de-127">Set the input type to the type used for the encoder output.</span></span>
3.  <span data-ttu-id="fb8de-128">Configurare il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="fb8de-128">Configure the output type.</span></span> <span data-ttu-id="fb8de-129">I tipi di output supportati sono diversi per gli input diversi.</span><span class="sxs-lookup"><span data-stu-id="fb8de-129">The supported output types are different for different inputs.</span></span>

> [!Note]  
> <span data-ttu-id="fb8de-130">È importante usare lo stesso tipo di supporto per l'input del decodificatore usato per l'output del codificatore.</span><span class="sxs-lookup"><span data-stu-id="fb8de-130">It is important to use the same media type for the decoder input as was used for the encoder output.</span></span> <span data-ttu-id="fb8de-131">Ciò è dovuto al fatto che i codec Windows Media Audio e video usano formati multimediali con dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="fb8de-131">This is because the Windows Media Audio and Video codecs use media formats with extra data.</span></span> <span data-ttu-id="fb8de-132">Senza i dati di formato esteso, non è possibile decodificare il contenuto compresso.</span><span class="sxs-lookup"><span data-stu-id="fb8de-132">Without the extended format data, you cannot decode the compressed content.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fb8de-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb8de-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb8de-134">Uso di codec MFTs</span><span class="sxs-lookup"><span data-stu-id="fb8de-134">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



