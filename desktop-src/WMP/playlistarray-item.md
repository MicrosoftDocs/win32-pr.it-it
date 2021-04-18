---
title: Metodo PlaylistArray. Item
description: Il metodo Item recupera la playlist in corrispondenza dell'indice specificato.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, classe PlaylistArray
- Classe PlaylistArray Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6144f6e1cfda93be32060e8206a96b0da7568d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330464"
---
# <a name="playlistarrayitem-method"></a><span data-ttu-id="97d30-106">Metodo PlaylistArray. Item</span><span class="sxs-lookup"><span data-stu-id="97d30-106">PlaylistArray.item method</span></span>

<span data-ttu-id="97d30-107">Il metodo **Item** recupera la playlist in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="97d30-107">The **item** method retrieves the playlist at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="97d30-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97d30-108">Syntax</span></span>


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="97d30-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="97d30-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97d30-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="97d30-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d30-111">**Numero** (**Long**) che contiene l'indice della playlist da recuperare.</span><span class="sxs-lookup"><span data-stu-id="97d30-111">**Number** (**long**) containing the index of the playlist to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97d30-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97d30-112">Return value</span></span>

<span data-ttu-id="97d30-113">Questo metodo restituisce un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="97d30-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="97d30-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="97d30-114">Remarks</span></span>

<span data-ttu-id="97d30-115">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="97d30-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="97d30-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="97d30-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97d30-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97d30-117">Requirements</span></span>



| <span data-ttu-id="97d30-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="97d30-118">Requirement</span></span> | <span data-ttu-id="97d30-119">Valore</span><span class="sxs-lookup"><span data-stu-id="97d30-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97d30-120">Versione</span><span class="sxs-lookup"><span data-stu-id="97d30-120">Version</span></span><br/> | <span data-ttu-id="97d30-121">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="97d30-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="97d30-122">DLL</span><span class="sxs-lookup"><span data-stu-id="97d30-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="97d30-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97d30-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97d30-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97d30-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d30-125">**Oggetto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="97d30-125">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="97d30-126">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="97d30-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="97d30-127">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="97d30-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





