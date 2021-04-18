---
title: Metodo IWMPPlaylist appendItem
description: Il metodo appendItem aggiunge un elemento multimediale alla fine di una playlist.
ms.assetid: d659298b-ec4e-4771-8e9b-8cfd7b3e0eb2
keywords:
- Metodo appendItem Windows Media Player
- Metodo appendItem Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, metodo appendItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.appendItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a94e1b515ec6301830af2de06bae32602bdf66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331993"
---
# <a name="iwmpplaylistappenditem-method"></a><span data-ttu-id="c644b-106">Metodo IWMPPlaylist:: appendItem</span><span class="sxs-lookup"><span data-stu-id="c644b-106">IWMPPlaylist::appendItem method</span></span>

<span data-ttu-id="c644b-107">Il metodo **appendItem** aggiunge un elemento multimediale alla fine di una playlist.</span><span class="sxs-lookup"><span data-stu-id="c644b-107">The **appendItem** method adds a media item to the end of a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="c644b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c644b-108">Syntax</span></span>


```CSharp
public void appendItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub appendItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.appendItem
```





## <a name="parameters"></a><span data-ttu-id="c644b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c644b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c644b-110">*pIWMPMedia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c644b-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c644b-111">Interfaccia **wmplib. IWMPMedia** che rappresenta l'elemento multimediale da accodare.</span><span class="sxs-lookup"><span data-stu-id="c644b-111">An **WMPLib.IWMPMedia** interface that represents the media item to be appended.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c644b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c644b-112">Return value</span></span>

<span data-ttu-id="c644b-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c644b-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c644b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c644b-114">Remarks</span></span>

<span data-ttu-id="c644b-115">Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="c644b-115">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="c644b-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c644b-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c644b-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="c644b-117">Examples</span></span>

<span data-ttu-id="c644b-118">Nell'esempio seguente viene usato **appendItem** per aggiungere l'elemento multimediale corrente alla playlist denominata "Three".</span><span class="sxs-lookup"><span data-stu-id="c644b-118">The following example uses **appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="c644b-119">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="c644b-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the current media item.
WMPLib.IWMPMedia currMedia = player.currentMedia;

// Get an interface to the playlist named "ThreeList".
WMPLib.IWMPPlaylist plThreeList = player.playlistCollection.getByName("ThreeList").Item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);
```


```VB

' Get an interface to the current media item.
Dim currMedia As WMPLib.IWMPMedia = player.currentMedia

&#39; Get an interface to the playlist named &quot;ThreeList&quot;.
Dim plThreeList As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;ThreeList&quot;).Item(0)

&#39; Append the media item to the playlist.
plThreeList.appendItem(currMedia)
```





## <a name="requirements"></a><span data-ttu-id="c644b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c644b-120">Requirements</span></span>



| <span data-ttu-id="c644b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c644b-121">Requirement</span></span> | <span data-ttu-id="c644b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c644b-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c644b-123">Versione</span><span class="sxs-lookup"><span data-stu-id="c644b-123">Version</span></span><br/>   | <span data-ttu-id="c644b-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c644b-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c644b-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c644b-125">Namespace</span></span><br/> | <span data-ttu-id="c644b-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c644b-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c644b-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="c644b-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c644b-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c644b-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c644b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c644b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c644b-130">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c644b-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c644b-131">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c644b-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





