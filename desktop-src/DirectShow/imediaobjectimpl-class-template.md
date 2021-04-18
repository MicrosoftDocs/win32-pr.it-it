---
description: Il modello di classe IMediaObjectImpl fornisce un'implementazione di base per l'interfaccia IMediaObject. Per ulteriori informazioni sull'utilizzo di questo modello, vedere Utilizzo del modello di classe DMO.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Modello di classe IMediaObjectImpl (Dmoimpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330398"
---
# <a name="imediaobjectimpl-class-template"></a><span data-ttu-id="eaf8a-104">Modello di classe IMediaObjectImpl</span><span class="sxs-lookup"><span data-stu-id="eaf8a-104">IMediaObjectImpl Class Template</span></span>

<span data-ttu-id="eaf8a-105">Il `IMediaObjectImpl` modello di classe fornisce un'implementazione di base per l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="eaf8a-105">The `IMediaObjectImpl` class template provides a base implementation for the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="eaf8a-106">Per ulteriori informazioni sull'utilizzo di questo modello, vedere [utilizzo del modello di classe DMO](using-the-dmo-class-template.md).</span><span class="sxs-lookup"><span data-stu-id="eaf8a-106">For more information on using this template, see [Using the DMO Class Template](using-the-dmo-class-template.md).</span></span>

<span data-ttu-id="eaf8a-107">Questo `IMediaObjectImpl` modello espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-107">This `IMediaObjectImpl` template exposes the following members.</span></span>



| <span data-ttu-id="eaf8a-108">Classe annidata</span><span class="sxs-lookup"><span data-stu-id="eaf8a-108">Nested Class</span></span>                              | <span data-ttu-id="eaf8a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eaf8a-109">Description</span></span>                                  |
|-------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="eaf8a-110">**LockIt**</span><span class="sxs-lookup"><span data-stu-id="eaf8a-110">**LockIt**</span></span>](imediaobjectimpl-lockit.md) | <span data-ttu-id="eaf8a-111">Classe helper che blocca e sblocca il DMO.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-111">Helper class that locks and unlocks the DMO.</span></span> |



 



| <span data-ttu-id="eaf8a-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="eaf8a-112">Method</span></span>                                                                      | <span data-ttu-id="eaf8a-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eaf8a-113">Description</span></span>                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="eaf8a-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="eaf8a-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span></span>                     | <span data-ttu-id="eaf8a-115">Determina se tutti i flussi non facoltativi hanno tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-115">Determines whether all of the non-optional streams have media types.</span></span> |
| <span data-ttu-id="eaf8a-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="eaf8a-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span></span>                             | <span data-ttu-id="eaf8a-117">Recupera il tipo di supporto corrente per un flusso di input specificato.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-117">Retrieves the current media type for a specified input stream.</span></span>       |
| <span data-ttu-id="eaf8a-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="eaf8a-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span></span>                       | <span data-ttu-id="eaf8a-119">Esegue una query per determinare se il tipo di supporto è stato impostato su un flusso di input.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-119">Queries whether the media type was set on an input stream.</span></span>           |
| <span data-ttu-id="eaf8a-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="eaf8a-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span></span>   | <span data-ttu-id="eaf8a-121">Esegue una query per determinare se un flusso di input può accettare più input.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-121">Queries whether an input stream can accept more input.</span></span>               |
| <span data-ttu-id="eaf8a-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="eaf8a-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span></span>   | <span data-ttu-id="eaf8a-123">Esegue una query per determinare se un flusso di input può accettare un determinato tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-123">Queries whether an input stream can accept a given media type.</span></span>       |
| <span data-ttu-id="eaf8a-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="eaf8a-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span></span> | <span data-ttu-id="eaf8a-125">Esegue una query per determinare se un flusso di output può accettare un determinato tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-125">Queries whether an output stream can accept a given media type.</span></span>      |
| <span data-ttu-id="eaf8a-126">[**Lock**](/previous-versions/ms809100(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="eaf8a-126">[**Lock**](/previous-versions/ms809100(v=msdn.10))</span></span>                                       | <span data-ttu-id="eaf8a-127">Blocca DMO</span><span class="sxs-lookup"><span data-stu-id="eaf8a-127">Locks the DMO</span></span>                                                        |
| <span data-ttu-id="eaf8a-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="eaf8a-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span></span>                           | <span data-ttu-id="eaf8a-129">Recupera il tipo di supporto corrente per un flusso di output specificato.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-129">Retrieves the current media type for a specified output stream.</span></span>      |
| <span data-ttu-id="eaf8a-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="eaf8a-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span></span>                     | <span data-ttu-id="eaf8a-131">Esegue una query per determinare se il tipo di supporto è stato impostato su un flusso di output.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-131">Queries whether the media type was set on an output stream.</span></span>          |
| <span data-ttu-id="eaf8a-132">[**Sblocca**](/previous-versions/ms809101(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="eaf8a-132">[**Unlock**](/previous-versions/ms809101(v=msdn.10))</span></span>                                   | <span data-ttu-id="eaf8a-133">Sblocca DMO</span><span class="sxs-lookup"><span data-stu-id="eaf8a-133">Unlocks the DMO</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="eaf8a-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eaf8a-134">Requirements</span></span>



| <span data-ttu-id="eaf8a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaf8a-135">Requirement</span></span> | <span data-ttu-id="eaf8a-136">Valore</span><span class="sxs-lookup"><span data-stu-id="eaf8a-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf8a-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eaf8a-137">Header</span></span><br/>  | <dl> <span data-ttu-id="eaf8a-138"><dt>Dmoimpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaf8a-138"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="eaf8a-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="eaf8a-139">Library</span></span><br/> | <dl> <span data-ttu-id="eaf8a-140"><dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eaf8a-140"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf8a-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eaf8a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf8a-142">Guida di riferimento a DMO</span><span class="sxs-lookup"><span data-stu-id="eaf8a-142">DMO Reference</span></span>](dmo-reference.md)
</dt> <dt>

[<span data-ttu-id="eaf8a-143">Uso del modello di classe DMO</span><span class="sxs-lookup"><span data-stu-id="eaf8a-143">Using the DMO Class Template</span></span>](using-the-dmo-class-template.md)
</dt> </dl>

 

 
