---
title: External. libraryLocationType
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. libraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- Media Player di Windows External. libraryLocationType
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c2f14940a2ad41bed24493396e2bacfba2f0a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324564"
---
# <a name="externallibrarylocationtype"></a><span data-ttu-id="e7c87-105">External. libraryLocationType</span><span class="sxs-lookup"><span data-stu-id="e7c87-105">External.libraryLocationType</span></span>

> [!Note]  
> <span data-ttu-id="e7c87-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="e7c87-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e7c87-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e7c87-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e7c87-108">La proprietà **libraryLocationType** recupera una [costante del percorso della libreria](library-location-constants.md) che indica il tipo della visualizzazione corrente in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e7c87-108">The **libraryLocationType** property retrieves a [library location constant](library-location-constants.md) that indicates the type of the current view in Windows Media Player.</span></span>

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a><span data-ttu-id="e7c87-109">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="e7c87-109">Possible Values</span></span>

<span data-ttu-id="e7c87-110">Questa proprietà è una **stringa** di sola lettura che contiene una delle costanti del percorso della libreria.</span><span class="sxs-lookup"><span data-stu-id="e7c87-110">This property is a read-only **String** that contains one of the library location constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7c87-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7c87-111">Remarks</span></span>

<span data-ttu-id="e7c87-112">Questa proprietà funziona in combinazione con la proprietà [External. libraryLocationID](external-librarylocationid.md) .</span><span class="sxs-lookup"><span data-stu-id="e7c87-112">This property works in combination with the [External.libraryLocationID](external-librarylocationid.md) property.</span></span> <span data-ttu-id="e7c87-113">Si supponga, ad esempio, che **libraryLocationType** sia uguale a CPAlbumID e che **libraryLocationID** sia uguale a 3.</span><span class="sxs-lookup"><span data-stu-id="e7c87-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="e7c87-114">Ciò significa che nella visualizzazione corrente di Windows Media Player viene visualizzato l'album con ID 3.</span><span class="sxs-lookup"><span data-stu-id="e7c87-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="e7c87-115">Per ulteriori informazioni sul modo in cui Windows Media Player caratterizza le visualizzazioni del contenuto di un negozio online, vedere [posizione e elemento selezionato](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="e7c87-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7c87-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7c87-116">Requirements</span></span>



| <span data-ttu-id="e7c87-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7c87-117">Requirement</span></span> | <span data-ttu-id="e7c87-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e7c87-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c87-119">Versione</span><span class="sxs-lookup"><span data-stu-id="e7c87-119">Version</span></span><br/> | <span data-ttu-id="e7c87-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="e7c87-120">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="e7c87-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e7c87-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="e7c87-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7c87-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7c87-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7c87-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c87-124">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="e7c87-124">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e7c87-125">**External. libraryLocationID**</span><span class="sxs-lookup"><span data-stu-id="e7c87-125">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="e7c87-126">**Posizione e elemento selezionato**</span><span class="sxs-lookup"><span data-stu-id="e7c87-126">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





