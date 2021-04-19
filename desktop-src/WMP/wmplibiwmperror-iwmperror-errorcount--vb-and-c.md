---
title: Proprietà errorCount di IWMPError
description: La proprietà errorCount ottiene il numero di errori nella coda degli errori.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- Finestra delle proprietà di errorCount Media Player
- Proprietà di errorCount Media Player Windows, interfaccia IWMPError
- Interfaccia IWMPError Windows Media Player, proprietà errorCount
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332436"
---
# <a name="iwmperrorerrorcount-property"></a><span data-ttu-id="6dd04-106">Proprietà IWMPError:: errorCount</span><span class="sxs-lookup"><span data-stu-id="6dd04-106">IWMPError::errorCount property</span></span>

<span data-ttu-id="6dd04-107">La proprietà **ErrorCount** ottiene il numero di errori nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="6dd04-107">The **errorCount** property gets the number of errors in the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd04-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6dd04-108">Syntax</span></span>


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="6dd04-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6dd04-109">Property value</span></span>

<span data-ttu-id="6dd04-110">**System. Int32** che rappresenta il numero di errori.</span><span class="sxs-lookup"><span data-stu-id="6dd04-110">A **System.Int32** that is the number of errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dd04-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6dd04-111">Remarks</span></span>

<span data-ttu-id="6dd04-112">È necessario impostare **IWMPSettings. enableErrorDialogs** su **false** se si sceglie di visualizzare i messaggi di errore personalizzati.</span><span class="sxs-lookup"><span data-stu-id="6dd04-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="6dd04-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="6dd04-113">Examples</span></span>

<span data-ttu-id="6dd04-114">Nell'esempio seguente viene usato **ErrorCount** in un gestore eventi di errore per avvisare l'utente dell'errore più recente nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="6dd04-114">The following example uses **errorCount** in an Error event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="6dd04-115">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="6dd04-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6dd04-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6dd04-116">Requirements</span></span>



| <span data-ttu-id="6dd04-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dd04-117">Requirement</span></span> | <span data-ttu-id="6dd04-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6dd04-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd04-119">Versione</span><span class="sxs-lookup"><span data-stu-id="6dd04-119">Version</span></span><br/>   | <span data-ttu-id="6dd04-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6dd04-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6dd04-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6dd04-121">Namespace</span></span><br/> | <span data-ttu-id="6dd04-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6dd04-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6dd04-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="6dd04-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6dd04-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6dd04-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dd04-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6dd04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dd04-126">**Interfaccia IWMPError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6dd04-126">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6dd04-127">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6dd04-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





