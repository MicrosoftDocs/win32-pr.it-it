---
title: Metodo IWMPMedia getMarkerTime
description: Il metodo getMarkerTime restituisce l'ora del marcatore in corrispondenza dell'indice specificato.
ms.assetid: 1c617e3a-0978-479c-a636-b655082232c1
keywords:
- Metodo getMarkerTime Windows Media Player
- Metodo getMarkerTime Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo getMarkerTime
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df171977adeee3b597cab1f40469af1d975425c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332395"
---
# <a name="iwmpmediagetmarkertime-method"></a><span data-ttu-id="f67ac-106">Metodo IWMPMedia:: getMarkerTime</span><span class="sxs-lookup"><span data-stu-id="f67ac-106">IWMPMedia::getMarkerTime method</span></span>

<span data-ttu-id="f67ac-107">Il metodo **getMarkerTime** restituisce l'ora del marcatore in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="f67ac-107">The **getMarkerTime** method returns the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f67ac-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f67ac-108">Syntax</span></span>


```CSharp
public System.Double getMarkerTime(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerTime( _
  ByVal MarkerNum As System.Int32 _
) As System.Double
Implements IWMPMedia.getMarkerTime
```





## <a name="parameters"></a><span data-ttu-id="f67ac-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f67ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f67ac-110">*MarkerNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f67ac-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f67ac-111">**System. Int32** che rappresenta l'indice del marcatore.</span><span class="sxs-lookup"><span data-stu-id="f67ac-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f67ac-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f67ac-112">Return value</span></span>

<span data-ttu-id="f67ac-113">**System. Double** che rappresenta l'ora del marcatore.</span><span class="sxs-lookup"><span data-stu-id="f67ac-113">A **System.Double** that is the marker time.</span></span>

## <a name="remarks"></a><span data-ttu-id="f67ac-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f67ac-114">Remarks</span></span>

<span data-ttu-id="f67ac-115">Questo metodo restituisce **null** se il marcatore specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="f67ac-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="f67ac-116">Alcuni elementi multimediali non contengono marcatori.</span><span class="sxs-lookup"><span data-stu-id="f67ac-116">Some media items do not contain markers.</span></span> <span data-ttu-id="f67ac-117">Usare **markerCount** per verificare il numero di marcatori presenti nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="f67ac-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="f67ac-118">I numeri di indice del marcatore iniziano da 1.</span><span class="sxs-lookup"><span data-stu-id="f67ac-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="f67ac-119">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="f67ac-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="f67ac-120">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f67ac-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f67ac-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="f67ac-121">Examples</span></span>

<span data-ttu-id="f67ac-122">Nell'esempio di codice seguente viene usato **getMarkerTime** per riempire una casella di testo a più righe con la posizione di ogni marcatore.</span><span class="sxs-lookup"><span data-stu-id="f67ac-122">The following code example uses **getMarkerTime** to fill a multi-line text box with the location of each marker.</span></span> <span data-ttu-id="f67ac-123">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="f67ac-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker times.
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker information in the array.
        markers[i] = "Marker number " + i + " occurs at ";
        markers[i] += player.currentMedia.getMarkerTime(i).ToString();
        markers[i] += " second(s).";
    }

    // Display the marker times in the text box.
    markerTimes.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker times.
Dim markers(mcount) As String

&#39; Verify that at least one marker exists in the current media.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker information in the array.
        markers(i) = (&quot;Marker number &quot; + i + &quot; occurs at &quot;)
        markers(i) += player.currentMedia.getMarkerTime(i).ToString()
        markers(i) += &quot; second(s).&quot;

    Next i

    &#39; Display the marker times in the text box.
    markerTimes.Lines = markers

End If
```





## <a name="requirements"></a><span data-ttu-id="f67ac-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f67ac-124">Requirements</span></span>



| <span data-ttu-id="f67ac-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f67ac-125">Requirement</span></span> | <span data-ttu-id="f67ac-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f67ac-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f67ac-127">Versione</span><span class="sxs-lookup"><span data-stu-id="f67ac-127">Version</span></span><br/>   | <span data-ttu-id="f67ac-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f67ac-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f67ac-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f67ac-129">Namespace</span></span><br/> | <span data-ttu-id="f67ac-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f67ac-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f67ac-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="f67ac-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f67ac-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f67ac-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f67ac-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f67ac-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f67ac-134">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f67ac-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f67ac-135">**IWMPMedia. markerCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f67ac-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





