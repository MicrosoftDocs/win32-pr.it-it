---
title: IWMPMedia getmarkername, metodo
description: Il metodo getmarkname restituisce il nome del marcatore in corrispondenza dell'indice specificato.
ms.assetid: 77f893cf-1669-41e3-9f62-8a1081e37add
keywords:
- Metodo getmarkname Media Player Windows
- Metodo getmarkname Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo getmarkname
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ba6a7bb640a397cce9c7dfd22b5f9b6203c47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332396"
---
# <a name="iwmpmediagetmarkername-method"></a><span data-ttu-id="31db6-106">Metodo IWMPMedia:: getmarkname</span><span class="sxs-lookup"><span data-stu-id="31db6-106">IWMPMedia::getMarkerName method</span></span>

<span data-ttu-id="31db6-107">Il metodo **Getmarkname** restituisce il nome del marcatore in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="31db6-107">The **getMarkerName** method returns the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="31db6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31db6-108">Syntax</span></span>


```CSharp
public System.String getMarkerName(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerName( _
  ByVal MarkerNum As System.Int32 _
) As System.String
Implements IWMPMedia.getMarkerName
```





## <a name="parameters"></a><span data-ttu-id="31db6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="31db6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31db6-110">*MarkerNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31db6-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31db6-111">**System. Int32** che rappresenta l'indice del marcatore.</span><span class="sxs-lookup"><span data-stu-id="31db6-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31db6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31db6-112">Return value</span></span>

<span data-ttu-id="31db6-113">**System. String** che rappresenta il nome del marcatore.</span><span class="sxs-lookup"><span data-stu-id="31db6-113">A **System.String** that is the marker name.</span></span>

## <a name="remarks"></a><span data-ttu-id="31db6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="31db6-114">Remarks</span></span>

<span data-ttu-id="31db6-115">Questo metodo restituisce **null** se il marcatore specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="31db6-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="31db6-116">Alcuni elementi multimediali non contengono marcatori.</span><span class="sxs-lookup"><span data-stu-id="31db6-116">Some media items do not contain markers.</span></span> <span data-ttu-id="31db6-117">Usare **markerCount** per verificare il numero di marcatori presenti nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="31db6-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="31db6-118">I numeri di indice del marcatore iniziano da 1.</span><span class="sxs-lookup"><span data-stu-id="31db6-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="31db6-119">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="31db6-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="31db6-120">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="31db6-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="31db6-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="31db6-121">Examples</span></span>

<span data-ttu-id="31db6-122">Nell'esempio di codice seguente viene usato **Getmarkname** per riempire una casella di testo a più righe con i nomi dei marcatori nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="31db6-122">The following code example uses **getMarkerName** to fill a multi-line text box with the names of the markers in the current media item.</span></span> <span data-ttu-id="31db6-123">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="31db6-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker names
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markers[i] = player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerNames.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mCount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker names
Dim markers(mCount) As String

&#39; Verify that at least one marker exists in the current media.
If (mCount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mCount

        &#39; Store the marker name in the array.
        markers(i) = player.currentMedia.getMarkerName(i)

    Next i

End If

&#39; Display the marker names in the text box.
markerNames.Lines = markers
```





## <a name="requirements"></a><span data-ttu-id="31db6-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31db6-124">Requirements</span></span>



| <span data-ttu-id="31db6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="31db6-125">Requirement</span></span> | <span data-ttu-id="31db6-126">Valore</span><span class="sxs-lookup"><span data-stu-id="31db6-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31db6-127">Versione</span><span class="sxs-lookup"><span data-stu-id="31db6-127">Version</span></span><br/>   | <span data-ttu-id="31db6-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="31db6-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="31db6-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="31db6-129">Namespace</span></span><br/> | <span data-ttu-id="31db6-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="31db6-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="31db6-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="31db6-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="31db6-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="31db6-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31db6-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31db6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31db6-134">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="31db6-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="31db6-135">**IWMPMedia. markerCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="31db6-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





