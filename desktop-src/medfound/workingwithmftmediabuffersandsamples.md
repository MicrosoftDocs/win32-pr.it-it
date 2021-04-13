---
description: Uso di buffer e esempi di supporti MFT
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Uso di buffer e esempi di supporti MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6373f6d75b4122409b54649eed6f90e95c2f50c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351336"
---
# <a name="working-with-mft-media-buffers-and-samples"></a><span data-ttu-id="60456-103">Uso di buffer e esempi di supporti MFT</span><span class="sxs-lookup"><span data-stu-id="60456-103">Working with MFT Media Buffers and Samples</span></span>

<span data-ttu-id="60456-104">Il codec MFTs passa i dati multimediali avanti e indietro usando buffer e esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="60456-104">Codec MFTs pass media data back and forth by using media buffers and samples.</span></span>

<span data-ttu-id="60456-105">Un buffer multimediale è un oggetto COM che gestisce un blocco di memoria, in genere per memorizzare i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="60456-105">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="60456-106">Quando i dati vengono passati a o da un MFT, vengono sempre passati sotto forma di buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="60456-106">When data is passed to or from an MFT, it is always passed in the form of a media buffer.</span></span>

<span data-ttu-id="60456-107">Tutti i buffer multimediali espongono l'interfaccia **IMFMediaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="60456-107">All media buffers expose the **IMFMediaBuffer** interface.</span></span> <span data-ttu-id="60456-108">Questa interfaccia è progettata per qualsiasi tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="60456-108">This interface is designed for any type of data.</span></span> <span data-ttu-id="60456-109">I buffer contenenti dati video spesso espongono anche **IMF2DBuffer**.</span><span class="sxs-lookup"><span data-stu-id="60456-109">Buffers containing video data often also expose **IMF2DBuffer**.</span></span>

<span data-ttu-id="60456-110">Un buffer multimediale ha una dimensione massima, ovvero la quantità di memoria allocata per il buffer.</span><span class="sxs-lookup"><span data-stu-id="60456-110">A media buffer has a maximum size, which is the amount of memory allocated for the buffer.</span></span> <span data-ttu-id="60456-111">Per trovare le dimensioni massime, chiamare **IMFMediaBuffer:: GetMaxLength**.</span><span class="sxs-lookup"><span data-stu-id="60456-111">To find the maximum size, call **IMFMediaBuffer::GetMaxLength**.</span></span> <span data-ttu-id="60456-112">In qualsiasi momento, un buffer multimediale dispone anche di una lunghezza corrente, ovvero la quantità di dati validi nel buffer, che va da zero byte fino alla dimensione massima.</span><span class="sxs-lookup"><span data-stu-id="60456-112">At any point in time, a media buffer also has a current length, which is the amount of valid data in the buffer, ranging from zero bytes up to the maximum size.</span></span> <span data-ttu-id="60456-113">Per ottenere la lunghezza corrente, chiamare **IMFMediaBuffer:: GetCurrentLength**.</span><span class="sxs-lookup"><span data-stu-id="60456-113">To get the current length, call **IMFMediaBuffer::GetCurrentLength**.</span></span> <span data-ttu-id="60456-114">Quando viene creato il buffer, la lunghezza corrente è zero.</span><span class="sxs-lookup"><span data-stu-id="60456-114">When the buffer is created, the current length is zero.</span></span> <span data-ttu-id="60456-115">Se si scrivono dati nel buffer, chiamare **IMFMediaBuffer:: SetCurrentLength** per aggiornare la lunghezza corrente.</span><span class="sxs-lookup"><span data-stu-id="60456-115">If you write data to the buffer, call **IMFMediaBuffer::SetCurrentLength** to update the current length.</span></span>

<span data-ttu-id="60456-116">Per accedere alla memoria nel buffer, chiamare **IMFMediaBuffer:: Lock**.</span><span class="sxs-lookup"><span data-stu-id="60456-116">To access the memory in the buffer, call **IMFMediaBuffer::Lock**.</span></span> <span data-ttu-id="60456-117">Questo metodo restituisce un puntatore all'inizio del blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="60456-117">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="60456-118">Al termine dell'utilizzo del puntatore, chiamare **IMFMediaBuffer:: Unlock**.</span><span class="sxs-lookup"><span data-stu-id="60456-118">When you are done using the pointer, call **IMFMediaBuffer::Unlock**.</span></span> <span data-ttu-id="60456-119">Il metodo **Lock** non è un meccanismo di sincronizzazione dei thread. non garantisce che altri thread non possano accedere al buffer.</span><span class="sxs-lookup"><span data-stu-id="60456-119">The **Lock** method is not a thread synchronization mechanism; it does not guarantee that other threads cannot access the buffer.</span></span> <span data-ttu-id="60456-120">Il metodo **Lock** viene usato per garantire che la memoria a cui si accede rimarrà valida fino a quando non si chiama il metodo **Unlock** .</span><span class="sxs-lookup"><span data-stu-id="60456-120">The **Lock** method is used to assure that the memory accessed will remain valid until you call the **Unlock** method.</span></span>

<span data-ttu-id="60456-121">Un oggetto di esempio multimediale (nel contesto di Media Foundation SDK) è un oggetto che contiene un elenco ordinato di zero o più buffer.</span><span class="sxs-lookup"><span data-stu-id="60456-121">A media sample object (in the context of the Media Foundation SDK) is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="60456-122">Gli esempi di supporti espongono l'interfaccia **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="60456-122">Media samples expose the **IMFSample** interface.</span></span>

<span data-ttu-id="60456-123">Per creare un nuovo esempio, chiamare la funzione **MFCreateSample** .</span><span class="sxs-lookup"><span data-stu-id="60456-123">To create a new sample, call the **MFCreateSample** function.</span></span> <span data-ttu-id="60456-124">Inizialmente, l'elenco di buffer dell'esempio è vuoto.</span><span class="sxs-lookup"><span data-stu-id="60456-124">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="60456-125">Per aggiungere un buffer alla fine dell'elenco, chiamare **IMFSample:: AddBuffer**.</span><span class="sxs-lookup"><span data-stu-id="60456-125">To add a buffer to the end of the list, call **IMFSample::AddBuffer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60456-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60456-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60456-127">Uso di codec DMOs</span><span class="sxs-lookup"><span data-stu-id="60456-127">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> <dt>

[<span data-ttu-id="60456-128">Uso di codec MFTs</span><span class="sxs-lookup"><span data-stu-id="60456-128">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



