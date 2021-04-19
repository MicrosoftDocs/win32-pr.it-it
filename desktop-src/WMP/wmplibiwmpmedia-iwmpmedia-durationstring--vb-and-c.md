---
title: Proprietà durationString di IWMPMedia
description: La proprietà durationString ottiene una stringa che indica la durata dell'elemento multimediale corrente nel formato HH MM SS.
ms.assetid: de33c737-d73e-41f0-9c1b-944279194738
keywords:
- Finestra delle proprietà di durationString Media Player
- Proprietà di durationString Media Player Windows, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, proprietà durationString
topic_type:
- apiref
api_name:
- IWMPMedia.durationString
- IWMPMedia.get_durationString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e6bc732388036aa9e79aeedd988de94fa263bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332408"
---
# <a name="iwmpmediadurationstring-property"></a><span data-ttu-id="dfb45-106">IWMPMedia::d proprietà urationString</span><span class="sxs-lookup"><span data-stu-id="dfb45-106">IWMPMedia::durationString property</span></span>

<span data-ttu-id="dfb45-107">La proprietà **durationstring** ottiene una stringa che indica la durata dell'elemento multimediale corrente nel formato HH: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="dfb45-107">The **durationString** property gets a string indicating the duration of the current media item in HH:MM:SS format.</span></span>

<span data-ttu-id="dfb45-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="dfb45-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb45-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfb45-109">Syntax</span></span>


```CSharp
public System.String durationString {get;}
```


```VB

Public ReadOnly Property durationString As System.String
```





## <a name="property-value"></a><span data-ttu-id="dfb45-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="dfb45-110">Property value</span></span>

<span data-ttu-id="dfb45-111">**System. String** che corrisponde alla durata.</span><span class="sxs-lookup"><span data-stu-id="dfb45-111">A **System.String** that is the duration.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfb45-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfb45-112">Remarks</span></span>

<span data-ttu-id="dfb45-113">Se questa proprietà viene utilizzata con un elemento multimediale diverso da quello specificato in AxWindowsMediaPlayer. currentMedia, potrebbe non contenere un valore valido.</span><span class="sxs-lookup"><span data-stu-id="dfb45-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span> <span data-ttu-id="dfb45-114">Se la lunghezza dell'elemento multimediale è inferiore a un'ora, la parte relativa all'ora del valore restituito viene omessa.</span><span class="sxs-lookup"><span data-stu-id="dfb45-114">If the media item is less than an hour long, the hours portion of the return value is omitted.</span></span>

<span data-ttu-id="dfb45-115">Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="dfb45-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="dfb45-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="dfb45-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dfb45-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="dfb45-117">Examples</span></span>

<span data-ttu-id="dfb45-118">Nell'esempio seguente viene usato **durationstring** per visualizzare la durata dell'elemento multimediale corrente come testo formattato in un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="dfb45-118">The following example uses **durationString** to display the duration of the current media item as formatted text in a label.</span></span> <span data-ttu-id="dfb45-119">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="dfb45-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Display the formatted duration string in the label.
         mediaDuration.Text = player.currentMedia.durationString;
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = 13) Then

        &#39; Display the formatted duration string in the label.
        mediaDuration.Text = player.currentMedia.durationString

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="dfb45-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfb45-120">Requirements</span></span>



| <span data-ttu-id="dfb45-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfb45-121">Requirement</span></span> | <span data-ttu-id="dfb45-122">Valore</span><span class="sxs-lookup"><span data-stu-id="dfb45-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb45-123">Versione</span><span class="sxs-lookup"><span data-stu-id="dfb45-123">Version</span></span><br/>   | <span data-ttu-id="dfb45-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="dfb45-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dfb45-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dfb45-125">Namespace</span></span><br/> | <span data-ttu-id="dfb45-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dfb45-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dfb45-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="dfb45-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dfb45-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dfb45-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb45-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfb45-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb45-130">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dfb45-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dfb45-131">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dfb45-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dfb45-132">**IWMPMedia. Duration (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dfb45-132">**IWMPMedia.duration (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)
</dt> </dl>

 

 





