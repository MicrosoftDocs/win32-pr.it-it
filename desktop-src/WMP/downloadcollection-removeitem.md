---
title: Metodo DownloadCollection. removeItem
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo removeItem rimuove un elemento di download da una raccolta di download.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- Metodo removeItem Windows Media Player
- Metodo removeItem Windows Media Player, classe DownloadCollection
- Scaricacollection (classe) Windows Media Player, metodo removeItem
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333417"
---
# <a name="downloadcollectionremoveitem-method"></a><span data-ttu-id="88dd0-108">Metodo DownloadCollection. removeItem</span><span class="sxs-lookup"><span data-stu-id="88dd0-108">DownloadCollection.removeItem method</span></span>

> [!Note]  
> <span data-ttu-id="88dd0-109">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="88dd0-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="88dd0-110">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="88dd0-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="88dd0-111">Il metodo **RemoveItem** rimuove un elemento di download da una raccolta di download.</span><span class="sxs-lookup"><span data-stu-id="88dd0-111">The **removeItem** method removes a download item from a download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="88dd0-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88dd0-112">Syntax</span></span>


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a><span data-ttu-id="88dd0-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="88dd0-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88dd0-114">*ID* \[ elemento in\]</span><span class="sxs-lookup"><span data-stu-id="88dd0-114">*itemID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88dd0-115">**Numero** (**Long**) che specifica l'indice del **DownloadItem** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="88dd0-115">**Number** (**long**) specifying the index of the **DownloadItem** to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88dd0-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88dd0-116">Return value</span></span>

<span data-ttu-id="88dd0-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="88dd0-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88dd0-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="88dd0-118">Remarks</span></span>

<span data-ttu-id="88dd0-119">Se è in corso il download rappresentato da *ItemId* , questo metodo annulla il download.</span><span class="sxs-lookup"><span data-stu-id="88dd0-119">If the download represented by *itemID* is in progress, this method cancels the download.</span></span>

## <a name="requirements"></a><span data-ttu-id="88dd0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88dd0-120">Requirements</span></span>



| <span data-ttu-id="88dd0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="88dd0-121">Requirement</span></span> | <span data-ttu-id="88dd0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="88dd0-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88dd0-123">Versione</span><span class="sxs-lookup"><span data-stu-id="88dd0-123">Version</span></span><br/> | <span data-ttu-id="88dd0-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="88dd0-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="88dd0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="88dd0-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="88dd0-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88dd0-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88dd0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88dd0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88dd0-128">**DownloadCollection. Item**</span><span class="sxs-lookup"><span data-stu-id="88dd0-128">**DownloadCollection.item**</span></span>](downloadcollection-item.md)
</dt> <dt>

[<span data-ttu-id="88dd0-129">**Download (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="88dd0-129">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





