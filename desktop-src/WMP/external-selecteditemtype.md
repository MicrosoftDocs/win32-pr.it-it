---
title: External. selectedItemType
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. selectedItemType
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- Media Player di Windows External. selectedItemType
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324544"
---
# <a name="externalselecteditemtype"></a><span data-ttu-id="8f1ed-105">External. selectedItemType</span><span class="sxs-lookup"><span data-stu-id="8f1ed-105">External.selectedItemType</span></span>

> [!Note]  
> <span data-ttu-id="8f1ed-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="8f1ed-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="8f1ed-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="8f1ed-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="8f1ed-108">La proprietà **selectedItemType** Recupera il tipo dell'elemento multimediale attualmente selezionato in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8f1ed-108">The **selectedItemType** property retrieves the type of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f1ed-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f1ed-109">Syntax</span></span>

<span data-ttu-id="8f1ed-110">finestra. External. selectedItemType ()</span><span class="sxs-lookup"><span data-stu-id="8f1ed-110">window.external.selectedItemType()</span></span>

## <a name="possible-values"></a><span data-ttu-id="8f1ed-111">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="8f1ed-111">Possible Values</span></span>

<span data-ttu-id="8f1ed-112">Questa proprietà è una **stringa** di sola lettura che contiene una delle [costanti del percorso della libreria](library-location-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8f1ed-112">This property is a read-only **String** that contains one of the [library location constants](library-location-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8f1ed-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f1ed-113">Remarks</span></span>

<span data-ttu-id="8f1ed-114">Questa proprietà viene utilizzata in combinazione con la proprietà **External. selectedItemID** .</span><span class="sxs-lookup"><span data-stu-id="8f1ed-114">This property is used in combination with the **External.selectedItemID** property.</span></span> <span data-ttu-id="8f1ed-115">Ad esempio, se **selectedItemType** è uguale a CPTrackID, **SELECTEDITEMID** è l'ID della traccia selezionata. Per ulteriori informazioni sul modo in cui Windows Media Player caratterizza le visualizzazioni del contenuto di un negozio online, vedere [posizione e elemento selezionato](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="8f1ed-115">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="8f1ed-116">Per alcune visualizzazioni di Windows Media Player è selezionato un particolare elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="8f1ed-116">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="8f1ed-117">Si supponga, ad esempio, che la visualizzazione corrente rappresenti un album.</span><span class="sxs-lookup"><span data-stu-id="8f1ed-117">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="8f1ed-118">Un album è un contenitore di tracce, quindi **selectedItemType** è uguale a CPTrackID e **SELECTEDITEMID** è l'ID della traccia selezionata. Altre visualizzazioni non dispongono di un elemento multimediale selezionato.</span><span class="sxs-lookup"><span data-stu-id="8f1ed-118">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="8f1ed-119">Ad esempio, se l'utente fa clic sul nodo radice dell'archivio online nel controllo di visualizzazione albero, Windows Media Player visualizza una pagina di individuazione fornita dal negozio online.</span><span class="sxs-lookup"><span data-stu-id="8f1ed-119">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="8f1ed-120">Il lettore non visualizza alcun contenitore di elementi multimediali nell'interfaccia utente del lettore.</span><span class="sxs-lookup"><span data-stu-id="8f1ed-120">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="8f1ed-121">In tal caso, **selectedItemType** è uguale a UnknownLocation e **selectedItemID** è uguale alla stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="8f1ed-121">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f1ed-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f1ed-122">Requirements</span></span>



| <span data-ttu-id="8f1ed-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f1ed-123">Requirement</span></span> | <span data-ttu-id="8f1ed-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8f1ed-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f1ed-125">Versione</span><span class="sxs-lookup"><span data-stu-id="8f1ed-125">Version</span></span><br/> | <span data-ttu-id="8f1ed-126">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="8f1ed-126">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="8f1ed-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8f1ed-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="8f1ed-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f1ed-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f1ed-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f1ed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f1ed-130">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="8f1ed-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8f1ed-131">**External. selectedItemID**</span><span class="sxs-lookup"><span data-stu-id="8f1ed-131">**External.selectedItemID**</span></span>](external-selecteditemid.md)
</dt> <dt>

[<span data-ttu-id="8f1ed-132">**Posizione e elemento selezionato**</span><span class="sxs-lookup"><span data-stu-id="8f1ed-132">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





