---
title: External. libraryLocationID
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- Media Player di Windows External. libraryLocationID
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324565"
---
# <a name="externallibrarylocationid"></a><span data-ttu-id="15eab-105">External. libraryLocationID</span><span class="sxs-lookup"><span data-stu-id="15eab-105">External.libraryLocationID</span></span>

> [!Note]  
> <span data-ttu-id="15eab-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="15eab-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="15eab-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="15eab-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="15eab-108">La proprietà **libraryLocationID** recupera l'identificatore dell'elemento multimediale specifico attualmente visualizzato nella visualizzazione del lettore.</span><span class="sxs-lookup"><span data-stu-id="15eab-108">The **libraryLocationID** property retrieves the identifier of the specific media item that is currently displayed in the Player's view.</span></span>

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a><span data-ttu-id="15eab-109">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="15eab-109">Possible Values</span></span>

<span data-ttu-id="15eab-110">Questa proprietà è una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="15eab-110">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="15eab-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="15eab-111">Remarks</span></span>

<span data-ttu-id="15eab-112">Questa proprietà funziona in combinazione con la proprietà [External. libraryLocationType](external-librarylocationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="15eab-112">This property works in combination with the [External.libraryLocationType](external-librarylocationtype.md) property.</span></span> <span data-ttu-id="15eab-113">Si supponga, ad esempio, che **libraryLocationType** sia uguale a CPAlbumID e che **libraryLocationID** sia uguale a 3.</span><span class="sxs-lookup"><span data-stu-id="15eab-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="15eab-114">Ciò significa che nella visualizzazione corrente di Windows Media Player viene visualizzato l'album con ID 3.</span><span class="sxs-lookup"><span data-stu-id="15eab-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="15eab-115">Per ulteriori informazioni sul modo in cui Windows Media Player caratterizza le visualizzazioni del contenuto di un negozio online, vedere [posizione e elemento selezionato](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="15eab-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="15eab-116">Alcune visualizzazioni in Windows Media Player sono associate a un particolare elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="15eab-116">Certain views in Windows Media Player are associated with a particular media item.</span></span> <span data-ttu-id="15eab-117">Ad esempio, se la visualizzazione corrente rappresenta un singolo album, **libraryLocationType** è uguale a CPAlbumID e **LIBRARYLOCATIONID** è l'ID dell'album.</span><span class="sxs-lookup"><span data-stu-id="15eab-117">For example, if the current view represents an individual album, **libraryLocationType** is equal to CPAlbumID, and **libraryLocationID** is the ID of the album.</span></span> <span data-ttu-id="15eab-118">Altre viste non sono associate a un particolare elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="15eab-118">Other views are not associated with any particular media item.</span></span> <span data-ttu-id="15eab-119">Se, ad esempio, la visualizzazione corrente rappresenta tutti gli album, **libraryLocationType** è uguale a AllCPAlbumIDs, ma non esiste alcun valore significativo che può essere assegnato a **libraryLocationID**.</span><span class="sxs-lookup"><span data-stu-id="15eab-119">For example, if the current view represents all albums, **libraryLocationType** is equal to AllCPAlbumIDs, but there is no meaningful value that can be assigned to **libraryLocationID**.</span></span> <span data-ttu-id="15eab-120">Nei casi in cui la proprietà **libraryLocationID** non ha un valore significativo, è uguale alla stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="15eab-120">In cases where the **libraryLocationID** property has no meaningful value, it is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="15eab-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15eab-121">Requirements</span></span>



| <span data-ttu-id="15eab-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="15eab-122">Requirement</span></span> | <span data-ttu-id="15eab-123">Valore</span><span class="sxs-lookup"><span data-stu-id="15eab-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15eab-124">Versione</span><span class="sxs-lookup"><span data-stu-id="15eab-124">Version</span></span><br/> | <span data-ttu-id="15eab-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="15eab-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="15eab-126">DLL</span><span class="sxs-lookup"><span data-stu-id="15eab-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="15eab-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15eab-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15eab-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15eab-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15eab-129">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="15eab-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="15eab-130">**External. libraryLocationType**</span><span class="sxs-lookup"><span data-stu-id="15eab-130">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="15eab-131">**Posizione e elemento selezionato**</span><span class="sxs-lookup"><span data-stu-id="15eab-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





