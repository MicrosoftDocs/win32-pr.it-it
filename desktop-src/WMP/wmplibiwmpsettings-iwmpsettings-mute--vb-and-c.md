---
title: Proprietà mute di IWMPSettings
description: La proprietà mute Ottiene o imposta un valore che indica se l'audio è disattivato.
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- Disattiva Media Player proprietà di Windows
- Proprietà mute Media Player di Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà mute
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67518bb9a6eccee13e4cc262f37341d30689439e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333907"
---
# <a name="iwmpsettingsmute-property"></a><span data-ttu-id="a3fe3-106">Proprietà IWMPSettings:: mute</span><span class="sxs-lookup"><span data-stu-id="a3fe3-106">IWMPSettings::mute property</span></span>

<span data-ttu-id="a3fe3-107">La proprietà **mute** Ottiene o imposta un valore che indica se l'audio è disattivato.</span><span class="sxs-lookup"><span data-stu-id="a3fe3-107">The **mute** property gets or sets a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3fe3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3fe3-108">Syntax</span></span>


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="a3fe3-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a3fe3-109">Property value</span></span>

<span data-ttu-id="a3fe3-110">Valore **System. Boolean** che indica se l'audio è disattivato.</span><span class="sxs-lookup"><span data-stu-id="a3fe3-110">A **System.Boolean** value indicating whether audio is muted.</span></span> <span data-ttu-id="a3fe3-111">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="a3fe3-111">The default is **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="a3fe3-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="a3fe3-112">Examples</span></span>

<span data-ttu-id="a3fe3-113">Nell'esempio seguente viene creata una casella di controllo e la proprietà **mute** viene attivata o disattivata per disattivare l'audio quando viene modificato lo stato di selezione della casella.</span><span class="sxs-lookup"><span data-stu-id="a3fe3-113">The following example creates a check box, and toggles the **mute** property to mute and un-mute audio when the checked state of the box is changed.</span></span> <span data-ttu-id="a3fe3-114">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="a3fe3-114">**AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a3fe3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3fe3-115">Requirements</span></span>



| <span data-ttu-id="a3fe3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3fe3-116">Requirement</span></span> | <span data-ttu-id="a3fe3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a3fe3-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3fe3-118">Versione</span><span class="sxs-lookup"><span data-stu-id="a3fe3-118">Version</span></span><br/>   | <span data-ttu-id="a3fe3-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a3fe3-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a3fe3-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a3fe3-120">Namespace</span></span><br/> | <span data-ttu-id="a3fe3-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a3fe3-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a3fe3-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="a3fe3-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a3fe3-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a3fe3-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3fe3-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3fe3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3fe3-125">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a3fe3-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a3fe3-126">**IWMPSettings. rate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a3fe3-126">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





