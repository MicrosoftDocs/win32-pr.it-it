---
title: IWMPError. Item (VB e C)
description: La proprietà Item (il \_ metodo Get Item in C \) ottiene un'interfaccia IWMPErrorItem in corrispondenza dell'indice specificato nella coda degli errori.
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- IWMPError. Item (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9217ec772512171c828dd0dad06ec8fe3704dba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328881"
---
# <a name="iwmperroritem-vb-and-c"></a><span data-ttu-id="4f85d-104">IWMPError. Item (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="4f85d-104">IWMPError.Item (VB and C#)</span></span>

<span data-ttu-id="4f85d-105">La proprietà **Item** (il metodo **get \_ Item** in C#) ottiene un'interfaccia **IWMPErrorItem** in corrispondenza dell'indice specificato nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="4f85d-105">The **Item** property (the **get\_Item** method in C#) gets an **IWMPErrorItem** interface at the specified index in the error queue.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="4f85d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f85d-106">Parameters</span></span>

<span data-ttu-id="4f85d-107">*dwIndex*</span><span class="sxs-lookup"><span data-stu-id="4f85d-107">*dwIndex*</span></span>

<span data-ttu-id="4f85d-108">**System. Int32** che rappresenta l'indice in base zero di un'interfaccia **IWMPErrorItem** nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="4f85d-108">A **System.Int32** that is the zero-based index of an **IWMPErrorItem** interface in the error queue.</span></span>

## <a name="property-value"></a><span data-ttu-id="4f85d-109">Valore della proprietà</span><span class="sxs-lookup"><span data-stu-id="4f85d-109">Property Value</span></span>

<span data-ttu-id="4f85d-110">Interfaccia **wmplib. IWMPErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="4f85d-110">A **WMPLib.IWMPErrorItem** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f85d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f85d-111">Remarks</span></span>

<span data-ttu-id="4f85d-112">Windows Media Player può generare un certo numero di errori in risposta a una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="4f85d-112">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="4f85d-113">Questa proprietà ottiene un errore specifico nella coda usando un numero di indice.</span><span class="sxs-lookup"><span data-stu-id="4f85d-113">This property gets a specific error in the queue by using an index number.</span></span> <span data-ttu-id="4f85d-114">I numeri di indice per la coda degli errori iniziano con zero.</span><span class="sxs-lookup"><span data-stu-id="4f85d-114">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="4f85d-115">È necessario impostare **IWMPSettings. enableErrorDialogs** su **false** se si sceglie di visualizzare i messaggi di errore personalizzati.</span><span class="sxs-lookup"><span data-stu-id="4f85d-115">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="4f85d-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="4f85d-116">Examples</span></span>

<span data-ttu-id="4f85d-117">Nell'esempio seguente viene usata la proprietà **Item** (il metodo **get \_ Item** in C#) in un gestore eventi di errore per recuperare e visualizzare informazioni sull'errore più recente nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="4f85d-117">The following example uses the **Item** property (the **get\_Item** method in C#) in an Error event handler to retrieve and display information about the most recent error in the error queue.</span></span> <span data-ttu-id="4f85d-118">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="4f85d-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4f85d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f85d-119">Requirements</span></span>



| <span data-ttu-id="4f85d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f85d-120">Requirement</span></span> | <span data-ttu-id="4f85d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4f85d-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f85d-122">Versione</span><span class="sxs-lookup"><span data-stu-id="4f85d-122">Version</span></span><br/>   | <span data-ttu-id="4f85d-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="4f85d-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4f85d-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f85d-124">Namespace</span></span><br/> | <span data-ttu-id="4f85d-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4f85d-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4f85d-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="4f85d-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4f85d-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4f85d-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f85d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f85d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f85d-129">**Interfaccia IWMPError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4f85d-129">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4f85d-130">**Interfaccia IWMPErrorItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4f85d-130">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4f85d-131">**IWMPSettings. enableErrorDialogs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4f85d-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





