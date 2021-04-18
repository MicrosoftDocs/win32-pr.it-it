---
description: La classe CImageSample implementa un esempio di supporto che gestisce una bitmap (DIB) indipendente dal dispositivo GDI.
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: Classe CImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2235d50c952ce1b76e4a70eda0341f0fe3c4167c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325047"
---
# <a name="cimagesample-class"></a><span data-ttu-id="e3e91-103">Classe CImageSample</span><span class="sxs-lookup"><span data-stu-id="e3e91-103">CImageSample class</span></span>

![gerarchia di classi cimagesample](images/wutil03.png)

<span data-ttu-id="e3e91-105">La `CImageSample` classe implementa un esempio di supporto che gestisce una bitmap (DIB) indipendente dal dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="e3e91-105">The `CImageSample` class implements a media sample that manages a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="e3e91-106">Questa classe deriva dalla classe [**CMediaSample**](cmediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="e3e91-106">This class derives from the [**CMediaSample**](cmediasample.md) class.</span></span> <span data-ttu-id="e3e91-107">È progettato per essere usato con la classe [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="e3e91-107">It is intended to be used with the [**CImageAllocator**](cimageallocator.md) class.</span></span> <span data-ttu-id="e3e91-108">La classe **CImageAllocator** fornisce un allocatore che crea `CImageSample` oggetti.</span><span class="sxs-lookup"><span data-stu-id="e3e91-108">The **CImageAllocator** class provides an allocator that creates `CImageSample` objects.</span></span>



| <span data-ttu-id="e3e91-109">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="e3e91-109">Protected Member Variables</span></span>                        | <span data-ttu-id="e3e91-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3e91-110">Description</span></span>                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="e3e91-111">**\_DibData m**</span><span class="sxs-lookup"><span data-stu-id="e3e91-111">**m\_DibData**</span></span>](cimagesample-m-dibdata.md)      | <span data-ttu-id="e3e91-112">Contiene informazioni sulla DIB gestita da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e3e91-112">Contains information about the DIB that this object is managing.</span></span>  |
| [<span data-ttu-id="e3e91-113">**m \_ Binit**</span><span class="sxs-lookup"><span data-stu-id="e3e91-113">**m\_bInit**</span></span>](cimagesample-m-binit.md)          | <span data-ttu-id="e3e91-114">Indica se l'oggetto è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="e3e91-114">Indicates whether the object has been initialized.</span></span>                |
| <span data-ttu-id="e3e91-115">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="e3e91-115">Public Methods</span></span>                                    | <span data-ttu-id="e3e91-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3e91-116">Description</span></span>                                                       |
| [<span data-ttu-id="e3e91-117">**CImageSample**</span><span class="sxs-lookup"><span data-stu-id="e3e91-117">**CImageSample**</span></span>](cimagesample-cimagesample.md) | <span data-ttu-id="e3e91-118">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="e3e91-118">Constructor method.</span></span>                                               |
| [<span data-ttu-id="e3e91-119">**GetDIBData**</span><span class="sxs-lookup"><span data-stu-id="e3e91-119">**GetDIBData**</span></span>](cimagesample-getdibdata.md)     | <span data-ttu-id="e3e91-120">Recupera le informazioni relative alla DIB gestita da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e3e91-120">Retrieves information about the DIB that this object is managing.</span></span> |
| [<span data-ttu-id="e3e91-121">**SetDIBData**</span><span class="sxs-lookup"><span data-stu-id="e3e91-121">**SetDIBData**</span></span>](cimagesample-setdibdata.md)     | <span data-ttu-id="e3e91-122">Imposta le informazioni sulla DIB gestite da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e3e91-122">Sets information about the DIB that this object is managing.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="e3e91-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3e91-123">Requirements</span></span>



| <span data-ttu-id="e3e91-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3e91-124">Requirement</span></span> | <span data-ttu-id="e3e91-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e3e91-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e91-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3e91-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e3e91-127"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3e91-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3e91-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3e91-128">Library</span></span><br/> | <dl> <span data-ttu-id="e3e91-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e3e91-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




