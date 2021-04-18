---
title: Metodo IWMPMedia setItemInfo
description: Il metodo setItemInfo imposta il valore dell'attributo specificato per l'elemento multimediale.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- Metodo setItemInfo Windows Media Player
- Metodo setItemInfo Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo setItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6702c80c13090a370e2922ccecade49bc06645de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328578"
---
# <a name="iwmpmediasetiteminfo-method"></a><span data-ttu-id="14ddc-106">Metodo IWMPMedia:: setItemInfo</span><span class="sxs-lookup"><span data-stu-id="14ddc-106">IWMPMedia::setItemInfo method</span></span>

<span data-ttu-id="14ddc-107">Il metodo **setItemInfo** imposta il valore dell'attributo specificato per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="14ddc-107">The **setItemInfo** method sets the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ddc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14ddc-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="14ddc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="14ddc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14ddc-110">*bstrItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14ddc-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ddc-111">**System. String** che rappresenta il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="14ddc-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="14ddc-112">*bstrVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14ddc-112">*bstrVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ddc-113">**System. String** che rappresenta il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="14ddc-113">A **System.String** that is the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14ddc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14ddc-114">Return value</span></span>

<span data-ttu-id="14ddc-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="14ddc-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14ddc-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="14ddc-116">Remarks</span></span>

<span data-ttu-id="14ddc-117">La proprietà **attributeCount** ottiene il numero di attributi disponibili per un determinato elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="14ddc-117">The **attributeCount** property gets the number of attributes available for a given media item.</span></span> <span data-ttu-id="14ddc-118">I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare i nomi degli attributi predefiniti che possono essere usati con questo metodo.</span><span class="sxs-lookup"><span data-stu-id="14ddc-118">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="14ddc-119">Prima di utilizzare questo metodo, utilizzare il metodo **isReadOnlyItem** per individuare se è possibile impostare un particolare attributo.</span><span class="sxs-lookup"><span data-stu-id="14ddc-119">Before using this method, use the **isReadOnlyItem** method to discover whether a particular attribute can be set.</span></span>

<span data-ttu-id="14ddc-120">Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="14ddc-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="14ddc-121">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="14ddc-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="14ddc-122">Nota</span><span class="sxs-lookup"><span data-stu-id="14ddc-122">Note</span></span>

<span data-ttu-id="14ddc-123">Se si incorpora il controllo Windows Media Player nell'applicazione, gli attributi di file modificati non verranno scritti nel file multimediale digitale fino a quando l'utente non esegue Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="14ddc-123">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="14ddc-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="14ddc-124">Examples</span></span>

<span data-ttu-id="14ddc-125">Nell'esempio seguente viene usato **setItemInfo** per modificare il valore dell'attributo genre per l'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="14ddc-125">The following example uses **setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="14ddc-126">Una casella di testo consente all'utente di immettere una stringa che viene quindi usata per modificare le informazioni sugli attributi in risposta all'evento Click di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="14ddc-126">A text box allows the user to enter a string, which is then used to change the attribute information in response to the Click event of a button.</span></span> <span data-ttu-id="14ddc-127">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="14ddc-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="14ddc-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14ddc-128">Requirements</span></span>



| <span data-ttu-id="14ddc-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="14ddc-129">Requirement</span></span> | <span data-ttu-id="14ddc-130">Valore</span><span class="sxs-lookup"><span data-stu-id="14ddc-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ddc-131">Versione</span><span class="sxs-lookup"><span data-stu-id="14ddc-131">Version</span></span><br/>   | <span data-ttu-id="14ddc-132">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="14ddc-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="14ddc-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="14ddc-133">Namespace</span></span><br/> | <span data-ttu-id="14ddc-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="14ddc-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="14ddc-135">Assembly</span><span class="sxs-lookup"><span data-stu-id="14ddc-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="14ddc-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="14ddc-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14ddc-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14ddc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ddc-138">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="14ddc-138">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="14ddc-139">**IWMPMedia. attributeCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="14ddc-139">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="14ddc-140">**IWMPMedia. GetAttribute (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="14ddc-140">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="14ddc-141">**IWMPMedia. isReadOnlyItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="14ddc-141">**IWMPMedia.isReadOnlyItem (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





