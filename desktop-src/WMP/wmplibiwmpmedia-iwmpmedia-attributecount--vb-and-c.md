---
title: Proprietà attributeCount di IWMPMedia
description: La proprietà attributeCount ottiene il numero di attributi che è possibile sottoporre a query e/o impostare per l'elemento multimediale.
ms.assetid: 527298ff-365d-41b0-90dd-e236d6adf6fa
keywords:
- Finestra delle proprietà di attributeCount Media Player
- Proprietà di attributeCount Media Player Windows, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, proprietà attributeCount
topic_type:
- apiref
api_name:
- IWMPMedia.attributeCount
- IWMPMedia.get_attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5a56d06a54590afd315f04a90aa582f3a364db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332410"
---
# <a name="iwmpmediaattributecount-property"></a><span data-ttu-id="9a2eb-106">Proprietà IWMPMedia:: attributeCount</span><span class="sxs-lookup"><span data-stu-id="9a2eb-106">IWMPMedia::attributeCount property</span></span>

<span data-ttu-id="9a2eb-107">La proprietà **attributeCount** ottiene il numero di attributi che è possibile sottoporre a query e/o impostare per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="9a2eb-107">The **attributeCount** property gets the number of attributes that can be queried and/or set for the media item.</span></span>

<span data-ttu-id="9a2eb-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9a2eb-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a2eb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a2eb-109">Syntax</span></span>


```CSharp
public System.Int32 attributeCount {get;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="9a2eb-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9a2eb-110">Property value</span></span>

<span data-ttu-id="9a2eb-111">**System. Int32** che rappresenta il conteggio.</span><span class="sxs-lookup"><span data-stu-id="9a2eb-111">A **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a2eb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a2eb-112">Remarks</span></span>

<span data-ttu-id="9a2eb-113">Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="9a2eb-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="9a2eb-114">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9a2eb-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="9a2eb-115">Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9a2eb-115">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9a2eb-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="9a2eb-116">Examples</span></span>

<span data-ttu-id="9a2eb-117">Nell'esempio seguente viene usato **attributeCount** per determinare il numero di attributi disponibili nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="9a2eb-117">The following example uses **attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="9a2eb-118">Il codice usa tale valore per visualizzare un elenco di nomi e valori di attributi in una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="9a2eb-118">The code uses that value to display a list of attribute names and values in a text box.</span></span> <span data-ttu-id="9a2eb-119">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="9a2eb-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface to the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Store the number of attributes in the current media item using attributeCount.
int numAttributes = cm.attributeCount;

// Create strings to hold each attribute name and value.
string atName;
string atValue;

// Create an array to hold the attribute list.
string [] atList = new string[numAttributes];

// Loop through the attribute list.   
for (int i = 0; i < numAttributes; i++)
{
    // Fill the strings with the attribute information.
    atName = cm.getAttributeName(i);
    atValue = cm.getItemInfo(atName);

    // Store the attribute information in an array.
    atList[i] = (atName + ": " + atValue);
}

// Display the attribute information in the text box.
attributeList.Lines = atList;
```


```VB

' Store an IWMPMedia3 interface to the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Store the number of attributes in the current media item using attributeCount.
Dim numAttributes As Integer = cm.attributeCount

&#39; Create strings to hold each attribute name and value.
Dim atName As String
Dim atValue As String

&#39; Create an array to hold the attribute list.
Dim atList(numAttributes) As String

&#39; Loop through the attribute list.   
For i As Integer = 0 To (numAttributes - 1)

    &#39; Fill the strings with the attribute information.
    atName = cm.getAttributeName(i)
    atValue = cm.getItemInfo(atName)

    &#39; Store the attribute information in an array.
    atList(i) = (atName + &quot;: &quot; + atValue)

Next i

&#39; Display the attribute information in the text box.
attributeList.Lines = atList
```





## <a name="requirements"></a><span data-ttu-id="9a2eb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a2eb-120">Requirements</span></span>



| <span data-ttu-id="9a2eb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a2eb-121">Requirement</span></span> | <span data-ttu-id="9a2eb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9a2eb-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2eb-123">Versione</span><span class="sxs-lookup"><span data-stu-id="9a2eb-123">Version</span></span><br/>   | <span data-ttu-id="9a2eb-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9a2eb-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9a2eb-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9a2eb-125">Namespace</span></span><br/> | <span data-ttu-id="9a2eb-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9a2eb-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9a2eb-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="9a2eb-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9a2eb-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9a2eb-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a2eb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a2eb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a2eb-130">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9a2eb-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





