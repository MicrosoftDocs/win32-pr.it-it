---
description: Uso dei buffer multimediali DMO
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Uso dei buffer multimediali DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320544"
---
# <a name="working-with-dmo-media-buffers"></a><span data-ttu-id="2c7b0-103">Uso dei buffer multimediali DMO</span><span class="sxs-lookup"><span data-stu-id="2c7b0-103">Working with DMO Media Buffers</span></span>

<span data-ttu-id="2c7b0-104">I dati di input vengono passati al codec DMOs usando i buffer multimediali.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-104">Input data is passed to the codec DMOs using media buffers.</span></span> <span data-ttu-id="2c7b0-105">Un buffer multimediale è un oggetto che implementa l'interfaccia [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="2c7b0-105">A media buffer is an object that implements the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface.</span></span> <span data-ttu-id="2c7b0-106">È possibile implementare una classe a questo scopo oppure, se si usa Windows Media Format SDK nell'applicazione, è possibile usare gli oggetti buffer definiti in tale SDK.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-106">You can implement a class for this purpose or, if you are using the Windows Media Format SDK in your application, you can use the buffer objects that are defined in that SDK.</span></span>

<span data-ttu-id="2c7b0-107">Se si implementa una classe di buffer personalizzata, prestare attenzione a come viene gestita la memoria del buffer.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-107">If you implement your own buffer class, be careful about how the buffer memory is handled.</span></span> <span data-ttu-id="2c7b0-108">Quando si passa un esempio di input, DMO mantiene un riferimento al buffer fino a quando non viene terminato con l'esempio.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-108">When you pass an input sample, the DMO keeps a reference to the buffer until it is finished with the sample.</span></span> <span data-ttu-id="2c7b0-109">È possibile rilasciare immediatamente il riferimento all'interfaccia [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) , ma non si ha modo di sapere quando il codec non necessita più del riferimento.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-109">You can immediately release your reference to the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface, but you have no way of knowing when the codec no longer needs its reference.</span></span> <span data-ttu-id="2c7b0-110">Per essere certi che la memoria venga liberata quando l'oggetto viene eliminato, è necessario implementare la classe in modo da allocare e liberare la memoria per il buffer internamente.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-110">To be certain that the memory is freed when the object deletes itself, you should implement your class so that it allocates and frees the memory for the buffer internally.</span></span>

<span data-ttu-id="2c7b0-111">Poiché il DMOs mantiene i riferimenti ai buffer per un periodo di tempo sconosciuto, non è una cosa banale usare un pool limitato di buffer.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-111">Because the DMOs keep references to buffers for an unknown period of time, it is not a trivial matter to use a limited pool of buffers.</span></span> <span data-ttu-id="2c7b0-112">La soluzione più semplice consiste nell'allocare un nuovo buffer per ogni esempio, anche se questa operazione non è efficiente.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-112">The simplest solution is to allocate a new buffer for each sample, although doing so is inefficient.</span></span>

<span data-ttu-id="2c7b0-113">Una soluzione migliore consiste nell'implementare un oggetto per gestire un pool di buffer.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-113">A better solution is to implement an object to manage a pool of buffers.</span></span> <span data-ttu-id="2c7b0-114">A tale scopo, scrivere il codice nel metodo di **rilascio** dell'implementazione di [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) che chiama un metodo di gestione buffer (anziché eliminarlo) quando il conteggio dei riferimenti scende a zero.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-114">To do this, write code in the **Release** method of your [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) implementation that calls a method of your buffer manager (instead of deleting itself) when the reference count drops to zero.</span></span> <span data-ttu-id="2c7b0-115">Gestione buffer può quindi gestire un elenco di puntatori agli oggetti buffer allocati.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-115">The buffer manager can then maintain a list of pointers to allocated buffer objects.</span></span> <span data-ttu-id="2c7b0-116">Creare un metodo in Gestione buffer per controllare l'elenco dei buffer liberi e restituire un puntatore in modo che l'applicazione possa accedere ai buffer quando necessario.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-116">Create a method in your buffer manager to check the list of free buffers and return a pointer so that your application can access buffers when needed.</span></span> <span data-ttu-id="2c7b0-117">Questo metodo deve creare nuovi buffer in base alle esigenze e aggiungerli all'elenco.</span><span class="sxs-lookup"><span data-stu-id="2c7b0-117">This method should create new buffers as needed and add them to the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c7b0-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c7b0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c7b0-119">Uso di codec DMOs</span><span class="sxs-lookup"><span data-stu-id="2c7b0-119">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
