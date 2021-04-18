---
title: Playlist. setItemInfo, metodo
description: Il metodo setItemInfo specifica il valore di un attributo della playlist.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- Metodo setItemInfo Windows Media Player
- Metodo setItemInfo Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo setItemInfo
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333839"
---
# <a name="playlistsetiteminfo-method"></a><span data-ttu-id="bba29-106">Playlist. setItemInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="bba29-106">Playlist.setItemInfo method</span></span>

<span data-ttu-id="bba29-107">Il metodo **setItemInfo** specifica il valore di un attributo della playlist.</span><span class="sxs-lookup"><span data-stu-id="bba29-107">The **setItemInfo** method specifies the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba29-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bba29-108">Syntax</span></span>


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="bba29-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bba29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba29-110">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bba29-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba29-111">**Stringa** contenente il nome dell'attributo da impostare.</span><span class="sxs-lookup"><span data-stu-id="bba29-111">**String** containing the name of the attribute to be set.</span></span> <span data-ttu-id="bba29-112">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bba29-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba29-113">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="bba29-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba29-114">**Stringa** contenente il nuovo valore per l'attributo.</span><span class="sxs-lookup"><span data-stu-id="bba29-114">**String** containing the new value for the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba29-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bba29-115">Return value</span></span>

<span data-ttu-id="bba29-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bba29-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bba29-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bba29-117">Remarks</span></span>

<span data-ttu-id="bba29-118">Un uso speciale del metodo **setItemInfo** consiste nell'ordinare gli elementi nella playlist usando l'attributo SortAttribute.</span><span class="sxs-lookup"><span data-stu-id="bba29-118">A special use of the **setItemInfo** method is to sort the items in the playlist by using the SortAttribute attribute.</span></span> <span data-ttu-id="bba29-119">Nell'esempio JScript seguente viene ordinata una playlist in base ai valori dell'attributo UserLastPlayedTime.</span><span class="sxs-lookup"><span data-stu-id="bba29-119">The following JScript example sorts a playlist by the values of the UserLastPlayedTime attribute.</span></span> <span data-ttu-id="bba29-120">La variabile playlist è un riferimento a un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="bba29-120">The variable playlist is a reference to a **Playlist** object.</span></span>


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



<span data-ttu-id="bba29-121">Per usare questo metodo, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="bba29-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="bba29-122">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="bba29-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="bba29-123">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bba29-123">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="bba29-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="bba29-124">Examples</span></span>

<span data-ttu-id="bba29-125">Per il codice di esempio che usa questa proprietà, vedere la proprietà [attributeCount](playlist-attributecount.md) .</span><span class="sxs-lookup"><span data-stu-id="bba29-125">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba29-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bba29-126">Requirements</span></span>



| <span data-ttu-id="bba29-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba29-127">Requirement</span></span> | <span data-ttu-id="bba29-128">Valore</span><span class="sxs-lookup"><span data-stu-id="bba29-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bba29-129">Versione</span><span class="sxs-lookup"><span data-stu-id="bba29-129">Version</span></span><br/> | <span data-ttu-id="bba29-130">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="bba29-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bba29-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bba29-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="bba29-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bba29-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bba29-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bba29-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba29-134">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="bba29-134">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="bba29-135">**Playlist. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="bba29-135">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="bba29-136">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bba29-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="bba29-137">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bba29-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





