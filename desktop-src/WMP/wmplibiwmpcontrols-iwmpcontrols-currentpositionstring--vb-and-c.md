---
title: Proprietà currentPositionString di IWMPControls
description: La proprietà currentPositionString ottiene la posizione corrente nell'elemento multimediale come stringa formattata come HH MM SS (ore, minuti e secondi).
ms.assetid: cd28dafa-b6a4-4bed-aa5d-7e7be6af1426
keywords:
- Finestra delle proprietà di currentPositionString Media Player
- Proprietà di currentPositionString Media Player Windows, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, proprietà currentPositionString
topic_type:
- apiref
api_name:
- IWMPControls.currentPositionString
- IWMPControls.get_currentPositionString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e941fceb61e4f00393b05f96489ec7ac8e950f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332488"
---
# <a name="iwmpcontrolscurrentpositionstring-property"></a><span data-ttu-id="a9ec9-106">Proprietà IWMPControls:: currentPositionString</span><span class="sxs-lookup"><span data-stu-id="a9ec9-106">IWMPControls::currentPositionString property</span></span>

<span data-ttu-id="a9ec9-107">La proprietà **currentPositionString** ottiene la posizione corrente nell'elemento multimediale sotto forma di stringa in formato HH: mm: SS (ore, minuti e secondi).</span><span class="sxs-lookup"><span data-stu-id="a9ec9-107">The **currentPositionString** property gets the current position in the media item as a string formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

<span data-ttu-id="a9ec9-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a9ec9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ec9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9ec9-109">Syntax</span></span>


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a><span data-ttu-id="a9ec9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a9ec9-110">Property value</span></span>

<span data-ttu-id="a9ec9-111">**System. String** formattato che rappresenta la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a9ec9-111">A formatted **System.String** that is the current position.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9ec9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9ec9-112">Remarks</span></span>

<span data-ttu-id="a9ec9-113">Se la lunghezza dell'elemento multimediale è inferiore a un'ora, la posizione corrente viene formattata come MM: SS (minuti e secondi).</span><span class="sxs-lookup"><span data-stu-id="a9ec9-113">If the media item is less than an hour long, the current position is formatted as MM:SS (minutes and seconds).</span></span>

## <a name="examples"></a><span data-ttu-id="a9ec9-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="a9ec9-114">Examples</span></span>

<span data-ttu-id="a9ec9-115">Nell'esempio seguente viene avviato un timer che attiva un evento a intervalli di un secondo.</span><span class="sxs-lookup"><span data-stu-id="a9ec9-115">The following example starts a timer that triggers an event at one-second intervals.</span></span> <span data-ttu-id="a9ec9-116">Nel gestore dell'evento timer, un'etichetta viene aggiornata con **currentPositionString**.</span><span class="sxs-lookup"><span data-stu-id="a9ec9-116">In the timer event handler, a label is updated with the **currentPositionString**.</span></span> <span data-ttu-id="a9ec9-117">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="a9ec9-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 
   
// Update the text of the label with the currentPositionString.
private void TimerEventProcessor(object sender, System.EventArgs e)
{
    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString;
}
```


```VB

' Set the timer to fire an event every second and start the timer.
timer.Interval = 1000
timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
&#39; determine when to start and stop the timer. 

&#39; Update the text of the label with the currentPositionString.
Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a9ec9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9ec9-118">Requirements</span></span>



| <span data-ttu-id="a9ec9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ec9-119">Requirement</span></span> | <span data-ttu-id="a9ec9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a9ec9-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ec9-121">Versione</span><span class="sxs-lookup"><span data-stu-id="a9ec9-121">Version</span></span><br/>   | <span data-ttu-id="a9ec9-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a9ec9-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a9ec9-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a9ec9-123">Namespace</span></span><br/> | <span data-ttu-id="a9ec9-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a9ec9-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a9ec9-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="a9ec9-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a9ec9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a9ec9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ec9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9ec9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ec9-128">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a9ec9-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a9ec9-129">**IWMPControls. currentPosition (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a9ec9-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





