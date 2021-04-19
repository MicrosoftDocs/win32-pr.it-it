---
title: Proprietà currentPosition di IWMPControls
description: La proprietà currentPosition Ottiene o imposta la posizione corrente nell'elemento multimediale in secondi dall'inizio.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- Finestra delle proprietà di currentPosition Media Player
- Proprietà di currentPosition Media Player Windows, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, proprietà currentPosition
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee8c2c8244d6034069f21033978ce2883ff852d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332487"
---
# <a name="iwmpcontrolscurrentposition-property"></a><span data-ttu-id="f56a5-106">Proprietà IWMPControls:: currentPosition</span><span class="sxs-lookup"><span data-stu-id="f56a5-106">IWMPControls::currentPosition property</span></span>

<span data-ttu-id="f56a5-107">La proprietà **currentPosition** Ottiene o imposta la posizione corrente nell'elemento multimediale in secondi dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="f56a5-107">The **currentPosition** property gets or sets the current position in the media item in seconds from the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="f56a5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f56a5-108">Syntax</span></span>


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a><span data-ttu-id="f56a5-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f56a5-109">Property value</span></span>

<span data-ttu-id="f56a5-110">**System. Double** che rappresenta la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="f56a5-110">A **System.Double** that is the current position.</span></span>

## <a name="examples"></a><span data-ttu-id="f56a5-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="f56a5-111">Examples</span></span>

<span data-ttu-id="f56a5-112">Nell'esempio seguente viene usato **currentPosition** per cercare una posizione fornita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f56a5-112">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="f56a5-113">In risposta a un clic del pulsante, **currentPosition** è impostato sul valore immesso in una casella di testo denominata NewPosition.</span><span class="sxs-lookup"><span data-stu-id="f56a5-113">In response to a button click, **currentPosition** is set to the value entered in a text box called newPosition.</span></span> <span data-ttu-id="f56a5-114">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="f56a5-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f56a5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f56a5-115">Requirements</span></span>



| <span data-ttu-id="f56a5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f56a5-116">Requirement</span></span> | <span data-ttu-id="f56a5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f56a5-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f56a5-118">Versione</span><span class="sxs-lookup"><span data-stu-id="f56a5-118">Version</span></span><br/>   | <span data-ttu-id="f56a5-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f56a5-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f56a5-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f56a5-120">Namespace</span></span><br/> | <span data-ttu-id="f56a5-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f56a5-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f56a5-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="f56a5-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f56a5-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f56a5-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f56a5-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f56a5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f56a5-125">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f56a5-125">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f56a5-126">**IWMPControls. currentPositionString (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f56a5-126">**IWMPControls.currentPositionString (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





