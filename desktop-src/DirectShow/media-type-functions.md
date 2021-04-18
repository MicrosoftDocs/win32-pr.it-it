---
description: Le classi base di DirectShow forniscono funzioni di supporto per la gestione della \_ struttura del tipo di supporto am \_ .
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Funzioni di tipo supporto (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323999"
---
# <a name="media-type-functions"></a><span data-ttu-id="7af6b-103">Funzioni di tipo multimediale</span><span class="sxs-lookup"><span data-stu-id="7af6b-103">Media Type Functions</span></span>

<span data-ttu-id="7af6b-104">Le classi base di DirectShow forniscono funzioni di supporto per la gestione della struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="7af6b-104">The DirectShow base classes provides helper functions for handling the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="7af6b-105">La struttura del **\_ \_ tipo di supporto am** contiene un puntatore (membro **pbFormat** ) a un altro blocco di memoria, denominato *blocco di formato*.</span><span class="sxs-lookup"><span data-stu-id="7af6b-105">The **AM\_MEDIA\_TYPE** structure contains a pointer (the **pbFormat** member) to another block of memory, which is called the *format block*.</span></span> <span data-ttu-id="7af6b-106">Quando si lavora con questa struttura, è necessario prestare attenzione all'allocazione di memoria per evitare perdite di memoria.</span><span class="sxs-lookup"><span data-stu-id="7af6b-106">When you work with this structure, therefore, you must be careful about memory allocation in order to avoid memory leaks.</span></span>

<span data-ttu-id="7af6b-107">Le funzioni seguenti allocano memoria:</span><span class="sxs-lookup"><span data-stu-id="7af6b-107">The following functions allocate memory:</span></span>

-   <span data-ttu-id="7af6b-108">**CreateMediaType** alloca una nuova struttura **del \_ \_ tipo di supporto am** e il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="7af6b-108">**CreateMediaType** allocates a new **AM\_MEDIA\_TYPE** structure and the format block.</span></span>
-   <span data-ttu-id="7af6b-109">**CopyMediaType** copia in una struttura **del \_ \_ tipo di supporto am** esistente, ma alloca il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="7af6b-109">**CopyMediaType** copies to an existing **AM\_MEDIA\_TYPE** structure, but allocates the format block.</span></span>
-   <span data-ttu-id="7af6b-110">**CreateAudioMediaType** Inizializza una struttura **del \_ \_ tipo di supporto am** esistente e, facoltativamente, alloca il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="7af6b-110">**CreateAudioMediaType** initializes an existing **AM\_MEDIA\_TYPE** structure, and optionally allocates the format block.</span></span>

<span data-ttu-id="7af6b-111">Le funzioni seguenti liberano memoria:</span><span class="sxs-lookup"><span data-stu-id="7af6b-111">The following functions free memory:</span></span>

-   <span data-ttu-id="7af6b-112">**FreeMediaType** rilascia il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="7af6b-112">**FreeMediaType** releases the format block.</span></span>
-   <span data-ttu-id="7af6b-113">**DeleteMediaType** libera una struttura **del \_ \_ tipo di supporto am** , incluso il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="7af6b-113">**DeleteMediaType** frees an **AM\_MEDIA\_TYPE** structure, including the format block.</span></span>



| <span data-ttu-id="7af6b-114">Funzione</span><span class="sxs-lookup"><span data-stu-id="7af6b-114">Function</span></span>                                             | <span data-ttu-id="7af6b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7af6b-115">Description</span></span>                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7af6b-116">**CopyMediaType**</span><span class="sxs-lookup"><span data-stu-id="7af6b-116">**CopyMediaType**</span></span>](copymediatype.md)               | <span data-ttu-id="7af6b-117">Copia una struttura del **tipo di \_ supporto \_ am** allocato per le attività.</span><span class="sxs-lookup"><span data-stu-id="7af6b-117">Copies a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                      |
| [<span data-ttu-id="7af6b-118">**CreateAudioMediaType**</span><span class="sxs-lookup"><span data-stu-id="7af6b-118">**CreateAudioMediaType**</span></span>](createaudiomediatype.md) | <span data-ttu-id="7af6b-119">Inizializza una struttura del tipo di supporto data una struttura del formato Wave.</span><span class="sxs-lookup"><span data-stu-id="7af6b-119">Initializes a media type structure given a wave format structure.</span></span>                                           |
| [<span data-ttu-id="7af6b-120">**CreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="7af6b-120">**CreateMediaType**</span></span>](createmediatype.md)           | <span data-ttu-id="7af6b-121">Alloca e Inizializza una struttura **del \_ \_ tipo di supporto am** da una struttura del **\_ \_ tipo di supporto am** esistente.</span><span class="sxs-lookup"><span data-stu-id="7af6b-121">Allocates and initializes an **AM\_MEDIA\_TYPE** structure, from an existing **AM\_MEDIA\_TYPE** structure.</span></span> |
| [<span data-ttu-id="7af6b-122">**DeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="7af6b-122">**DeleteMediaType**</span></span>](deletemediatype.md)           | <span data-ttu-id="7af6b-123">Elimina una struttura del **tipo di \_ supporto \_ am** allocato per le attività.</span><span class="sxs-lookup"><span data-stu-id="7af6b-123">Deletes a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                     |
| [<span data-ttu-id="7af6b-124">**FreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="7af6b-124">**FreeMediaType**</span></span>](freemediatype.md)               | <span data-ttu-id="7af6b-125">Libera una struttura del **\_ \_ tipo di supporto am** allocata per le attività dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="7af6b-125">Frees a task-allocated **AM\_MEDIA\_TYPE** structure from memory.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="7af6b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7af6b-126">Requirements</span></span>



| <span data-ttu-id="7af6b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7af6b-127">Requirement</span></span> | <span data-ttu-id="7af6b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="7af6b-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7af6b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7af6b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7af6b-130"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7af6b-130"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="7af6b-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="7af6b-131">Library</span></span><br/> | <dl> <span data-ttu-id="7af6b-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7af6b-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




