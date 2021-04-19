---
title: Proprietà imageSourceHeight di IWMPMedia
description: La proprietà imageSourceHeight Ottiene l'altezza in pixel dell'elemento multimediale corrente.
ms.assetid: d60f1713-7110-4605-9009-45825c380546
keywords:
- Finestra delle proprietà di imageSourceHeight Media Player
- Proprietà di imageSourceHeight Media Player Windows, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, proprietà imageSourceHeight
topic_type:
- apiref
api_name:
- IWMPMedia.imageSourceHeight
- IWMPMedia.get_imageSourceHeight
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b80a702f119ba72220e5ac3ac86b524ce8c11c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332394"
---
# <a name="iwmpmediaimagesourceheight-property"></a><span data-ttu-id="028bb-106">Proprietà IWMPMedia:: imageSourceHeight</span><span class="sxs-lookup"><span data-stu-id="028bb-106">IWMPMedia::imageSourceHeight property</span></span>

<span data-ttu-id="028bb-107">La proprietà **imageSourceHeight** Ottiene l'altezza in pixel dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="028bb-107">The **imageSourceHeight** property gets the height of the current media item in pixels.</span></span>

<span data-ttu-id="028bb-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="028bb-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="028bb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="028bb-109">Syntax</span></span>


```CSharp
public System.Int32 imageSourceHeight {get;}
```


```VB

Public ReadOnly Property imageSourceHeight As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="028bb-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="028bb-110">Property value</span></span>

<span data-ttu-id="028bb-111">**System. Int32** che rappresenta l'altezza dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="028bb-111">A **System.Int32** that is the height of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="028bb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="028bb-112">Remarks</span></span>

<span data-ttu-id="028bb-113">Se l'elemento multimediale non è quello corrente, questa proprietà restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="028bb-113">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="028bb-114">Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="028bb-114">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="028bb-115">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="028bb-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="028bb-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="028bb-116">Examples</span></span>

<span data-ttu-id="028bb-117">Nell'esempio seguente viene usato **imageSourceHeight** per visualizzare la dimensione dell'immagine, in pixel, dell'elemento multimediale corrente in una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="028bb-117">The following example uses **imageSourceHeight** to display the image size, in pixels, of the current media item in a text box.</span></span> <span data-ttu-id="028bb-118">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="028bb-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Store the height and width of the new media item.
         int height = player.currentMedia.imageSourceHeight;
         int width = player.currentMedia.imageSourceWidth;

         // Clear all the information in the text box.
         videoSize.Clear();

         // Test whether an image is visible.
         if (height != 0 && width != 0)
         {
            // Display the image size information.
            videoSize.Text = (width.ToString() + " x " + height.ToString());
         }
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = WMPLib.WMPOpenState.wmposMediaOpen) Then

        &#39; Store the height and width of the new media item.
        Dim Height As Integer = player.currentMedia.imageSourceHeight
        Dim Width As Integer = player.currentMedia.imageSourceWidth

        &#39; Clear all the information in the text box.
        videoSize.Clear()

        &#39; Test whether an image is visible.
        If (Height <> 0 And Width <> 0) Then

            &#39; Display the image size information.
            videoSize.Text = (Width.ToString() + &quot; x &quot; + Height.ToString())

        End If

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="028bb-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="028bb-119">Requirements</span></span>



| <span data-ttu-id="028bb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="028bb-120">Requirement</span></span> | <span data-ttu-id="028bb-121">Valore</span><span class="sxs-lookup"><span data-stu-id="028bb-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="028bb-122">Versione</span><span class="sxs-lookup"><span data-stu-id="028bb-122">Version</span></span><br/>   | <span data-ttu-id="028bb-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="028bb-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="028bb-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="028bb-124">Namespace</span></span><br/> | <span data-ttu-id="028bb-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="028bb-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="028bb-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="028bb-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="028bb-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="028bb-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="028bb-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="028bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="028bb-129">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="028bb-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





