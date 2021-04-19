---
title: DownloadItem. Type
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà Type recupera il tipo di download.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem. Type Media Player Windows
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cdcf21ce7443d7730d4a75518fb4749af0b9e52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326022"
---
# <a name="downloaditemtype"></a><span data-ttu-id="1c7e5-106">DownloadItem. Type</span><span class="sxs-lookup"><span data-stu-id="1c7e5-106">DownloadItem.type</span></span>

> [!Note]  
> <span data-ttu-id="1c7e5-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1c7e5-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1c7e5-109">La proprietà **Type** Recupera il tipo di download.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-109">The **type** property retrieves the type of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c7e5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c7e5-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a><span data-ttu-id="1c7e5-111">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1c7e5-111">Possible Values</span></span>

<span data-ttu-id="1c7e5-112">Questa proprietà è una **stringa** di sola lettura contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-112">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="1c7e5-113">Valore</span><span class="sxs-lookup"><span data-stu-id="1c7e5-113">Value</span></span>      | <span data-ttu-id="1c7e5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c7e5-114">Description</span></span>                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c7e5-115">background</span><span class="sxs-lookup"><span data-stu-id="1c7e5-115">background</span></span> | <span data-ttu-id="1c7e5-116">(Solo Windows XP). Il download viene eseguito come processo in background, in quanto il tempo del processore diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-116">(Windows XP only.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="1c7e5-117">Gli Stati di download vengono mantenuti anche quando Windows Media Player o Windows XP viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-117">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="1c7e5-118">tempo reale</span><span class="sxs-lookup"><span data-stu-id="1c7e5-118">real time</span></span>  | <span data-ttu-id="1c7e5-119">(Tutti i sistemi operativi supportati). Il download viene eseguito in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-119">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="1c7e5-120">Nessun stato di download viene mantenuto tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-120">No download states persist between sessions.</span></span>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="1c7e5-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c7e5-121">Remarks</span></span>

<span data-ttu-id="1c7e5-122">Ogni tipo di download presenta vantaggi e svantaggi.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-122">Each type of download has advantages and disadvantages.</span></span> <span data-ttu-id="1c7e5-123">Il download in background consente all'utente di passare ad altre attività e persino di riavviare Windows senza annullare il download, ma richiede più tempo per completare il download ed è supportato solo per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-123">Background downloading allows the user to proceed to other tasks and even restart Windows without cancelling the download, but takes more time overall to complete the download and is only supported for Windows XP.</span></span> <span data-ttu-id="1c7e5-124">Il download in tempo reale richiede meno tempo, ma richiede che l'utente completi tutti i download prima di chiudere Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-124">Real-time downloading takes less time to complete, but requires the user to finish all downloading before closing Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c7e5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c7e5-125">Requirements</span></span>



| <span data-ttu-id="1c7e5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c7e5-126">Requirement</span></span> | <span data-ttu-id="1c7e5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1c7e5-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c7e5-128">Versione</span><span class="sxs-lookup"><span data-stu-id="1c7e5-128">Version</span></span><br/> | <span data-ttu-id="1c7e5-129">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1c7e5-129">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="1c7e5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1c7e5-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="1c7e5-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c7e5-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c7e5-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c7e5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c7e5-133">**Oggetto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="1c7e5-133">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





