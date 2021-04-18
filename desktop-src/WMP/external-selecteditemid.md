---
title: External. selectedItemID
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. selectedItemID
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- Media Player di Windows External. selectedItemID
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768387c9e20082ef47cb0f502a2c4572bf462f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324545"
---
# <a name="externalselecteditemid"></a><span data-ttu-id="884f7-105">External. selectedItemID</span><span class="sxs-lookup"><span data-stu-id="884f7-105">External.selectedItemID</span></span>

> [!Note]  
> <span data-ttu-id="884f7-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="884f7-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="884f7-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="884f7-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="884f7-108">La proprietà **selectedItemID** recupera l'identificatore dell'elemento multimediale attualmente selezionato in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="884f7-108">The **selectedItemID** property retrieves the identifier of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="884f7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="884f7-109">Syntax</span></span>

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a><span data-ttu-id="884f7-110">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="884f7-110">Possible Values</span></span>

<span data-ttu-id="884f7-111">Questa proprietà è una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="884f7-111">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="884f7-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="884f7-112">Remarks</span></span>

<span data-ttu-id="884f7-113">Questa proprietà viene utilizzata in combinazione con la proprietà [External. selectedItemType](external-selecteditemtype.md) .</span><span class="sxs-lookup"><span data-stu-id="884f7-113">This property is used in combination with the [External.selectedItemType](external-selecteditemtype.md) property.</span></span> <span data-ttu-id="884f7-114">Ad esempio, se **selectedItemType** è uguale a CPTrackID, **SELECTEDITEMID** è l'ID della traccia selezionata. Per ulteriori informazioni sul modo in cui Windows Media Player caratterizza le visualizzazioni del contenuto di un negozio online, vedere [posizione e elemento selezionato](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="884f7-114">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="884f7-115">Per alcune visualizzazioni di Windows Media Player è selezionato un particolare elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="884f7-115">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="884f7-116">Si supponga, ad esempio, che la visualizzazione corrente rappresenti un album.</span><span class="sxs-lookup"><span data-stu-id="884f7-116">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="884f7-117">Un album è un contenitore di tracce, quindi **selectedItemType** è uguale a CPTrackID e **SELECTEDITEMID** è l'ID della traccia selezionata. Altre visualizzazioni non dispongono di un elemento multimediale selezionato.</span><span class="sxs-lookup"><span data-stu-id="884f7-117">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="884f7-118">Ad esempio, se l'utente fa clic sul nodo radice dell'archivio online nel controllo di visualizzazione albero, Windows Media Player visualizza una pagina di individuazione fornita dal negozio online.</span><span class="sxs-lookup"><span data-stu-id="884f7-118">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="884f7-119">Il lettore non visualizza alcun contenitore di elementi multimediali nell'interfaccia utente del lettore.</span><span class="sxs-lookup"><span data-stu-id="884f7-119">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="884f7-120">In tal caso, **selectedItemType** è uguale a UnknownLocation e **selectedItemID** è uguale alla stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="884f7-120">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="884f7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="884f7-121">Requirements</span></span>



| <span data-ttu-id="884f7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="884f7-122">Requirement</span></span> | <span data-ttu-id="884f7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="884f7-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="884f7-124">Versione</span><span class="sxs-lookup"><span data-stu-id="884f7-124">Version</span></span><br/> | <span data-ttu-id="884f7-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="884f7-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="884f7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="884f7-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="884f7-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="884f7-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="884f7-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="884f7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="884f7-129">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="884f7-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="884f7-130">**External. selectedItemType**</span><span class="sxs-lookup"><span data-stu-id="884f7-130">**External.selectedItemType**</span></span>](external-selecteditemtype.md)
</dt> <dt>

[<span data-ttu-id="884f7-131">**Posizione e elemento selezionato**</span><span class="sxs-lookup"><span data-stu-id="884f7-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





