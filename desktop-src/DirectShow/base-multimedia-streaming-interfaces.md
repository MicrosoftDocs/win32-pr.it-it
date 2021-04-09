---
description: Interfacce di streaming multimediali di base
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Interfacce di streaming multimediali di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968974"
---
# <a name="base-multimedia-streaming-interfaces"></a><span data-ttu-id="318bb-103">Interfacce di streaming multimediali di base</span><span class="sxs-lookup"><span data-stu-id="318bb-103">Base Multimedia Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="318bb-104">Queste API sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="318bb-104">These APIs are deprecated.</span></span> <span data-ttu-id="318bb-105">Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="318bb-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="318bb-106">Le interfacce di streaming multimediali di base forniscono un modo programmatico per accedere ai flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="318bb-106">The base multimedia streaming interfaces provide a programmatic way to access multimedia streams.</span></span> <span data-ttu-id="318bb-107">Tuttavia, l'uso di un'interfaccia di base per accedere a un tipo specifico di dati può limitare la quantità di controllo sui dati, quindi gli sviluppatori di contenuti multimediali devono creare versioni derivate di queste interfacce che offrono un controllo più efficace sulle funzionalità esclusive del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="318bb-107">However, using a base interface to access a specific type of data can limit the amount of control you have over the data, so media developers should create derived versions of these interfaces that provide more powerful control over the unique capabilities of their media type.</span></span>



| <span data-ttu-id="318bb-108">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="318bb-108">Interface</span></span>                                      | <span data-ttu-id="318bb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="318bb-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="318bb-110">**IMultiMediaStream**</span><span class="sxs-lookup"><span data-stu-id="318bb-110">**IMultiMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | <span data-ttu-id="318bb-111">Definisce come accedere all'oggetto flusso multimediale di livello più alto. Questo oggetto contiene e fornisce l'accesso ad altri oggetti del flusso.</span><span class="sxs-lookup"><span data-stu-id="318bb-111">Defines how to access the highest-level multimedia stream object; this object contains and provides access to other stream objects.</span></span> <span data-ttu-id="318bb-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) dispone di metodi che enumerano o recuperano flussi specifici, oltre a controllare la durata totale del flusso e la ricerca all'interno del flusso.</span><span class="sxs-lookup"><span data-stu-id="318bb-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) has methods that enumerate or retrieve specific streams, as well as checking the stream's total time duration and seeking within the stream.</span></span>                                                                                                       |
| [<span data-ttu-id="318bb-113">**IMediaStream**</span><span class="sxs-lookup"><span data-stu-id="318bb-113">**IMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | <span data-ttu-id="318bb-114">Definisce un oggetto flusso generico.</span><span class="sxs-lookup"><span data-stu-id="318bb-114">Defines a generic stream object.</span></span> <span data-ttu-id="318bb-115">Usare i relativi metodi per recuperare un puntatore al flusso, ottenere informazioni sul flusso e creare esempi dai dati del flusso.</span><span class="sxs-lookup"><span data-stu-id="318bb-115">Use its methods to retrieve a pointer to the stream, get information about the stream, and create samples from the stream data.</span></span> <span data-ttu-id="318bb-116">È anche possibile creare esempi di flusso condiviso a cui possono accedere più flussi senza duplicare i dati dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="318bb-116">You can also create shared stream samples, which multiple streams can access without duplicating the sample's data.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="318bb-117">**IStreamSample**</span><span class="sxs-lookup"><span data-stu-id="318bb-117">**IStreamSample**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | <span data-ttu-id="318bb-118">Controlla il comportamento di un esempio di flusso specifico.</span><span class="sxs-lookup"><span data-stu-id="318bb-118">Controls the behavior of a specific stream sample.</span></span> <span data-ttu-id="318bb-119">È possibile recuperare il flusso che ha creato l'esempio, controllare l'ora di inizio e di fine dell'esempio e lo stato di completamento ed eseguire una funzione definita dall'utente nell'esempio stesso (tramite il metodo [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) ).</span><span class="sxs-lookup"><span data-stu-id="318bb-119">You can retrieve the stream that created the sample, check the sample's start and end times and completion status, and perform a user-defined function on the sample itself (through the [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) method).</span></span> <span data-ttu-id="318bb-120">In genere, il metodo Update elabora i dati di esempio in modo appropriato, ad esempio il rendering dei dati video o la riproduzione di dati audio.</span><span class="sxs-lookup"><span data-stu-id="318bb-120">Typically, the Update method processes the sample data in an appropriate manner, such as rendering video data or playing back audio data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="318bb-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="318bb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="318bb-122">Elenco di interfacce di streaming multimediali</span><span class="sxs-lookup"><span data-stu-id="318bb-122">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



