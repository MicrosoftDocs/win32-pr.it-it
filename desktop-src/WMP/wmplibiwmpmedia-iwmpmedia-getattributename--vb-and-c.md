---
title: Metodo GetAttribute IWMPMedia
description: Il metodo GetAttribute restituisce il nome dell'attributo corrispondente all'indice specificato.
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- Metodo GetAttributeName Windows Media Player
- Metodo GetAttributeName Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo GetAttribute
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb40ef8c0c984258dc11dd00c80807db2f4eb64a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332407"
---
# <a name="iwmpmediagetattributename-method"></a><span data-ttu-id="21ba3-106">Metodo IWMPMedia:: GetAttribute</span><span class="sxs-lookup"><span data-stu-id="21ba3-106">IWMPMedia::getAttributeName method</span></span>

<span data-ttu-id="21ba3-107">Il metodo **GetAttribute** restituisce il nome dell'attributo corrispondente all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="21ba3-107">The **getAttributeName** method returns the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="21ba3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21ba3-108">Syntax</span></span>


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a><span data-ttu-id="21ba3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="21ba3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21ba3-110">*lIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21ba3-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21ba3-111">**System. Int32** che rappresenta l'indice.</span><span class="sxs-lookup"><span data-stu-id="21ba3-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21ba3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21ba3-112">Return value</span></span>

<span data-ttu-id="21ba3-113">**System. String** che rappresenta il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="21ba3-113">A **System.String** that is the attribute name.</span></span>

## <a name="remarks"></a><span data-ttu-id="21ba3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="21ba3-114">Remarks</span></span>

<span data-ttu-id="21ba3-115">Il nome dell'attributo restituito può essere utilizzato insieme a **GetItemInfo** per recuperare il valore per un attributo denominato specifico.</span><span class="sxs-lookup"><span data-stu-id="21ba3-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="21ba3-116">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="21ba3-116">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="21ba3-117">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="21ba3-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="21ba3-118">Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="21ba3-118">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="21ba3-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="21ba3-119">Examples</span></span>

<span data-ttu-id="21ba3-120">Nell'esempio seguente viene utilizzato **GetAttribute** per compilare una casella di testo a più righe con l'indice e il nome di ogni attributo per l'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="21ba3-120">The following example uses **getAttributeName** to fill a multi-line text box with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="21ba3-121">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="21ba3-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
```





## <a name="requirements"></a><span data-ttu-id="21ba3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21ba3-122">Requirements</span></span>



| <span data-ttu-id="21ba3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="21ba3-123">Requirement</span></span> | <span data-ttu-id="21ba3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="21ba3-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21ba3-125">Versione</span><span class="sxs-lookup"><span data-stu-id="21ba3-125">Version</span></span><br/>   | <span data-ttu-id="21ba3-126">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="21ba3-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="21ba3-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21ba3-127">Namespace</span></span><br/> | <span data-ttu-id="21ba3-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="21ba3-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="21ba3-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="21ba3-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="21ba3-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="21ba3-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21ba3-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21ba3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ba3-132">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="21ba3-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="21ba3-133">**IWMPMedia. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="21ba3-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





