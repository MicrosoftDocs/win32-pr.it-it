---
title: Proprietà imageSourceWidth di IWMPMedia
description: La proprietà imageSourceWidth ottiene la larghezza dell'elemento multimediale corrente in pixel.
ms.assetid: d3644217-6faf-415e-b0c0-23db85c31a3a
keywords:
- Finestra delle proprietà di imageSourceWidth Media Player
- Proprietà di imageSourceWidth Media Player Windows, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, proprietà imageSourceWidth
topic_type:
- apiref
api_name:
- IWMPMedia.imageSourceWidth
- IWMPMedia.get_imageSourceWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 441c4fb4a05f610aee5a2c923353fb9688bffcc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332392"
---
# <a name="iwmpmediaimagesourcewidth-property"></a><span data-ttu-id="6c524-106">Proprietà IWMPMedia:: imageSourceWidth</span><span class="sxs-lookup"><span data-stu-id="6c524-106">IWMPMedia::imageSourceWidth property</span></span>

<span data-ttu-id="6c524-107">La proprietà **imageSourceWidth** ottiene la larghezza dell'elemento multimediale corrente in pixel.</span><span class="sxs-lookup"><span data-stu-id="6c524-107">The **imageSourceWidth** property gets the width of the current media item in pixels.</span></span>

<span data-ttu-id="6c524-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6c524-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c524-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c524-109">Syntax</span></span>


```CSharp
public System.Int32 imageSourceWidth {get;}
```


```VB

Public ReadOnly Property imageSourceWidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="6c524-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6c524-110">Property value</span></span>

<span data-ttu-id="6c524-111">**System. Int32** che rappresenta la larghezza dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="6c524-111">A **System.Int32** that is the width of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c524-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c524-112">Remarks</span></span>

<span data-ttu-id="6c524-113">Se l'elemento multimediale non è quello corrente, questa proprietà restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="6c524-113">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="6c524-114">Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="6c524-114">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="6c524-115">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6c524-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6c524-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="6c524-116">Examples</span></span>

<span data-ttu-id="6c524-117">Nell'esempio seguente viene usato **imageSourceWidth** per visualizzare la dimensione dell'immagine, in pixel, dell'elemento multimediale corrente in una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="6c524-117">The following example uses **imageSourceWidth** to display the image size, in pixels, of the current media item in a text box.</span></span> <span data-ttu-id="6c524-118">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="6c524-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the new media item is open.
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

    &#39; Test whether the new media item is open.
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





## <a name="requirements"></a><span data-ttu-id="6c524-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c524-119">Requirements</span></span>



| <span data-ttu-id="6c524-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c524-120">Requirement</span></span> | <span data-ttu-id="6c524-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6c524-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c524-122">Versione</span><span class="sxs-lookup"><span data-stu-id="6c524-122">Version</span></span><br/>   | <span data-ttu-id="6c524-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6c524-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6c524-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6c524-124">Namespace</span></span><br/> | <span data-ttu-id="6c524-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6c524-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6c524-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="6c524-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6c524-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6c524-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c524-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c524-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c524-129">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6c524-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





