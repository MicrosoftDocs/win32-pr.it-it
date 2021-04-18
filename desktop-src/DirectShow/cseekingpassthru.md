---
description: La classe CSeekingPassThru è un oggetto helper che crea oggetti CPosPassThru e CRendererPosPassThru.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: Classe CSeekingPassThru (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324663"
---
# <a name="cseekingpassthru-class"></a><span data-ttu-id="533d5-103">Classe CSeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="533d5-103">CSeekingPassThru class</span></span>

<span data-ttu-id="533d5-104">La `CSeekingPassThru` classe è un oggetto helper che crea oggetti [**CPosPassThru**](cpospassthru.md) e [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="533d5-104">The `CSeekingPassThru` class is a helper object that creates [**CPosPassThru**](cpospassthru.md) and [**CRendererPosPassThru**](crendererpospassthru.md) objects.</span></span>

<span data-ttu-id="533d5-105">Le classi **CPosPassThru** e **CRendererPosPassThru** sono oggetti helper che passano i comandi di ricerca upstream, quindi la `CSeekingPassThru` classe è un oggetto helper per la creazione di oggetti helper.</span><span class="sxs-lookup"><span data-stu-id="533d5-105">The **CPosPassThru** and **CRendererPosPassThru** classes are helper objects that pass seeking commands upstream, so the `CSeekingPassThru` class is a helper object for creating helper objects.</span></span>

<span data-ttu-id="533d5-106">Non è necessario usare direttamente questa classe.</span><span class="sxs-lookup"><span data-stu-id="533d5-106">It is not necessary to use this class directly.</span></span> <span data-ttu-id="533d5-107">Usare invece la funzione [**CreatePosPassThru**](createpospassthru.md) , che gestisce tutti i dettagli dell'uso di questa classe.</span><span class="sxs-lookup"><span data-stu-id="533d5-107">Instead, use the [**CreatePosPassThru**](createpospassthru.md) function, which handles all of the details of using this class.</span></span> <span data-ttu-id="533d5-108">Offre l'ulteriore vantaggio di caricare l'oggetto da Quartz.dll, riducendo in qualche modo le dimensioni del codice del filtro.</span><span class="sxs-lookup"><span data-stu-id="533d5-108">It has the further advantage of loading the object from Quartz.dll, which reduces the code size of your filter somewhat.</span></span> <span data-ttu-id="533d5-109">Per ulteriori informazioni, vedere [**CPosPassThru**](cpospassthru.md).</span><span class="sxs-lookup"><span data-stu-id="533d5-109">For more information, see [**CPosPassThru**](cpospassthru.md).</span></span>

<span data-ttu-id="533d5-110">La `CSeekingPassThru` classe espone l'interfaccia [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) .</span><span class="sxs-lookup"><span data-stu-id="533d5-110">The `CSeekingPassThru` class exposes the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface.</span></span> <span data-ttu-id="533d5-111">Il metodo [**ISeekingPassThru:: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) Inizializza l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="533d5-111">The [**ISeekingPassThru::Init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) method initializes the object.</span></span> <span data-ttu-id="533d5-112">Dopo che l'oggetto è stato inizializzato, il filtro può eseguire una query per le interfacce [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) e [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .</span><span class="sxs-lookup"><span data-stu-id="533d5-112">After the object is initialized, the filter can query it for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interfaces.</span></span>



| <span data-ttu-id="533d5-113">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="533d5-113">Public Methods</span></span>                                                  | <span data-ttu-id="533d5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="533d5-114">Description</span></span>                        |
|-----------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="533d5-115">**CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="533d5-115">**CSeekingPassThru**</span></span>](cseekingpassthru-cseekingpassthru.md)   | <span data-ttu-id="533d5-116">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="533d5-116">Constructor method.</span></span>                |
| [<span data-ttu-id="533d5-117">**~ CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="533d5-117">**~CSeekingPassThru**</span></span>](cseekingpassthru--cseekingpassthru.md) | <span data-ttu-id="533d5-118">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="533d5-118">Destructor method.</span></span>                 |
| [<span data-ttu-id="533d5-119">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="533d5-119">**CreateInstance**</span></span>](cseekingpassthru-createinstance.md)       | <span data-ttu-id="533d5-120">Crea un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="533d5-120">Creates an instance of the object.</span></span> |
| <span data-ttu-id="533d5-121">Metodi ISeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="533d5-121">ISeekingPassThru Methods</span></span>                                        | <span data-ttu-id="533d5-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="533d5-122">Description</span></span>                        |
| [<span data-ttu-id="533d5-123">**Init**</span><span class="sxs-lookup"><span data-stu-id="533d5-123">**Init**</span></span>](cseekingpassthru-init.md)                           | <span data-ttu-id="533d5-124">Inizializza l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="533d5-124">Initializes the object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="533d5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="533d5-125">Requirements</span></span>



| <span data-ttu-id="533d5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="533d5-126">Requirement</span></span> | <span data-ttu-id="533d5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="533d5-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="533d5-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="533d5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="533d5-129"><dt>Seekpt. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="533d5-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="533d5-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="533d5-130">Library</span></span><br/> | <dl> <span data-ttu-id="533d5-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="533d5-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




