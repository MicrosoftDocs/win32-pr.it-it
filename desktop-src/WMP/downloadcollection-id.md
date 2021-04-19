---
title: DownloadCollection.id
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà ID recupera l'ID della raccolta di download.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- Media Player Windows DownloadCollection.id
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9edcca4f56c485951ca907ae228dfec7a958b308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333419"
---
# <a name="downloadcollectionid"></a><span data-ttu-id="59b3a-106">DownloadCollection.id</span><span class="sxs-lookup"><span data-stu-id="59b3a-106">DownloadCollection.id</span></span>

> [!Note]  
> <span data-ttu-id="59b3a-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="59b3a-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="59b3a-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="59b3a-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="59b3a-109">La proprietà **ID** recupera l'ID della raccolta di download.</span><span class="sxs-lookup"><span data-stu-id="59b3a-109">The **id** property retrieves the ID of the download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b3a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59b3a-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a><span data-ttu-id="59b3a-111">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="59b3a-111">Possible Values</span></span>

<span data-ttu-id="59b3a-112">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="59b3a-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="59b3a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="59b3a-113">Remarks</span></span>

<span data-ttu-id="59b3a-114">Quando Download Manager crea una nuova raccolta di download, assegna alla raccolta un numero ID.</span><span class="sxs-lookup"><span data-stu-id="59b3a-114">When the Download Manager creates a new download collection, it assigns the collection an ID number.</span></span> <span data-ttu-id="59b3a-115">I numeri ID vengono mantenuti tra le sessioni di Windows Media Player e quelle del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="59b3a-115">ID numbers persist between Windows Media Player sessions and operating system sessions.</span></span>

<span data-ttu-id="59b3a-116">I numeri ID non sono univoci.</span><span class="sxs-lookup"><span data-stu-id="59b3a-116">ID numbers are not unique.</span></span> <span data-ttu-id="59b3a-117">Tuttavia, sono disponibili numeri ID sufficienti nel valore a 32 bit che è estremamente improbabile che un numero ID esistente venga sovrascritto da uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="59b3a-117">However, there are enough ID numbers available in the 32-bit value that it is extremely unlikely that an existing ID number will ever be overwritten by a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b3a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59b3a-118">Requirements</span></span>



| <span data-ttu-id="59b3a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b3a-119">Requirement</span></span> | <span data-ttu-id="59b3a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="59b3a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59b3a-121">Versione</span><span class="sxs-lookup"><span data-stu-id="59b3a-121">Version</span></span><br/> | <span data-ttu-id="59b3a-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="59b3a-122">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="59b3a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="59b3a-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="59b3a-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59b3a-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b3a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59b3a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b3a-126">**Download (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="59b3a-126">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





