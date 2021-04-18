---
title: Proprietà bufferingTime di IWMPNetwork
description: La proprietà bufferingTime Ottiene o imposta la quantità di tempo in millisecondi allocata per il buffering dei dati in ingresso prima che inizi la riproduzione.
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- Finestra delle proprietà di bufferingTime Media Player
- Proprietà di bufferingTime Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà bufferingTime
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8594d53797b028dd74a8ef11cb8f2fa64b3654cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324526"
---
# <a name="iwmpnetworkbufferingtime-property"></a><span data-ttu-id="3061e-106">Proprietà IWMPNetwork:: bufferingTime</span><span class="sxs-lookup"><span data-stu-id="3061e-106">IWMPNetwork::bufferingTime property</span></span>

<span data-ttu-id="3061e-107">La proprietà **bufferingTime** Ottiene o imposta la quantità di tempo in millisecondi allocata per il buffering dei dati in ingresso prima che inizi la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3061e-107">The **bufferingTime** property gets or sets the amount of time in milliseconds allocated for buffering incoming data before playback begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="3061e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3061e-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="3061e-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3061e-109">Property value</span></span>

<span data-ttu-id="3061e-110">**System. Int32** che rappresenta il tempo di memorizzazione nel buffer, in millisecondi, compreso tra 0 e 60.000 e il valore predefinito 5.000.</span><span class="sxs-lookup"><span data-stu-id="3061e-110">A **System.Int32** that is the buffering time in milliseconds, which ranges from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="3061e-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="3061e-111">Examples</span></span>

<span data-ttu-id="3061e-112">Nell'esempio di codice seguente viene usato **bufferingTime** per specificare il numero di secondi allocati per il buffering dei dati in ingresso.</span><span class="sxs-lookup"><span data-stu-id="3061e-112">The following code example uses **bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="3061e-113">Una casella di testo consente all'utente di immettere un nuovo valore per **bufferingTime** e la proprietà viene aggiornata in risposta all'evento Click di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="3061e-113">A text box allows the user to enter a new value for **bufferingTime**, and the property is updated in response to the Click event of a button.</span></span> <span data-ttu-id="3061e-114">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="3061e-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3061e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3061e-115">Requirements</span></span>



| <span data-ttu-id="3061e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3061e-116">Requirement</span></span> | <span data-ttu-id="3061e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3061e-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3061e-118">Versione</span><span class="sxs-lookup"><span data-stu-id="3061e-118">Version</span></span><br/>   | <span data-ttu-id="3061e-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3061e-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3061e-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3061e-120">Namespace</span></span><br/> | <span data-ttu-id="3061e-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3061e-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3061e-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="3061e-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3061e-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3061e-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3061e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3061e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3061e-125">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3061e-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





