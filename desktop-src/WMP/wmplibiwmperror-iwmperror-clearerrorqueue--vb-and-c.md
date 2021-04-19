---
title: Metodo IWMPError clearErrorQueue
description: Il metodo clearErrorQueue Cancella gli errori dalla coda degli errori. | Metodo IWMPError clearErrorQueue
ms.assetid: a8e8e666-56e4-4e75-9ed5-2714d272ce7c
keywords:
- Metodo clearErrorQueue Windows Media Player
- Metodo clearErrorQueue Windows Media Player, interfaccia IWMPError
- Interfaccia IWMPError Windows Media Player, metodo clearErrorQueue
topic_type:
- apiref
api_name:
- IWMPError.clearErrorQueue
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c3f422a9bc32049106d83c970bd8d2c9b2110f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332445"
---
# <a name="iwmperrorclearerrorqueue-method"></a><span data-ttu-id="a33f5-107">Metodo IWMPError:: clearErrorQueue</span><span class="sxs-lookup"><span data-stu-id="a33f5-107">IWMPError::clearErrorQueue method</span></span>

<span data-ttu-id="a33f5-108">Il metodo **clearErrorQueue** Cancella gli errori dalla coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="a33f5-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="a33f5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a33f5-109">Syntax</span></span>


```CSharp
public void clearErrorQueue();
```


```VB

Public Sub clearErrorQueue()
Implements IWMPError.clearErrorQueue
```





## <a name="parameters"></a><span data-ttu-id="a33f5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a33f5-110">Parameters</span></span>

<span data-ttu-id="a33f5-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a33f5-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a33f5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a33f5-112">Return value</span></span>

<span data-ttu-id="a33f5-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a33f5-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a33f5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a33f5-114">Remarks</span></span>

<span data-ttu-id="a33f5-115">Utilizzare questo metodo per cancellare la coda degli errori dopo l'elaborazione di una serie di errori.</span><span class="sxs-lookup"><span data-stu-id="a33f5-115">Use this method to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="a33f5-116">È necessario impostare **IWMPSettings. enableErrorDialogs** su **false** se si sceglie di visualizzare i messaggi di errore personalizzati.</span><span class="sxs-lookup"><span data-stu-id="a33f5-116">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="a33f5-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="a33f5-117">Examples</span></span>

<span data-ttu-id="a33f5-118">Nell'esempio seguente viene usato **clearErrorQueue** in un gestore eventi di errore per svuotare la coda degli errori dopo la visualizzazione di tutte le descrizioni degli errori.</span><span class="sxs-lookup"><span data-stu-id="a33f5-118">The following example uses **clearErrorQueue** in an Error event handler to empty the error queue after all error descriptions have been displayed.</span></span> <span data-ttu-id="a33f5-119">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="a33f5-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_clearErrorQueue(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Loop through the list of errors.
    for (int i = 0; i < max; i++)
    {
        // Get the description for this error.
        string errDesc = player.Error.get_Item(i).errorDescription;

        // Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc);
    }

    // Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue();
}
```


```VB

Public Sub player_ErrorEvent_clearErrorQueue(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Loop through the list of errors.
    For i As Integer = 0 To (max - 1)

        &#39; Get the description for this error.
        Dim errDesc As String = player.Error.Item(i).errorDescription

        &#39; Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc)

    Next i

    &#39; Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a33f5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a33f5-120">Requirements</span></span>



| <span data-ttu-id="a33f5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33f5-121">Requirement</span></span> | <span data-ttu-id="a33f5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a33f5-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a33f5-123">Versione</span><span class="sxs-lookup"><span data-stu-id="a33f5-123">Version</span></span><br/>   | <span data-ttu-id="a33f5-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a33f5-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a33f5-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a33f5-125">Namespace</span></span><br/> | <span data-ttu-id="a33f5-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a33f5-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a33f5-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="a33f5-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a33f5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a33f5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a33f5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a33f5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33f5-130">**Interfaccia IWMPError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a33f5-130">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a33f5-131">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a33f5-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





