---
title: Playlist. getItemInfo, metodo
description: Il metodo getItemInfo Recupera il valore di un attributo playlist.
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo getItemInfo
topic_type:
- apiref
api_name:
- Playlist.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b1151528d6cf4e36aaed1cb4dc48a70f4083c4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324736"
---
# <a name="playlistgetiteminfo-method"></a><span data-ttu-id="09060-106">Playlist. getItemInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="09060-106">Playlist.getItemInfo method</span></span>

<span data-ttu-id="09060-107">Il metodo **GetItemInfo** Recupera il valore di un attributo playlist.</span><span class="sxs-lookup"><span data-stu-id="09060-107">The **getItemInfo** method retrieves the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="09060-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09060-108">Syntax</span></span>


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="09060-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="09060-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09060-110">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09060-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09060-111">**Stringa** contenente il nome dell'attributo da recuperare.</span><span class="sxs-lookup"><span data-stu-id="09060-111">**String** containing the name of the attribute to be retrieved.</span></span> <span data-ttu-id="09060-112">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="09060-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09060-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09060-113">Return value</span></span>

<span data-ttu-id="09060-114">Questo metodo restituisce una **stringa**.</span><span class="sxs-lookup"><span data-stu-id="09060-114">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="09060-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="09060-115">Remarks</span></span>

<span data-ttu-id="09060-116">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="09060-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="09060-117">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="09060-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="09060-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="09060-118">Examples</span></span>

<span data-ttu-id="09060-119">Per il codice di esempio che usa questa proprietà, vedere la proprietà [attributeCount](playlist-attributecount.md) .</span><span class="sxs-lookup"><span data-stu-id="09060-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="09060-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09060-120">Requirements</span></span>



| <span data-ttu-id="09060-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="09060-121">Requirement</span></span> | <span data-ttu-id="09060-122">Valore</span><span class="sxs-lookup"><span data-stu-id="09060-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09060-123">Versione</span><span class="sxs-lookup"><span data-stu-id="09060-123">Version</span></span><br/> | <span data-ttu-id="09060-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="09060-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="09060-125">DLL</span><span class="sxs-lookup"><span data-stu-id="09060-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="09060-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09060-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09060-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09060-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09060-128">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="09060-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="09060-129">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="09060-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="09060-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="09060-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="09060-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="09060-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





