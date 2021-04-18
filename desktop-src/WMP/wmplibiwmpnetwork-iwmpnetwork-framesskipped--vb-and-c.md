---
title: Proprietà framesSkipped di IWMPNetwork
description: La proprietà framesSkipped ottiene il numero totale di frame ignorati durante la riproduzione.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- Finestra delle proprietà di framesSkipped Media Player
- Proprietà di framesSkipped Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà framesSkipped
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328282"
---
# <a name="iwmpnetworkframesskipped-property"></a><span data-ttu-id="ab1da-106">Proprietà IWMPNetwork:: framesSkipped</span><span class="sxs-lookup"><span data-stu-id="ab1da-106">IWMPNetwork::framesSkipped property</span></span>

<span data-ttu-id="ab1da-107">La proprietà **framesSkipped** ottiene il numero totale di frame ignorati durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ab1da-107">The **framesSkipped** property gets the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1da-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab1da-108">Syntax</span></span>


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="ab1da-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ab1da-109">Property value</span></span>

<span data-ttu-id="ab1da-110">**System. Int32** che rappresenta il numero di frame ignorati.</span><span class="sxs-lookup"><span data-stu-id="ab1da-110">A **System.Int32** that is the number of frames skipped.</span></span>

## <a name="examples"></a><span data-ttu-id="ab1da-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="ab1da-111">Examples</span></span>

<span data-ttu-id="ab1da-112">Nell'esempio di codice seguente viene usato **framesSkipped** per visualizzare il numero totale di frame ignorati durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ab1da-112">The following code example uses **framesSkipped** to display the total number of frames skipped during playback.</span></span> <span data-ttu-id="ab1da-113">Le informazioni vengono visualizzate in un'etichetta quando l'utente fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="ab1da-113">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="ab1da-114">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="ab1da-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="ab1da-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab1da-115">Requirements</span></span>



| <span data-ttu-id="ab1da-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab1da-116">Requirement</span></span> | <span data-ttu-id="ab1da-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ab1da-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1da-118">Versione</span><span class="sxs-lookup"><span data-stu-id="ab1da-118">Version</span></span><br/>   | <span data-ttu-id="ab1da-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ab1da-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ab1da-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ab1da-120">Namespace</span></span><br/> | <span data-ttu-id="ab1da-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ab1da-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ab1da-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="ab1da-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ab1da-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ab1da-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab1da-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab1da-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab1da-125">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ab1da-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





