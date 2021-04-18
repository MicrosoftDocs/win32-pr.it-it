---
title: Metodo IWMPMediaCollection getAttributeStringCollection
description: Il metodo getAttributeStringCollection restituisce un'interfaccia IWMPStringCollection che rappresenta il set di tutti i valori per un attributo specificato all'interno di un tipo di supporto.
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- Metodo getAttributeStringCollection Windows Media Player
- Metodo getAttributeStringCollection Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo getAttributeStringCollection
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAttributeStringCollection
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef25cd811890e82273fd5d634633e25e7ec460c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333645"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a><span data-ttu-id="32851-106">Metodo IWMPMediaCollection:: getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="32851-106">IWMPMediaCollection::getAttributeStringCollection method</span></span>

<span data-ttu-id="32851-107">Il metodo **getAttributeStringCollection** restituisce un'interfaccia **IWMPStringCollection** che rappresenta il set di tutti i valori per un attributo specificato all'interno di un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="32851-107">The **getAttributeStringCollection** method returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="32851-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32851-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getAttributeStringCollection(
  System.String bstrAttribute,
  System.String bstrMediaType
);
```


```VB

Public Function getAttributeStringCollection( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPStringCollection
Implements IWMPMediaCollection.getAttributeStringCollection
```





## <a name="parameters"></a><span data-ttu-id="32851-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="32851-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32851-110">*bstrAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32851-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32851-111">**System. String** che rappresenta l'attributo per il quale vengono recuperati i valori.</span><span class="sxs-lookup"><span data-stu-id="32851-111">A **System.String** that is the attribute for which the values are retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="32851-112">*bstrMediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32851-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32851-113">**System. String** che rappresenta il tipo di supporto per il quale vengono recuperati i valori.</span><span class="sxs-lookup"><span data-stu-id="32851-113">A **System.String** that is the media type for which the values are retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32851-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32851-114">Return value</span></span>

<span data-ttu-id="32851-115">Interfaccia **wmplib. IWMPStringCollection** per i valori recuperati.</span><span class="sxs-lookup"><span data-stu-id="32851-115">A **WMPLib.IWMPStringCollection** interface for the retrieved values.</span></span>

## <a name="remarks"></a><span data-ttu-id="32851-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="32851-116">Remarks</span></span>

<span data-ttu-id="32851-117">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="32851-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="32851-118">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="32851-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="32851-119">Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="32851-119">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="32851-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="32851-120">Examples</span></span>

<span data-ttu-id="32851-121">Nell'esempio seguente viene usato **getAttributeStringCollection** per visualizzare un elenco di valori che corrispondono a un particolare attributo per gli elementi audio nell'insieme di supporti.</span><span class="sxs-lookup"><span data-stu-id="32851-121">The following example uses **getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="32851-122">Una casella di riepilogo consente all'utente di selezionare un attributo, ad esempio artista, genere o album e una casella di testo a più righe Visualizza il risultato.</span><span class="sxs-lookup"><span data-stu-id="32851-122">A list box allows the user to select an attribute, such as Artist, Genre, or Album and a multi-line text box displays the result.</span></span> <span data-ttu-id="32851-123">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="32851-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void audioAttributes_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Retrieve the attribute type from the ListBox
    string attributeType = (string)((System.Windows.Forms.ListBox)sender).SelectedItem;

    // Get an interface to the mediaCollection.  
    WMPLib.IWMPMediaCollection2 library = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

    // Get an interface to the string collection for the attribute type the user selects.
    WMPLib.IWMPStringCollection2 all = (WMPLib.IWMPStringCollection2)library.getAttributeStringCollection(attributeType, "Audio");

    // Clear the text box of previous results.
    attributeValues.Clear();

    // Create an array to hold the attribute values.
    string[] attributeArray = new string[all.count];
    
    // Loop through the string collection.
    for (int i = 0; i < all.count; i++)
    {
        // Store the items in the array.
        attributeArray[i] = all.Item(i);
    }

    // Display the items in the text box.
    attributeValues.Lines = attributeArray;
}
```


```VB

Public Sub audioAttributes_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles audioAttributes.SelectedIndexChanged

    &#39; Retrieve the attribute type from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim attributeType As String = lb.SelectedItem

    &#39; Get an interface to the mediaCollection.  
    Dim library As WMPLib.IWMPMediaCollection2 = player.mediaCollection

    &#39; Get an interface to the string collection for the attribute type the user selects.
    Dim all As WMPLib.IWMPStringCollection2 = library.getAttributeStringCollection(attributeType, &quot;Audio&quot;)

    &#39; Clear the text box of previous results.
    attributeValues.Clear()

    &#39; Create an array to hold the attribute values.
    Dim attributeArray(all.count) As String

    &#39; Loop through the string collection.
    For i As Integer = 0 To (all.count - 1)

        &#39; Store the items in the array.
        attributeArray(i) = all.Item(i)

    Next i

    &#39; Display the items in the text box.
    attributeValues.Lines = attributeArray

End Sub
```





## <a name="requirements"></a><span data-ttu-id="32851-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32851-124">Requirements</span></span>



| <span data-ttu-id="32851-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="32851-125">Requirement</span></span> | <span data-ttu-id="32851-126">Valore</span><span class="sxs-lookup"><span data-stu-id="32851-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32851-127">Versione</span><span class="sxs-lookup"><span data-stu-id="32851-127">Version</span></span><br/>   | <span data-ttu-id="32851-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="32851-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="32851-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="32851-129">Namespace</span></span><br/> | <span data-ttu-id="32851-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="32851-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="32851-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="32851-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="32851-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="32851-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32851-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32851-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32851-134">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="32851-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="32851-135">**Interfaccia IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="32851-135">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





