---
title: Proprietà errorCode IWMPErrorItem
description: La proprietà errorCode ottiene il codice di errore corrente.
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- Proprietà errorCode Media Player di Windows
- Proprietà errorCode Media Player Windows, interfaccia IWMPErrorItem
- Interfaccia IWMPErrorItem Windows Media Player, proprietà errorCode
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f284d5655fc1f4007695a1f681c744a9c5c6fc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332431"
---
# <a name="iwmperroritemerrorcode-property"></a><span data-ttu-id="2cf62-106">Proprietà IWMPErrorItem:: errorCode</span><span class="sxs-lookup"><span data-stu-id="2cf62-106">IWMPErrorItem::errorCode property</span></span>

<span data-ttu-id="2cf62-107">La proprietà **ErrorCode** ottiene il codice di errore corrente.</span><span class="sxs-lookup"><span data-stu-id="2cf62-107">The **errorCode** property gets the current error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf62-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cf62-108">Syntax</span></span>


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="2cf62-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2cf62-109">Property value</span></span>

<span data-ttu-id="2cf62-110">**System. Int32** che rappresenta il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="2cf62-110">A **System.Int32** that is the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cf62-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cf62-111">Remarks</span></span>

<span data-ttu-id="2cf62-112">È necessario impostare **IWMPSettings. enableErrorDialogs** su **false** se si sceglie di visualizzare i messaggi di errore personalizzati.</span><span class="sxs-lookup"><span data-stu-id="2cf62-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="2cf62-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="2cf62-113">Examples</span></span>

<span data-ttu-id="2cf62-114">Nell'esempio seguente viene utilizzato **ErrorCode** in un gestore eventi di errore per visualizzare il codice di errore all'utente.</span><span class="sxs-lookup"><span data-stu-id="2cf62-114">The following example uses **errorCode** in an Error event handler to display the error code to the user.</span></span> <span data-ttu-id="2cf62-115">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="2cf62-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2cf62-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cf62-116">Requirements</span></span>



| <span data-ttu-id="2cf62-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cf62-117">Requirement</span></span> | <span data-ttu-id="2cf62-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2cf62-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf62-119">Versione</span><span class="sxs-lookup"><span data-stu-id="2cf62-119">Version</span></span><br/>   | <span data-ttu-id="2cf62-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2cf62-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2cf62-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2cf62-121">Namespace</span></span><br/> | <span data-ttu-id="2cf62-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2cf62-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2cf62-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="2cf62-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2cf62-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2cf62-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cf62-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cf62-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf62-126">**Interfaccia IWMPErrorItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2cf62-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2cf62-127">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2cf62-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





