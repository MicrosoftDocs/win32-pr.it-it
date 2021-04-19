---
title: DownloadManager. getdownloadcollection, metodo
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo getdownloadcollection recupera la raccolta di download specificata.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- Metodo getdownloadcollection Media Player Windows
- Metodo getdownloadcollection Windows Media Player, classe DownloadManager
- Classe DownloadManager Media Player Windows, metodo getdownloadcollection
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326013"
---
# <a name="downloadmanagergetdownloadcollection-method"></a><span data-ttu-id="44b9e-108">DownloadManager. getdownloadcollection, metodo</span><span class="sxs-lookup"><span data-stu-id="44b9e-108">DownloadManager.getDownloadCollection method</span></span>

> [!Note]  
> <span data-ttu-id="44b9e-109">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="44b9e-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="44b9e-110">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="44b9e-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="44b9e-111">Il metodo **Getdownloadcollection** recupera la raccolta di download specificata.</span><span class="sxs-lookup"><span data-stu-id="44b9e-111">The **getDownloadCollection** method retrieves the specified download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="44b9e-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44b9e-112">Syntax</span></span>


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a><span data-ttu-id="44b9e-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="44b9e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44b9e-114">*CollectionId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44b9e-114">*collectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44b9e-115">**Numero** (**Long**) che specifica l'ID della raccolta di download da recuperare.</span><span class="sxs-lookup"><span data-stu-id="44b9e-115">**Number** (**long**) specifying the ID of the download collection to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44b9e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44b9e-116">Return value</span></span>

<span data-ttu-id="44b9e-117">Questo metodo restituisce un oggetto **DownloadCollection** .</span><span class="sxs-lookup"><span data-stu-id="44b9e-117">This method returns a **DownloadCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44b9e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="44b9e-118">Remarks</span></span>

<span data-ttu-id="44b9e-119">È prima necessario chiamare *downloadmanager*. **createDownloadCollection** per creare una nuova raccolta e recuperare il relativo valore ID.</span><span class="sxs-lookup"><span data-stu-id="44b9e-119">You must first call *DownloadManager*.**createDownloadCollection** to create a new collection and retrieve its ID value.</span></span>

<span data-ttu-id="44b9e-120">Una raccolta di download esistente può contenere elementi che sono stati contrassegnati come annullati.</span><span class="sxs-lookup"><span data-stu-id="44b9e-120">An existing download collection may contain items that have been marked as cancelled.</span></span>

<span data-ttu-id="44b9e-121">Gli elementi di download in tempo reale non completati in una sessione precedente non vengono recuperati come parte della raccolta.</span><span class="sxs-lookup"><span data-stu-id="44b9e-121">Real-time download items not completed in a prior session are not retrieved as part of the collection.</span></span> <span data-ttu-id="44b9e-122">I download in background completati prima della sessione corrente rimangono nella raccolta di download fino a quando non vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="44b9e-122">Background downloads that were completed prior to the current session remain in the download collection until removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="44b9e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44b9e-123">Requirements</span></span>



| <span data-ttu-id="44b9e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="44b9e-124">Requirement</span></span> | <span data-ttu-id="44b9e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="44b9e-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44b9e-126">Versione</span><span class="sxs-lookup"><span data-stu-id="44b9e-126">Version</span></span><br/> | <span data-ttu-id="44b9e-127">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="44b9e-127">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="44b9e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="44b9e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="44b9e-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44b9e-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44b9e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44b9e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b9e-131">**Oggetto DownloadManager**</span><span class="sxs-lookup"><span data-stu-id="44b9e-131">**DownloadManager Object**</span></span>](downloadmanager-object.md)
</dt> <dt>

[<span data-ttu-id="44b9e-132">**DownloadManager. createDownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="44b9e-132">**DownloadManager. createDownloadCollection**</span></span>](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="44b9e-133">**Download (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="44b9e-133">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





