---
title: Metodo precedente IWMPControls
description: Il metodo precedente imposta l'elemento precedente nella playlist come elemento corrente.
ms.assetid: 380524f5-e8b6-45c4-9f6c-3dbb49b1ac9f
keywords:
- Metodo precedente Media Player Windows
- Metodo precedente Media Player Windows, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo precedente
topic_type:
- apiref
api_name:
- IWMPControls.previous
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823038205a026afb7141491f562698eb60515a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332470"
---
# <a name="iwmpcontrolsprevious-method"></a><span data-ttu-id="b8c53-106">IWMPControls::p metodo reambiguo</span><span class="sxs-lookup"><span data-stu-id="b8c53-106">IWMPControls::previous method</span></span>

<span data-ttu-id="b8c53-107">Il metodo **precedente** imposta l'elemento precedente nella playlist come elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="b8c53-107">The **previous** method sets the previous item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8c53-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8c53-108">Syntax</span></span>


```CSharp
public void previous();
```


```VB

Public Sub previous()
Implements IWMPControls.previous
```





## <a name="parameters"></a><span data-ttu-id="b8c53-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8c53-109">Parameters</span></span>

<span data-ttu-id="b8c53-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b8c53-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8c53-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8c53-111">Return value</span></span>

<span data-ttu-id="b8c53-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b8c53-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8c53-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8c53-113">Remarks</span></span>

<span data-ttu-id="b8c53-114">Se la playlist si trova nella prima voce quando viene richiamato il **precedente** , l'ultima voce nella playlist diventerà quella corrente.</span><span class="sxs-lookup"><span data-stu-id="b8c53-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="b8c53-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="b8c53-115">Examples</span></span>

<span data-ttu-id="b8c53-116">Nell'esempio seguente viene usato **Previous** per passare all'elemento precedente nella playlist corrente in risposta all'evento Click di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="b8c53-116">The following example uses **previous** to move to the previous item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="b8c53-117">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="b8c53-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void previousButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("previous"))
    {
        controls.previous();
    }
}
```


```VB

Public Sub previousButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles previousButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;previous&quot;)) Then

        controls.previous()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b8c53-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8c53-118">Requirements</span></span>



| <span data-ttu-id="b8c53-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8c53-119">Requirement</span></span> | <span data-ttu-id="b8c53-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c53-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c53-121">Versione</span><span class="sxs-lookup"><span data-stu-id="b8c53-121">Version</span></span><br/>   | <span data-ttu-id="b8c53-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b8c53-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b8c53-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b8c53-123">Namespace</span></span><br/> | <span data-ttu-id="b8c53-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b8c53-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b8c53-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="b8c53-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b8c53-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b8c53-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8c53-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8c53-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8c53-128">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b8c53-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8c53-129">**IWMPControls. Next (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b8c53-129">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8c53-130">**IWMPControls. Stop (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b8c53-130">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





