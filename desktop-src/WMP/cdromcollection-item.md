---
title: Metodo cdromcollection. Item
description: Il metodo Item recupera l'oggetto CDROM in corrispondenza dell'indice specificato.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, classe cdromcollection
- Classe cdromcollection Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333131"
---
# <a name="cdromcollectionitem-method"></a><span data-ttu-id="fb74e-106">Metodo cdromcollection. Item</span><span class="sxs-lookup"><span data-stu-id="fb74e-106">CdromCollection.item method</span></span>

<span data-ttu-id="fb74e-107">Il metodo **Item** recupera l'oggetto **CDROM** in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="fb74e-107">The **item** method retrieves the **Cdrom** object at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb74e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb74e-108">Syntax</span></span>


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="fb74e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb74e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb74e-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fb74e-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb74e-111">**Numero** (**Long**) che contiene l'indice.</span><span class="sxs-lookup"><span data-stu-id="fb74e-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb74e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb74e-112">Return value</span></span>

<span data-ttu-id="fb74e-113">Questo metodo restituisce un oggetto **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="fb74e-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb74e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb74e-114">Remarks</span></span>

<span data-ttu-id="fb74e-115">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="fb74e-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="fb74e-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fb74e-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="fb74e-117">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="fb74e-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="fb74e-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="fb74e-118">Examples</span></span>

<span data-ttu-id="fb74e-119">Nell'esempio JScript seguente viene usato *cdromcollection*. **elemento** per stampare il nome della playlist da ogni CD disponibile nel computer.</span><span class="sxs-lookup"><span data-stu-id="fb74e-119">The following JScript example uses *CdromCollection*.**item** to print the playlist name from each CD available on the computer.</span></span> <span data-ttu-id="fb74e-120">Se l'unità contiene effettivamente contenuto DVD, è necessario Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="fb74e-120">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="fb74e-121">È stato creato un elemento TextArea HTML con ID = "playlists".</span><span class="sxs-lookup"><span data-stu-id="fb74e-121">An HTML TextArea element was created with ID = "playlists".</span></span> <span data-ttu-id="fb74e-122">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="fb74e-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="fb74e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb74e-123">Requirements</span></span>



| <span data-ttu-id="fb74e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb74e-124">Requirement</span></span> | <span data-ttu-id="fb74e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fb74e-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb74e-126">Versione</span><span class="sxs-lookup"><span data-stu-id="fb74e-126">Version</span></span><br/> | <span data-ttu-id="fb74e-127">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="fb74e-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fb74e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fb74e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb74e-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb74e-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb74e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb74e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb74e-131">**Cdrom. driveSpecifier**</span><span class="sxs-lookup"><span data-stu-id="fb74e-131">**Cdrom.driveSpecifier**</span></span>](cdrom-drivespecifier.md)
</dt> <dt>

[<span data-ttu-id="fb74e-132">**Oggetto cdromcollection**</span><span class="sxs-lookup"><span data-stu-id="fb74e-132">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="fb74e-133">**Cdromcollection. Count**</span><span class="sxs-lookup"><span data-stu-id="fb74e-133">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="fb74e-134">**Playlist.name**</span><span class="sxs-lookup"><span data-stu-id="fb74e-134">**Playlist.name**</span></span>](playlist-name.md)
</dt> <dt>

[<span data-ttu-id="fb74e-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fb74e-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="fb74e-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fb74e-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





