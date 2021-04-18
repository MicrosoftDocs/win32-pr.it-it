---
title: Metodo External. Buy
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo Buy avvia l'acquisto di un set di elementi multimediali.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- acquistare il metodo Windows Media Player
- Metodo di acquisto Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo Buy
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328888"
---
# <a name="externalbuy-method"></a><span data-ttu-id="dfd68-108">Metodo External. Buy</span><span class="sxs-lookup"><span data-stu-id="dfd68-108">External.buy method</span></span>

> [!Note]  
> <span data-ttu-id="dfd68-109">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="dfd68-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="dfd68-110">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="dfd68-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="dfd68-111">Il metodo **buy** avvia l'acquisto di un set di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="dfd68-111">The **buy** method initiates the purchase of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd68-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfd68-112">Syntax</span></span>


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="dfd68-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="dfd68-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfd68-114">*ViewType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd68-114">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd68-115">**Stringa** che specifica il tipo di elemento da acquistare.</span><span class="sxs-lookup"><span data-stu-id="dfd68-115">**String** that specifies the type of item to be purchased.</span></span> <span data-ttu-id="dfd68-116">Il chiamante deve impostare questo parametro su una delle seguenti [costanti del percorso della libreria](library-location-constants.md):</span><span class="sxs-lookup"><span data-stu-id="dfd68-116">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="dfd68-117">CPListID</span><span class="sxs-lookup"><span data-stu-id="dfd68-117">CPListID</span></span>

<span data-ttu-id="dfd68-118">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="dfd68-118">CPTrackID</span></span>

<span data-ttu-id="dfd68-119">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="dfd68-119">CPAlbumID</span></span>

</dd> <dt>

<span data-ttu-id="dfd68-120">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfd68-120">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd68-121">**Stringa** contenente gli ID, delimitati da punti e virgola, degli elementi da acquistare.</span><span class="sxs-lookup"><span data-stu-id="dfd68-121">**String** containing the IDs, delimited by semicolons, of the items to be purchased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfd68-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dfd68-122">Return value</span></span>

<span data-ttu-id="dfd68-123">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="dfd68-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd68-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfd68-124">Requirements</span></span>



| <span data-ttu-id="dfd68-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfd68-125">Requirement</span></span> | <span data-ttu-id="dfd68-126">Valore</span><span class="sxs-lookup"><span data-stu-id="dfd68-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd68-127">Versione</span><span class="sxs-lookup"><span data-stu-id="dfd68-127">Version</span></span><br/> | <span data-ttu-id="dfd68-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="dfd68-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="dfd68-129">DLL</span><span class="sxs-lookup"><span data-stu-id="dfd68-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="dfd68-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfd68-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfd68-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfd68-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd68-132">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="dfd68-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="dfd68-133">**External. download**</span><span class="sxs-lookup"><span data-stu-id="dfd68-133">**External.download**</span></span>](external-download.md)
</dt> <dt>

[<span data-ttu-id="dfd68-134">**IWMPContentPartner:: Buy**</span><span class="sxs-lookup"><span data-stu-id="dfd68-134">**IWMPContentPartner::Buy**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[<span data-ttu-id="dfd68-135">**Acquisto di contenuti multimediali**</span><span class="sxs-lookup"><span data-stu-id="dfd68-135">**Purchasing Media Content**</span></span>](purchasing-media-content.md)
</dt> </dl>

 

 





