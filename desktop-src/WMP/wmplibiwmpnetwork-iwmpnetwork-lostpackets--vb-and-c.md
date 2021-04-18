---
title: Proprietà lostPackets di IWMPNetwork
description: La proprietà lostPackets ottiene il numero di pacchetti persi.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- Finestra delle proprietà di lostPackets Media Player
- Proprietà di lostPackets Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà lostPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1adac5f4aa8b1f58c023a556af04b8eae4bd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329912"
---
# <a name="iwmpnetworklostpackets-property"></a><span data-ttu-id="03f73-106">Proprietà IWMPNetwork:: lostPackets</span><span class="sxs-lookup"><span data-stu-id="03f73-106">IWMPNetwork::lostPackets property</span></span>

<span data-ttu-id="03f73-107">La proprietà **lostPackets** ottiene il numero di pacchetti persi.</span><span class="sxs-lookup"><span data-stu-id="03f73-107">The **lostPackets** property gets the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="03f73-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03f73-108">Syntax</span></span>


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="03f73-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="03f73-109">Property value</span></span>

<span data-ttu-id="03f73-110">**System. Int32** che rappresenta il numero di pacchetti persi.</span><span class="sxs-lookup"><span data-stu-id="03f73-110">A **System.Int32** that is the number of lost packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="03f73-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="03f73-111">Remarks</span></span>

<span data-ttu-id="03f73-112">Questa proprietà include solo i pacchetti per flussi multimediali e restituisce zero quando si usa il protocollo HTTP, che è senza perdita di contenuti.</span><span class="sxs-lookup"><span data-stu-id="03f73-112">This property includes streaming media packets only, and will return zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="03f73-113">I pacchetti possono essere persi per diversi motivi, ad esempio il tipo e la qualità della connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="03f73-113">Packets can be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="03f73-114">Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene reimpostata su zero.</span><span class="sxs-lookup"><span data-stu-id="03f73-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="03f73-115">Il valore non viene reimpostato se la riproduzione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="03f73-115">The value is not reset if playback is paused.</span></span> <span data-ttu-id="03f73-116">Questa proprietà ottiene informazioni valide solo in fase di esecuzione quando l'URL per la riproduzione viene impostato tramite la proprietà **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="03f73-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="03f73-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="03f73-117">Examples</span></span>

<span data-ttu-id="03f73-118">Nell'esempio di codice seguente viene usato **lostPackets** per visualizzare il numero totale di pacchetti persi durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="03f73-118">The following code example uses **lostPackets** to display the total number of packets lost during playback.</span></span> <span data-ttu-id="03f73-119">Le informazioni vengono visualizzate in un'etichetta quando l'utente fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="03f73-119">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="03f73-120">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="03f73-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="03f73-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03f73-121">Requirements</span></span>



| <span data-ttu-id="03f73-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="03f73-122">Requirement</span></span> | <span data-ttu-id="03f73-123">Valore</span><span class="sxs-lookup"><span data-stu-id="03f73-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03f73-124">Versione</span><span class="sxs-lookup"><span data-stu-id="03f73-124">Version</span></span><br/>   | <span data-ttu-id="03f73-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="03f73-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="03f73-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03f73-126">Namespace</span></span><br/> | <span data-ttu-id="03f73-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="03f73-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="03f73-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="03f73-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="03f73-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="03f73-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f73-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03f73-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f73-131">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="03f73-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="03f73-132">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="03f73-132">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





