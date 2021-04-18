---
title: DownloadItem. Cancel, metodo
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo Cancel Annulla il download.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- Annulla il metodo Windows Media Player
- Metodo Cancel Media Player Windows, classe DownloadItem
- Classe DownloadItem Media Player Windows, metodo Cancel
topic_type:
- apiref
api_name:
- DownloadItem.cancel
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c14d538e85d0930a43db883e226c007bea70de24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331484"
---
# <a name="downloaditemcancel-method"></a><span data-ttu-id="e36ee-108">DownloadItem. Cancel, metodo</span><span class="sxs-lookup"><span data-stu-id="e36ee-108">DownloadItem.cancel method</span></span>

> [!Note]  
> <span data-ttu-id="e36ee-109">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="e36ee-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e36ee-110">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e36ee-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e36ee-111">Il metodo **Cancel** Annulla il download.</span><span class="sxs-lookup"><span data-stu-id="e36ee-111">The **cancel** method cancels the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="e36ee-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e36ee-112">Syntax</span></span>


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a><span data-ttu-id="e36ee-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="e36ee-113">Parameters</span></span>

<span data-ttu-id="e36ee-114">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e36ee-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e36ee-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e36ee-115">Return value</span></span>

<span data-ttu-id="e36ee-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e36ee-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e36ee-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e36ee-117">Remarks</span></span>

<span data-ttu-id="e36ee-118">Gli elementi annullati non vengono rimossi dalla raccolta di download.</span><span class="sxs-lookup"><span data-stu-id="e36ee-118">Cancelled items are not removed from the download collection.</span></span> <span data-ttu-id="e36ee-119">Gli elementi annullati restituiscono un valore **downloadState** pari a 4 (annullato).</span><span class="sxs-lookup"><span data-stu-id="e36ee-119">Cancelled items return a **downloadState** value of 4 (canceled).</span></span>

## <a name="requirements"></a><span data-ttu-id="e36ee-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e36ee-120">Requirements</span></span>



| <span data-ttu-id="e36ee-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e36ee-121">Requirement</span></span> | <span data-ttu-id="e36ee-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e36ee-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e36ee-123">Versione</span><span class="sxs-lookup"><span data-stu-id="e36ee-123">Version</span></span><br/> | <span data-ttu-id="e36ee-124">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e36ee-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e36ee-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e36ee-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="e36ee-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e36ee-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e36ee-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e36ee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e36ee-128">**Oggetto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="e36ee-128">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="e36ee-129">**DownloadItem.downloadState**</span><span class="sxs-lookup"><span data-stu-id="e36ee-129">**DownloadItem.downloadState**</span></span>](downloaditem-downloadstate.md)
</dt> </dl>

 

 





