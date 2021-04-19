---
title: Proprietà markerCount di IWMPMedia
description: La proprietà markerCount ottiene il numero di marcatori nell'elemento multimediale.
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- Finestra delle proprietà di markerCount Media Player
- Proprietà di markerCount Media Player Windows, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, proprietà markerCount
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad591d8be66dcd20bc5e59d206a637d9b1181f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332389"
---
# <a name="iwmpmediamarkercount-property"></a><span data-ttu-id="91c36-106">Proprietà IWMPMedia:: markerCount</span><span class="sxs-lookup"><span data-stu-id="91c36-106">IWMPMedia::markerCount property</span></span>

<span data-ttu-id="91c36-107">La proprietà **markerCount** ottiene il numero di marcatori nell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="91c36-107">The **markerCount** property gets the number of markers in the media item.</span></span>

<span data-ttu-id="91c36-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="91c36-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c36-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91c36-109">Syntax</span></span>


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="91c36-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="91c36-110">Property value</span></span>

<span data-ttu-id="91c36-111">**System. Int32** che rappresenta il numero di marcatori.</span><span class="sxs-lookup"><span data-stu-id="91c36-111">A **System.Int32** that is the marker count.</span></span>

## <a name="remarks"></a><span data-ttu-id="91c36-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="91c36-112">Remarks</span></span>

<span data-ttu-id="91c36-113">Questa proprietà restituisce zero se un file non ha marcatori o se l'elemento multimediale non è uguale a quello specificato in AxWindowsMediaPlayer. currentMedia.</span><span class="sxs-lookup"><span data-stu-id="91c36-113">This property returns zero if a file has no markers, or if the media item is not the same as the one specified in AxWindowsMediaPlayer.currentMedia.</span></span>

<span data-ttu-id="91c36-114">I numeri degli indicatori iniziano da 1.</span><span class="sxs-lookup"><span data-stu-id="91c36-114">Marker numbers start at 1.</span></span>

<span data-ttu-id="91c36-115">Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="91c36-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="91c36-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="91c36-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="91c36-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="91c36-117">Examples</span></span>

<span data-ttu-id="91c36-118">Nell'esempio seguente viene usato **markerCount** per recuperare il numero di marcatori nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="91c36-118">The following example uses **markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="91c36-119">Tale valore viene quindi utilizzato come limite superiore per una struttura di ciclo, che scorre l'elenco dei marcatori per recuperare ogni nome del marcatore e visualizzarlo in una casella di testo a più righe.</span><span class="sxs-lookup"><span data-stu-id="91c36-119">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name and display it in a multi-line text box.</span></span> <span data-ttu-id="91c36-120">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="91c36-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
```





## <a name="requirements"></a><span data-ttu-id="91c36-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91c36-121">Requirements</span></span>



| <span data-ttu-id="91c36-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="91c36-122">Requirement</span></span> | <span data-ttu-id="91c36-123">Valore</span><span class="sxs-lookup"><span data-stu-id="91c36-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c36-124">Versione</span><span class="sxs-lookup"><span data-stu-id="91c36-124">Version</span></span><br/>   | <span data-ttu-id="91c36-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="91c36-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="91c36-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="91c36-126">Namespace</span></span><br/> | <span data-ttu-id="91c36-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="91c36-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="91c36-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="91c36-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="91c36-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="91c36-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91c36-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91c36-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c36-131">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="91c36-131">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="91c36-132">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="91c36-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





