---
title: DownloadItem.downloadState
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà downloadState recupera lo stato del download.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- Media Player Windows DownloadItem. downloadState
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd2af2fab2ecb69df5b4695b227631b5be2dd96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333414"
---
# <a name="downloaditemdownloadstate"></a><span data-ttu-id="643fd-106">DownloadItem.downloadState</span><span class="sxs-lookup"><span data-stu-id="643fd-106">DownloadItem.downloadState</span></span>

> [!Note]  
> <span data-ttu-id="643fd-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="643fd-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="643fd-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="643fd-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="643fd-109">La proprietà **downloadState** recupera lo stato del download.</span><span class="sxs-lookup"><span data-stu-id="643fd-109">The **downloadState** property retrieves the state of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="643fd-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="643fd-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a><span data-ttu-id="643fd-111">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="643fd-111">Possible Values</span></span>

<span data-ttu-id="643fd-112">Questa proprietà è un **numero** di sola lettura contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="643fd-112">This property is a read-only **Number** containing one of the following values.</span></span>



| <span data-ttu-id="643fd-113">Valore</span><span class="sxs-lookup"><span data-stu-id="643fd-113">Value</span></span> | <span data-ttu-id="643fd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="643fd-114">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="643fd-115">0</span><span class="sxs-lookup"><span data-stu-id="643fd-115">0</span></span>     | <span data-ttu-id="643fd-116">Download in corso</span><span class="sxs-lookup"><span data-stu-id="643fd-116">Downloading</span></span> |
| <span data-ttu-id="643fd-117">1</span><span class="sxs-lookup"><span data-stu-id="643fd-117">1</span></span>     | <span data-ttu-id="643fd-118">Paused</span><span class="sxs-lookup"><span data-stu-id="643fd-118">Paused</span></span>      |
| <span data-ttu-id="643fd-119">2</span><span class="sxs-lookup"><span data-stu-id="643fd-119">2</span></span>     | <span data-ttu-id="643fd-120">Elaborazione in corso</span><span class="sxs-lookup"><span data-stu-id="643fd-120">Processing</span></span>  |
| <span data-ttu-id="643fd-121">3</span><span class="sxs-lookup"><span data-stu-id="643fd-121">3</span></span>     | <span data-ttu-id="643fd-122">Completato</span><span class="sxs-lookup"><span data-stu-id="643fd-122">Completed</span></span>   |
| <span data-ttu-id="643fd-123">4</span><span class="sxs-lookup"><span data-stu-id="643fd-123">4</span></span>     | <span data-ttu-id="643fd-124">Cancellati</span><span class="sxs-lookup"><span data-stu-id="643fd-124">Canceled</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="643fd-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="643fd-125">Remarks</span></span>

<span data-ttu-id="643fd-126">Gli Stati di download possono essere eseguiti in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="643fd-126">Download states can occur in any order.</span></span> <span data-ttu-id="643fd-127">Non scrivere codice che dipende dall'occorrenza di un particolare stato di download.</span><span class="sxs-lookup"><span data-stu-id="643fd-127">Do not write code that depends on the occurrence of any particular download state.</span></span>

## <a name="requirements"></a><span data-ttu-id="643fd-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="643fd-128">Requirements</span></span>



| <span data-ttu-id="643fd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="643fd-129">Requirement</span></span> | <span data-ttu-id="643fd-130">Valore</span><span class="sxs-lookup"><span data-stu-id="643fd-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="643fd-131">Versione</span><span class="sxs-lookup"><span data-stu-id="643fd-131">Version</span></span><br/> | <span data-ttu-id="643fd-132">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="643fd-132">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="643fd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="643fd-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="643fd-134"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="643fd-134"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="643fd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="643fd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="643fd-136">**Oggetto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="643fd-136">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





