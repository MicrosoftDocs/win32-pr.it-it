---
title: Metodo elemento IWMPCdromCollection
description: Il metodo Item restituisce un'interfaccia IWMPCdrom in corrispondenza dell'indice specificato.
ms.assetid: 66e51aa9-39c8-4b79-9cc7-d7125516e87e
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, interfaccia IWMPCdromCollection
- Interfaccia IWMPCdromCollection Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- IWMPCdromCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0c4a0c79a17b1e6956ba640daec74f0cbb2825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329289"
---
# <a name="iwmpcdromcollectionitem-method"></a><span data-ttu-id="391b4-106">Metodo IWMPCdromCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="391b4-106">IWMPCdromCollection::Item method</span></span>

<span data-ttu-id="391b4-107">Il metodo **Item** restituisce un'interfaccia **IWMPCdrom** in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="391b4-107">The **Item** method returns an **IWMPCdrom** interface at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="391b4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="391b4-108">Syntax</span></span>


```CSharp
public IWMPCdrom Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPCdrom
Implements IWMPCdromCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="391b4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="391b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="391b4-110">*lIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="391b4-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="391b4-111">**System. Int32** che rappresenta l'indice.</span><span class="sxs-lookup"><span data-stu-id="391b4-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="391b4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="391b4-112">Return value</span></span>

<span data-ttu-id="391b4-113">Interfaccia **wmplib. IWMPCdrom** .</span><span class="sxs-lookup"><span data-stu-id="391b4-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="391b4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="391b4-114">Remarks</span></span>

<span data-ttu-id="391b4-115">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="391b4-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="391b4-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="391b4-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="391b4-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="391b4-117">Examples</span></span>

<span data-ttu-id="391b4-118">Nell'esempio seguente viene usato **Item** per visualizzare l'identificatore di unità e il nome della playlist da ogni CD disponibile nel computer in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="391b4-118">The following example uses **Item** to display the drive specifier and playlist name from each CD available on the computer in a list box.</span></span> <span data-ttu-id="391b4-119">Se l'unità contiene effettivamente contenuto DVD, è necessario Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="391b4-119">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="391b4-120">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="391b4-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives.
for (int i = 0; i < numDrives; i++)
{
    // Store the drive specifier and playlist name for this drive in a string.
    string pl = player.cdromCollection.Item(i).driveSpecifier + " ";
    pl += player.cdromCollection.Item(i).Playlist.name;

    // Add the string to a list box.
    myPlaylists.Items.Add(pl);
}
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Loop through the available drives.
For i As Integer = 0 To (numDrives - 1)

    &#39; Store the drive specifier and playlist name for this drive in a string.
    Dim pl As String = player.cdromCollection.Item(i).driveSpecifier + &quot; &quot;
    pl += player.cdromCollection.Item(i).Playlist.name

    &#39; Add the string to a list box.
    myPlaylists.Items.Add(pl)

Next i
```





## <a name="requirements"></a><span data-ttu-id="391b4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="391b4-121">Requirements</span></span>



| <span data-ttu-id="391b4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="391b4-122">Requirement</span></span> | <span data-ttu-id="391b4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="391b4-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="391b4-124">Versione</span><span class="sxs-lookup"><span data-stu-id="391b4-124">Version</span></span><br/>   | <span data-ttu-id="391b4-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="391b4-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="391b4-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="391b4-126">Namespace</span></span><br/> | <span data-ttu-id="391b4-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="391b4-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="391b4-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="391b4-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="391b4-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="391b4-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="391b4-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="391b4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="391b4-131">**Interfaccia IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="391b4-131">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="391b4-132">**Interfaccia IWMPCdromCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="391b4-132">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="391b4-133">**IWMPCdromCollection. Count (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="391b4-133">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="391b4-134">**IWMPCdromCollection. getByDriveSpecifier (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="391b4-134">**IWMPCdromCollection.getByDriveSpecifier (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="391b4-135">**IWMPPlaylist.name (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="391b4-135">**IWMPPlaylist.name (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="391b4-136">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="391b4-136">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="391b4-137">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="391b4-137">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





