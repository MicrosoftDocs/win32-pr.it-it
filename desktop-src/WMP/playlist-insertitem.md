---
title: Playlist. insertItem, metodo
description: Il metodo insertItem inserisce un elemento multimediale nella playlist nella posizione specificata.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- metodo insertItem Media Player Windows
- metodo insertItem Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo insertItem
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324722"
---
# <a name="playlistinsertitem-method"></a><span data-ttu-id="cfe22-106">Playlist. insertItem, metodo</span><span class="sxs-lookup"><span data-stu-id="cfe22-106">Playlist.insertItem method</span></span>

<span data-ttu-id="cfe22-107">Il metodo **InsertItem** inserisce un elemento multimediale nella playlist nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="cfe22-107">The **insertItem** method inserts a media item into the playlist at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe22-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cfe22-108">Syntax</span></span>


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a><span data-ttu-id="cfe22-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfe22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe22-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="cfe22-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe22-111">**Numero** (**Long**) che contiene l'indice in corrispondenza del quale aggiungere l'elemento.</span><span class="sxs-lookup"><span data-stu-id="cfe22-111">**Number** (**long**) containing the index at which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="cfe22-112">*elemento* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="cfe22-112">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe22-113">Oggetto **multimediale** da inserire.</span><span class="sxs-lookup"><span data-stu-id="cfe22-113">**Media** object to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe22-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfe22-114">Return value</span></span>

<span data-ttu-id="cfe22-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cfe22-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfe22-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfe22-116">Remarks</span></span>

<span data-ttu-id="cfe22-117">Per tutti gli elementi dopo l'elemento inserito i numeri di indice aumenteranno di uno.</span><span class="sxs-lookup"><span data-stu-id="cfe22-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="cfe22-118">Per usare questo metodo, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="cfe22-118">To use this method, full access to the library is required.</span></span> <span data-ttu-id="cfe22-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cfe22-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe22-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfe22-120">Requirements</span></span>



| <span data-ttu-id="cfe22-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe22-121">Requirement</span></span> | <span data-ttu-id="cfe22-122">Valore</span><span class="sxs-lookup"><span data-stu-id="cfe22-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe22-123">Versione</span><span class="sxs-lookup"><span data-stu-id="cfe22-123">Version</span></span><br/> | <span data-ttu-id="cfe22-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="cfe22-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cfe22-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cfe22-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="cfe22-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfe22-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe22-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfe22-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe22-128">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="cfe22-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="cfe22-129">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="cfe22-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="cfe22-130">**Playlist. removeItem**</span><span class="sxs-lookup"><span data-stu-id="cfe22-130">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="cfe22-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="cfe22-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="cfe22-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="cfe22-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





