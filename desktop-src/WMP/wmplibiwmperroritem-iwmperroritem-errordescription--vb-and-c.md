---
title: Proprietà errorDescription di IWMPErrorItem
description: La proprietà errorDescription ottiene una descrizione dell'errore.
ms.assetid: a9914c24-1d10-422a-bcba-80be9fb85108
keywords:
- Finestra delle proprietà di errorDescription Media Player
- Proprietà di errorDescription Media Player Windows, interfaccia IWMPErrorItem
- Interfaccia IWMPErrorItem Windows Media Player, proprietà errorDescription
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8725099d1ce49eae8f378b2571dc4030f60611e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332429"
---
# <a name="iwmperroritemerrordescription-property"></a><span data-ttu-id="73083-106">Proprietà IWMPErrorItem:: errorDescription</span><span class="sxs-lookup"><span data-stu-id="73083-106">IWMPErrorItem::errorDescription property</span></span>

<span data-ttu-id="73083-107">La proprietà **errorDescription** ottiene una descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="73083-107">The **errorDescription** property gets a description of the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="73083-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73083-108">Syntax</span></span>


```CSharp
public System.String errorDescription {get; set;}
```


```VB

Public ReadOnly Property errorDescription As System.String
```





## <a name="property-value"></a><span data-ttu-id="73083-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="73083-109">Property value</span></span>

<span data-ttu-id="73083-110">**System. String** che rappresenta la descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="73083-110">A **System.String** that is the error description.</span></span>

## <a name="remarks"></a><span data-ttu-id="73083-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="73083-111">Remarks</span></span>

<span data-ttu-id="73083-112">È necessario impostare **IWMPSettings. enableErrorDialogs** su **false** se si sceglie di visualizzare i messaggi di errore personalizzati.</span><span class="sxs-lookup"><span data-stu-id="73083-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="73083-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="73083-113">Examples</span></span>

<span data-ttu-id="73083-114">Nell'esempio seguente viene usato **errorDescription** in un gestore eventi di errore per visualizzare la descrizione dell'errore all'utente.</span><span class="sxs-lookup"><span data-stu-id="73083-114">The following example uses **errorDescription** in an Error event handler to display the error description to the user.</span></span> <span data-ttu-id="73083-115">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="73083-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorDescription(object sender, System.EventArgs e)
{
    // Get the error description for the first error item.
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show("Error: " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorDescription(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error description for the first error item.
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(&quot;Error: &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="73083-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73083-116">Requirements</span></span>



| <span data-ttu-id="73083-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="73083-117">Requirement</span></span> | <span data-ttu-id="73083-118">Valore</span><span class="sxs-lookup"><span data-stu-id="73083-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73083-119">Versione</span><span class="sxs-lookup"><span data-stu-id="73083-119">Version</span></span><br/>   | <span data-ttu-id="73083-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="73083-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="73083-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="73083-121">Namespace</span></span><br/> | <span data-ttu-id="73083-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="73083-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="73083-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="73083-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="73083-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="73083-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73083-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73083-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73083-126">**Interfaccia IWMPErrorItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="73083-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="73083-127">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="73083-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





