---
title: Metodo mediacollection. Add
description: Il metodo Add aggiunge un nuovo elemento multimediale o una playlist alla raccolta. | Metodo mediacollection. Add
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Aggiungi metodo Windows Media Player
- Metodo Add Media Player Windows, classe Mediacollection
- Mediacollection (classe) Windows Media Player, Aggiungi metodo
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330358"
---
# <a name="mediacollectionadd-method"></a><span data-ttu-id="24724-107">Metodo mediacollection. Add</span><span class="sxs-lookup"><span data-stu-id="24724-107">MediaCollection.add method</span></span>

<span data-ttu-id="24724-108">Il metodo **Add** aggiunge un nuovo elemento multimediale o una playlist alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="24724-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="24724-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24724-109">Syntax</span></span>


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a><span data-ttu-id="24724-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="24724-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24724-111">*percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24724-111">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24724-112">**Stringa** che contiene il percorso.</span><span class="sxs-lookup"><span data-stu-id="24724-112">**String** containing the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24724-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24724-113">Return value</span></span>

<span data-ttu-id="24724-114">Questo metodo restituisce un oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="24724-114">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="24724-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="24724-115">Remarks</span></span>

<span data-ttu-id="24724-116">Questo metodo carica un elemento multimediale o una playlist esistente nella libreria, dato un percorso a un file.</span><span class="sxs-lookup"><span data-stu-id="24724-116">This method loads an existing media item or playlist into the library, given a path to a file.</span></span> <span data-ttu-id="24724-117">Questo metodo non sposta o modifica il file.</span><span class="sxs-lookup"><span data-stu-id="24724-117">This method does not move or change the file.</span></span> <span data-ttu-id="24724-118">Questo metodo ha esito negativo se viene specificato un percorso locale non valido, ma non viene verificata la validità dei file multimediali digitali prima che vengano aggiunti alla libreria.</span><span class="sxs-lookup"><span data-stu-id="24724-118">This method fails if given an invalid local path, but digital media files are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="24724-119">Questo metodo accetta sia i file di playlist statici che quelli automatici.</span><span class="sxs-lookup"><span data-stu-id="24724-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="24724-120">*PlaylistCollection*. il metodo **importPlaylist** può essere usato anche per aggiungere una playlist statica alla libreria.</span><span class="sxs-lookup"><span data-stu-id="24724-120">The *PlaylistCollection*.**importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="24724-121">Per usare questo metodo, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="24724-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="24724-122">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="24724-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="24724-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="24724-123">Examples</span></span>

<span data-ttu-id="24724-124">Nell'esempio Microsoft JScript seguente vengono aggiunti tre oggetti multimediali alla raccolta di supporti Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="24724-124">The following Microsoft JScript example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="24724-125">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="24724-125">The **Player** object was created with ID="Player".</span></span>


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a><span data-ttu-id="24724-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24724-126">Requirements</span></span>



| <span data-ttu-id="24724-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="24724-127">Requirement</span></span> | <span data-ttu-id="24724-128">Valore</span><span class="sxs-lookup"><span data-stu-id="24724-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24724-129">Versione</span><span class="sxs-lookup"><span data-stu-id="24724-129">Version</span></span><br/> | <span data-ttu-id="24724-130">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="24724-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="24724-131">DLL</span><span class="sxs-lookup"><span data-stu-id="24724-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="24724-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24724-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24724-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24724-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24724-134">**Gestione delle playlist**</span><span class="sxs-lookup"><span data-stu-id="24724-134">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="24724-135">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="24724-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="24724-136">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="24724-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="24724-137">**Mediacollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="24724-137">**MediaCollection.remove**</span></span>](mediacollection-remove.md)
</dt> <dt>

[<span data-ttu-id="24724-138">**PlaylistCollection. importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="24724-138">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="24724-139">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="24724-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="24724-140">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="24724-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





