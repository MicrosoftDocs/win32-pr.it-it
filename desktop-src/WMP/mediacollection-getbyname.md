---
title: Mediacollection. getByName (metodo)
description: Il metodo getByName recupera una playlist degli elementi multimediali con il nome specificato.
ms.assetid: f9395a4f-06d6-438b-b7c5-7a063abdf59f
keywords:
- metodo getByName Media Player Windows
- metodo getByName Media Player Windows, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getByName
topic_type:
- apiref
api_name:
- MediaCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a3fc6e34b508fa094f79d2fbbd1d44ab712789
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327167"
---
# <a name="mediacollectiongetbyname-method"></a><span data-ttu-id="36c3c-106">Mediacollection. getByName (metodo)</span><span class="sxs-lookup"><span data-stu-id="36c3c-106">MediaCollection.getByName method</span></span>

<span data-ttu-id="36c3c-107">Il metodo **GetByName** recupera una playlist degli elementi multimediali con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="36c3c-107">The **getByName** method retrieves a playlist of the media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="36c3c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36c3c-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="36c3c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="36c3c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36c3c-110">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36c3c-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36c3c-111">**Stringa** che contiene il nome.</span><span class="sxs-lookup"><span data-stu-id="36c3c-111">**String** containing the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36c3c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36c3c-112">Return value</span></span>

<span data-ttu-id="36c3c-113">Questo metodo restituisce un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="36c3c-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="36c3c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="36c3c-114">Remarks</span></span>

<span data-ttu-id="36c3c-115">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="36c3c-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="36c3c-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="36c3c-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="36c3c-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="36c3c-117">Examples</span></span>

<span data-ttu-id="36c3c-118">Nell'esempio JScript seguente viene utilizzato *mediacollection*. **GetByName** per recuperare tre elementi dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="36c3c-118">The following JScript example uses *MediaCollection*.**getByName** to retrieve three items from the library.</span></span> <span data-ttu-id="36c3c-119">Ogni elemento viene quindi aggiunto alla playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="36c3c-119">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="36c3c-120">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="36c3c-120">The **Player** object was created with ID="Player".</span></span>


```JScript
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get a playlist object that contains an Internet URL.
var One = Player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");
 
// Get a playlist object that contains a file on a network server.
var Two = Player.mediaCollection.getByName("Jeanne");

// Get a playlist object that contains a file on a local drive.
var Three = Player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use Playlist.item with
// an index of zero to reference that item.
Player.currentPlaylist.appendItem(One.item(0));
Player.currentPlaylist.appendItem(Two.item(0));
Player.currentPlaylist.appendItem(Three.item(0));

```



## <a name="requirements"></a><span data-ttu-id="36c3c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36c3c-121">Requirements</span></span>



| <span data-ttu-id="36c3c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="36c3c-122">Requirement</span></span> | <span data-ttu-id="36c3c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="36c3c-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36c3c-124">Versione</span><span class="sxs-lookup"><span data-stu-id="36c3c-124">Version</span></span><br/> | <span data-ttu-id="36c3c-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="36c3c-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="36c3c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="36c3c-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="36c3c-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36c3c-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36c3c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36c3c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36c3c-129">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="36c3c-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="36c3c-130">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="36c3c-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="36c3c-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="36c3c-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="36c3c-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="36c3c-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





