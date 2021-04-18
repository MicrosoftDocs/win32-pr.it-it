---
title: External. addToBasket, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. addToBasket, metodo
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- Metodo addToBasket Windows Media Player
- Metodo addToBasket Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo addToBasket
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329932"
---
# <a name="externaladdtobasket-method"></a><span data-ttu-id="576b7-107">External. addToBasket, metodo</span><span class="sxs-lookup"><span data-stu-id="576b7-107">External.addToBasket method</span></span>

> [!Note]  
> <span data-ttu-id="576b7-108">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="576b7-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="576b7-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="576b7-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="576b7-110">Il metodo **addToBasket** aggiunge elementi multimediali al riquadro elenco (detto anche basket) in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="576b7-110">The **addToBasket** method adds media items to the list pane (also called the basket) in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="576b7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="576b7-111">Syntax</span></span>


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="576b7-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="576b7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="576b7-113">*ViewType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="576b7-113">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576b7-114">**Stringa** che specifica il tipo di elemento da aggiungere al riquadro elenco.</span><span class="sxs-lookup"><span data-stu-id="576b7-114">**String** that specifies the type of item being added to the list pane.</span></span> <span data-ttu-id="576b7-115">Il chiamante deve impostare questo parametro su una delle seguenti [costanti del percorso della libreria](library-location-constants.md):</span><span class="sxs-lookup"><span data-stu-id="576b7-115">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="576b7-116">CPListID</span><span class="sxs-lookup"><span data-stu-id="576b7-116">CPListID</span></span>

<span data-ttu-id="576b7-117">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="576b7-117">CPTrackID</span></span>

<span data-ttu-id="576b7-118">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="576b7-118">CPAlbumID</span></span>

<span data-ttu-id="576b7-119">CPArtist</span><span class="sxs-lookup"><span data-stu-id="576b7-119">CPArtist</span></span>

<span data-ttu-id="576b7-120">CPGenreID</span><span class="sxs-lookup"><span data-stu-id="576b7-120">CPGenreID</span></span>

<span data-ttu-id="576b7-121">CPAlbumSubGenreID</span><span class="sxs-lookup"><span data-stu-id="576b7-121">CPAlbumSubGenreID</span></span>

<span data-ttu-id="576b7-122">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="576b7-122">CPRadioID</span></span>

</dd> <dt>

<span data-ttu-id="576b7-123">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="576b7-123">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576b7-124">**Stringa** contenente gli ID, delimitati da punti e virgola, degli elementi da aggiungere al riquadro elenco.</span><span class="sxs-lookup"><span data-stu-id="576b7-124">**String** containing the IDs, delimited by semicolons, of the items to be added to the list pane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="576b7-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="576b7-125">Return value</span></span>

<span data-ttu-id="576b7-126">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="576b7-126">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="576b7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="576b7-127">Requirements</span></span>



| <span data-ttu-id="576b7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="576b7-128">Requirement</span></span> | <span data-ttu-id="576b7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="576b7-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="576b7-130">Versione</span><span class="sxs-lookup"><span data-stu-id="576b7-130">Version</span></span><br/> | <span data-ttu-id="576b7-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="576b7-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="576b7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="576b7-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="576b7-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="576b7-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="576b7-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="576b7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="576b7-135">**ExternalObject per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="576b7-135">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="576b7-136">**External. basketTitle**</span><span class="sxs-lookup"><span data-stu-id="576b7-136">**External.basketTitle**</span></span>](external-baskettitle.md)
</dt> </dl>

 

 





