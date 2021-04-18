---
title: IWMPMediaCollection Add (metodo)
description: Il metodo Add aggiunge un nuovo elemento multimediale o una playlist alla raccolta. | IWMPMediaCollection Add (metodo)
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Aggiungi metodo Windows Media Player
- aggiungere il metodo Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, Aggiungi metodo
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7953067281e394df71a1a53c874cb80837a5f35d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324364"
---
# <a name="iwmpmediacollectionadd-method"></a><span data-ttu-id="65a3e-107">Metodo IWMPMediaCollection:: Add</span><span class="sxs-lookup"><span data-stu-id="65a3e-107">IWMPMediaCollection::add method</span></span>

<span data-ttu-id="65a3e-108">Il metodo **Add** aggiunge un nuovo elemento multimediale o una playlist alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="65a3e-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a3e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65a3e-109">Syntax</span></span>


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a><span data-ttu-id="65a3e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="65a3e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65a3e-111">*bstrURL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65a3e-111">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a3e-112">**System. String** che rappresenta l'URL che specifica la posizione dell'elemento multimediale o della playlist.</span><span class="sxs-lookup"><span data-stu-id="65a3e-112">A **System.String** that is the URL that specifies the location of the media item or playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65a3e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65a3e-113">Return value</span></span>

<span data-ttu-id="65a3e-114">Interfaccia **wmplib. IWMPMedia** per l'elemento o la playlist aggiunta.</span><span class="sxs-lookup"><span data-stu-id="65a3e-114">The **WMPLib.IWMPMedia** interface for the added item or playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="65a3e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="65a3e-115">Remarks</span></span>

<span data-ttu-id="65a3e-116">Questo metodo carica un elemento multimediale o una playlist esistente nella libreria, dato un percorso.</span><span class="sxs-lookup"><span data-stu-id="65a3e-116">This method loads an existing media item or playlist into the library, given a path.</span></span> <span data-ttu-id="65a3e-117">Questo metodo non sposta o modifica il file.</span><span class="sxs-lookup"><span data-stu-id="65a3e-117">This method does not move or change the file.</span></span> <span data-ttu-id="65a3e-118">Questo metodo ha esito negativo se viene specificato un percorso locale non valido, ma non viene verificata la validità degli elementi multimediali prima che vengano aggiunti alla libreria.</span><span class="sxs-lookup"><span data-stu-id="65a3e-118">This method fails if given an invalid local path, but media items themselves are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="65a3e-119">Questo metodo accetta sia i file di playlist statici che quelli automatici.</span><span class="sxs-lookup"><span data-stu-id="65a3e-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="65a3e-120">Il metodo **IWMPPlaylistCollection. importPlaylist** può essere usato anche per aggiungere una playlist statica alla libreria.</span><span class="sxs-lookup"><span data-stu-id="65a3e-120">The **IWMPPlaylistCollection.importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="65a3e-121">Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="65a3e-121">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="65a3e-122">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="65a3e-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="65a3e-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="65a3e-123">Examples</span></span>

<span data-ttu-id="65a3e-124">Nell'esempio seguente vengono aggiunti tre oggetti multimediali alla raccolta di supporti Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="65a3e-124">The following example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="65a3e-125">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="65a3e-125">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
```





## <a name="requirements"></a><span data-ttu-id="65a3e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65a3e-126">Requirements</span></span>



| <span data-ttu-id="65a3e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="65a3e-127">Requirement</span></span> | <span data-ttu-id="65a3e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="65a3e-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65a3e-129">Versione</span><span class="sxs-lookup"><span data-stu-id="65a3e-129">Version</span></span><br/>   | <span data-ttu-id="65a3e-130">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="65a3e-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="65a3e-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="65a3e-131">Namespace</span></span><br/> | <span data-ttu-id="65a3e-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="65a3e-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="65a3e-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="65a3e-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="65a3e-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="65a3e-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65a3e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65a3e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a3e-136">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="65a3e-136">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="65a3e-137">**IWMPMediaCollection. Remove (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="65a3e-137">**IWMPMediaCollection.remove (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="65a3e-138">**IWMPPlaylistCollection. importPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="65a3e-138">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





