---
title: PlaylistCollection. getByName (metodo)
description: Il metodo getByName recupera un oggetto PlaylistArray contenente playlist con il nome specificato, se esistente.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- metodo getByName Media Player Windows
- metodo getByName Windows Media Player, Classe PlaylistCollection
- Classe PlaylistCollection Windows Media Player, metodo getByName
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330455"
---
# <a name="playlistcollectiongetbyname-method"></a><span data-ttu-id="0af43-106">PlaylistCollection. getByName (metodo)</span><span class="sxs-lookup"><span data-stu-id="0af43-106">PlaylistCollection.getByName method</span></span>

<span data-ttu-id="0af43-107">Il metodo **GetByName** recupera un oggetto **PlaylistArray** contenente playlist con il nome specificato, se esistente.</span><span class="sxs-lookup"><span data-stu-id="0af43-107">The **getByName** method retrieves a **PlaylistArray** object containing playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="0af43-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0af43-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="0af43-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0af43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0af43-110">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0af43-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0af43-111">**Stringa** contenente il nome delle playlist da recuperare.</span><span class="sxs-lookup"><span data-stu-id="0af43-111">**String** containing the name of the playlists to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0af43-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0af43-112">Return value</span></span>

<span data-ttu-id="0af43-113">Questo metodo restituisce un oggetto **PlaylistArray** .</span><span class="sxs-lookup"><span data-stu-id="0af43-113">This method returns a **PlaylistArray** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0af43-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0af43-114">Remarks</span></span>

<span data-ttu-id="0af43-115">Usare *PlaylistArray*. **conteggio** per determinare se esiste una playlist.</span><span class="sxs-lookup"><span data-stu-id="0af43-115">Use *PlaylistArray*.**count** to determine whether a playlist exists.</span></span> <span data-ttu-id="0af43-116">Se **count** è zero, una playlist non esiste.</span><span class="sxs-lookup"><span data-stu-id="0af43-116">If **count** is zero, a playlist does not exist.</span></span>

<span data-ttu-id="0af43-117">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="0af43-117">To use this method, read access to the library is required.</span></span> <span data-ttu-id="0af43-118">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0af43-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0af43-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="0af43-119">Examples</span></span>

<span data-ttu-id="0af43-120">Nell'esempio di codice JScript seguente viene usato *PlaylistCollection*. **GetByName** per controllare l'oggetto **PlaylistCollection** per una playlist denominata "Three".</span><span class="sxs-lookup"><span data-stu-id="0af43-120">The following JScript example uses *playlistCollection*.**getByName** to check the **playlistCollection** object for a playlist named "ThreeList".</span></span> <span data-ttu-id="0af43-121">Se è presente la playlist "Three-", **GetByName** imposta "Three" come playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="0af43-121">If the "Threelist" playlist exists, **getByName** sets "ThreeList" as the current playlist.</span></span> <span data-ttu-id="0af43-122">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="0af43-122">The **Player** object was created with the ID = "Player".</span></span>


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a><span data-ttu-id="0af43-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0af43-123">Requirements</span></span>



| <span data-ttu-id="0af43-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0af43-124">Requirement</span></span> | <span data-ttu-id="0af43-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0af43-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0af43-126">Versione</span><span class="sxs-lookup"><span data-stu-id="0af43-126">Version</span></span><br/> | <span data-ttu-id="0af43-127">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="0af43-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0af43-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0af43-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="0af43-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0af43-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0af43-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0af43-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af43-131">**Oggetto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="0af43-131">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="0af43-132">**PlaylistArray. Count**</span><span class="sxs-lookup"><span data-stu-id="0af43-132">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="0af43-133">**PlaylistCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="0af43-133">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="0af43-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0af43-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0af43-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0af43-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





