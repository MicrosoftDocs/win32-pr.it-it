---
title: Proprietà AxWindowsMediaPlayer. fullScreen
description: La proprietà fullScreen Ottiene o imposta un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- Finestre delle proprietà a schermo intero Media Player
- Proprietà fullScreen Media Player Windows, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, proprietà fullScreen
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324384"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a><span data-ttu-id="2d420-106">Proprietà AxWindowsMediaPlayer. fullScreen</span><span class="sxs-lookup"><span data-stu-id="2d420-106">AxWindowsMediaPlayer.fullScreen property</span></span>

<span data-ttu-id="2d420-107">La proprietà fullScreen Ottiene o imposta un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="2d420-107">The fullScreen property gets or sets a value indicating whether video content is played in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d420-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d420-108">Syntax</span></span>


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="2d420-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2d420-109">Property value</span></span>

<span data-ttu-id="2d420-110">Valore System. Boolean che indica se il contenuto viene riprodotto in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="2d420-110">A System.Boolean value that indicates whether content is played in full-screen mode.</span></span> <span data-ttu-id="2d420-111">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="2d420-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d420-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d420-112">Remarks</span></span>

<span data-ttu-id="2d420-113">Per il corretto funzionamento della modalità a schermo intero quando si incorpora il controllo Media Player di Windows, l'area di visualizzazione del video deve avere un'altezza e una larghezza pari ad almeno un pixel.</span><span class="sxs-lookup"><span data-stu-id="2d420-113">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="2d420-114">Se **uiMode** è impostato su "mini" o "full", l'altezza del controllo deve essere 65 o superiore per ospitare l'area di visualizzazione video oltre all'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="2d420-114">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="2d420-115">Se **uiMode** è impostato su "invisibile", l'impostazione di questa proprietà su true genera un errore e non influisce sul comportamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="2d420-115">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="2d420-116">Durante la riproduzione a schermo intero, Windows Media Player nasconde il cursore del mouse quando [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) è uguale a false e **uiMode** è uguale a "None".</span><span class="sxs-lookup"><span data-stu-id="2d420-116">During full-screen playback, Windows Media Player hides the mouse cursor when [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="2d420-117">Se **uiMode** è impostato su "full" o "mini", Windows Media Player Visualizza i controlli di trasporto in modalità schermo intero quando il cursore del mouse si sposta.</span><span class="sxs-lookup"><span data-stu-id="2d420-117">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="2d420-118">Dopo un breve intervallo di assenza del movimento del mouse, i controlli di trasporto sono nascosti.</span><span class="sxs-lookup"><span data-stu-id="2d420-118">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="2d420-119">Se **uiMode** è impostato su "None", non viene visualizzato alcun controllo in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="2d420-119">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="2d420-120">Per visualizzare i controlli di trasporto in modalità schermo intero, è necessario il sistema operativo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2d420-120">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

 

<span data-ttu-id="2d420-121">Se i controlli di trasporto non vengono visualizzati in modalità schermo intero, Windows Media Player esce automaticamente dalla modalità schermo intero quando la riproduzione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="2d420-121">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

## <a name="examples"></a><span data-ttu-id="2d420-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="2d420-122">Examples</span></span>

<span data-ttu-id="2d420-123">Nell'esempio seguente viene creato un pulsante che usa la proprietà fullScreen per passare un oggetto Player incorporato alla modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="2d420-123">The following example creates a button that uses the fullScreen property to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="2d420-124">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="2d420-124">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2d420-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d420-125">Requirements</span></span>



| <span data-ttu-id="2d420-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d420-126">Requirement</span></span> | <span data-ttu-id="2d420-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2d420-127">Value</span></span> |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d420-128">Versione</span><span class="sxs-lookup"><span data-stu-id="2d420-128">Version</span></span><br/>   | <span data-ttu-id="2d420-129">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2d420-129">Windows Media Player 9 Series or later</span></span><br/>                                                                  |
| <span data-ttu-id="2d420-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2d420-130">Namespace</span></span><br/> | <span data-ttu-id="2d420-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2d420-131">**AxWMPLib**</span></span><br/>                                                                                            |
| <span data-ttu-id="2d420-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="2d420-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2d420-133"><dt>AxInterop. WMPLib (AxInterop.WMPLib.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2d420-133"><dt>AxInterop.WMPLib (AxInterop.WMPLib.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d420-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d420-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d420-135">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2d420-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2d420-136">**AxWindowsMediaPlayer. uiMode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2d420-136">**AxWindowsMediaPlayer.uiMode (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





