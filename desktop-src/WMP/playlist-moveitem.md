---
title: Playlist. moveItem, metodo
description: Il metodo moveItem modifica la posizione di un elemento nella playlist.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- Metodo moveItem Windows Media Player
- Metodo moveItem Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo moveItem
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332521"
---
# <a name="playlistmoveitem-method"></a><span data-ttu-id="79295-106">Playlist. moveItem, metodo</span><span class="sxs-lookup"><span data-stu-id="79295-106">Playlist.moveItem method</span></span>

<span data-ttu-id="79295-107">Il metodo **moveItem** modifica la posizione di un elemento nella playlist.</span><span class="sxs-lookup"><span data-stu-id="79295-107">The **moveItem** method changes the location of an item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="79295-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79295-108">Syntax</span></span>


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a><span data-ttu-id="79295-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="79295-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79295-110">*OldIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79295-110">*oldIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79295-111">**Numero** (**Long**) che contiene l'indice precedente.</span><span class="sxs-lookup"><span data-stu-id="79295-111">**Number** (**long**) containing the old index.</span></span>

</dd> <dt>

<span data-ttu-id="79295-112">*newIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79295-112">*newIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79295-113">**Numero** (**Long**) che contiene il nuovo indice.</span><span class="sxs-lookup"><span data-stu-id="79295-113">**Number** (**long**) containing the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79295-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79295-114">Return value</span></span>

<span data-ttu-id="79295-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="79295-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79295-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="79295-116">Remarks</span></span>

<span data-ttu-id="79295-117">Le playlist archiviate nella libreria possono essere modificate all'esterno del controllo.</span><span class="sxs-lookup"><span data-stu-id="79295-117">Playlists stored in the library can change outside your control.</span></span> <span data-ttu-id="79295-118">Assicurarsi di monitorare e gestire tutti gli eventi appropriati correlati alla playlist, in modo che l'ordine degli elementi nella playlist non venga modificato in modo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="79295-118">Be sure to monitor and handle all appropriate playlist-related events so that the order of items in the playlist does not change unexpectedly.</span></span>

<span data-ttu-id="79295-119">Per usare questo metodo, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="79295-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="79295-120">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="79295-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79295-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79295-121">Requirements</span></span>



| <span data-ttu-id="79295-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="79295-122">Requirement</span></span> | <span data-ttu-id="79295-123">Valore</span><span class="sxs-lookup"><span data-stu-id="79295-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79295-124">Versione</span><span class="sxs-lookup"><span data-stu-id="79295-124">Version</span></span><br/> | <span data-ttu-id="79295-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="79295-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="79295-126">DLL</span><span class="sxs-lookup"><span data-stu-id="79295-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="79295-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79295-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79295-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79295-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79295-129">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="79295-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="79295-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="79295-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="79295-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="79295-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





