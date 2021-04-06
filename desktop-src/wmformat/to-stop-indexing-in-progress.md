---
title: Per arrestare l'indicizzazione in corso
description: Per arrestare l'indicizzazione in corso
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows Media Format SDK, arresto dell'indicizzazione in corso
- ASF (Advanced Systems Format), arresto dell'indicizzazione in corso
- ASF (formato avanzato dei sistemi), arresto dell'indicizzazione in corso
- indici, arresto dell'indicizzazione in corso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046330"
---
# <a name="to-stop-indexing-in-progress"></a><span data-ttu-id="73495-107">Per arrestare l'indicizzazione in corso</span><span class="sxs-lookup"><span data-stu-id="73495-107">To Stop Indexing in Progress</span></span>

<span data-ttu-id="73495-108">Dopo l'avvio dell'indicizzazione con una chiamata a [**IWMIndexer:: startindexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), l'indicizzatore continuerà a continuare fino a quando il file non sarà indicizzato.</span><span class="sxs-lookup"><span data-stu-id="73495-108">After you begin indexing with a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), the indexer will normally continue until the file is indexed.</span></span> <span data-ttu-id="73495-109">È possibile arrestare le operazioni di indicizzazione chiamando il metodo [**IWMIndexer:: Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) .</span><span class="sxs-lookup"><span data-stu-id="73495-109">You can stop indexing operations by calling the [**IWMIndexer::Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) method.</span></span> <span data-ttu-id="73495-110">Dopo aver annullato l'indicizzazione, è possibile chiamare di nuovo la funzione **startIndex** , ma l'indicizzatore inizierà dall'inizio del file anziché riprendere dal punto di annullamento.</span><span class="sxs-lookup"><span data-stu-id="73495-110">After you have canceled indexing, you can call **StartIndexing** again, but the indexer will start from the beginning of the file rather than resuming from the point of cancellation.</span></span>

<span data-ttu-id="73495-111">Poiché la funzione **startIndex** è una chiamata asincrona, in genere è necessario chiamare **Cancel** da un altro thread o gestore eventi nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73495-111">Because **StartIndexing** is an asynchronous call, you will normally need to call **Cancel** from some other thread or event handler in your application.</span></span> <span data-ttu-id="73495-112">In genere l' **annullamento** verrà chiamato da una routine di evento associata a un controllo Button di un'applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="73495-112">Typically **Cancel** will be called from an event procedure associated with a button control of a Windows application.</span></span>

<span data-ttu-id="73495-113">Quando l'indicizzazione viene annullata, l'indicizzatore passa un messaggio di stato WMT \_ chiuso, come se il file fosse stato indicizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="73495-113">When indexing is canceled, the indexer will pass a status message of WMT\_CLOSED, just as if the file had been indexed properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73495-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73495-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73495-115">**Interfaccia IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="73495-115">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="73495-116">**Operazioni con gli indici**</span><span class="sxs-lookup"><span data-stu-id="73495-116">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




