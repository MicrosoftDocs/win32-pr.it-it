---
title: Metodo IWMPMedia isReadOnlyItem
description: Il metodo isReadOnlyItem restituisce un valore che indica se è possibile modificare gli attributi dell'elemento multimediale specificato.
ms.assetid: c810c5c1-8cb9-4ac7-ac49-1ebdc86f5d7f
keywords:
- Metodo isReadOnlyItem Windows Media Player
- Metodo isReadOnlyItem Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo isReadOnlyItem
topic_type:
- apiref
api_name:
- IWMPMedia.isReadOnlyItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21d3dfefc1222832783e62962298da8bcb02b25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332390"
---
# <a name="iwmpmediaisreadonlyitem-method"></a><span data-ttu-id="8ce4d-106">Metodo IWMPMedia:: isReadOnlyItem</span><span class="sxs-lookup"><span data-stu-id="8ce4d-106">IWMPMedia::isReadOnlyItem method</span></span>

<span data-ttu-id="8ce4d-107">Il metodo **isReadOnlyItem** restituisce un valore che indica se è possibile modificare gli attributi dell'elemento multimediale specificato.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-107">The **isReadOnlyItem** method returns a value indicating whether the attributes of the specified media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ce4d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ce4d-108">Syntax</span></span>


```CSharp
public System.Boolean isReadOnlyItem(
  System.String bstrItemName
);
```


```VB

Public Function isReadOnlyItem( _
  ByVal bstrItemName As System.String _
) As System.Boolean
Implements IWMPMedia.isReadOnlyItem
```





## <a name="parameters"></a><span data-ttu-id="8ce4d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ce4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ce4d-110">*bstrItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ce4d-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ce4d-111">**System. String** che rappresenta il nome dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-111">A **System.String** that is the name of the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ce4d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ce4d-112">Return value</span></span>

<span data-ttu-id="8ce4d-113">Valore **System. Boolean** che indica se gli attributi sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-113">A **System.Boolean** value that indicates whether the attributes are read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ce4d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ce4d-114">Remarks</span></span>

<span data-ttu-id="8ce4d-115">Se un attributo è di sola lettura, non può essere impostato con il metodo **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="8ce4d-115">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="8ce4d-116">Si noti che questo metodo può restituire valori diversi per un attributo specifico se usato con versioni diverse di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-116">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="8ce4d-117">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="8ce4d-118">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8ce4d-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8ce4d-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="8ce4d-119">Examples</span></span>

<span data-ttu-id="8ce4d-120">Nell'esempio seguente viene usato **isReadOnlyItem** per inserire una casella di testo a più righe con informazioni sull'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-120">The following example uses **isReadOnlyItem** to fill a multi-line text box with information about the current media item.</span></span> <span data-ttu-id="8ce4d-121">Il codice Visualizza ogni attributo dell'elemento multimediale corrente, insieme al testo che indica se l'attributo è di sola lettura o in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-121">The code displays each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="8ce4d-122">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store a WMPLib.IWMPMedia3 interface to the current media item.
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes in the current media item.
int attCount = player.currentMedia.attributeCount;

// Create an array to store the list of attribute information.
string[] atInfo = new string[attCount];

// Create a variable to hold each attribute name.
string atName;

// Loop through the attribute list.
for (int i = 0; i < cm.attributeCount; i++)
{
    // Get the attribute name.
    atName = cm.getAttributeName(i);

    // Test whether the attribute is read-only.
    string test = ((cm.isReadOnlyItem(atName)) ? "Read-Only" : "Read/Write");

    // Store the attribute information in the array.
    atInfo[i] = (atName + " is " + test);
}

// Display the attribute information in the text box.
rwText.Lines = atInfo;
```


```VB

' Store a WMPLib.IWMPMedia3 interface to the current media item.
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes in the current media item.
Dim attCount As Integer = player.currentMedia.attributeCount

&#39; Create an array to store the list of attribute information.
Dim atInfo(attCount) As String

&#39; Create a variable to hold each attribute name.
Dim atName As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (cm.attributeCount - 1)

    &#39; Get the attribute name.
    atName = cm.getAttributeName(i)

    &#39; Test whether the attribute is read-only.
    If (cm.isReadOnlyItem(atName)) Then

        atInfo(i) = (atName + &quot; is Read-Only&quot;)

    Else

        atInfo(i) = (atName + &quot; is Read/Write&quot;)

    End If

Next i

&#39; Display the attribute information in the text box.
rwText.Lines = atInfo
```





## <a name="requirements"></a><span data-ttu-id="8ce4d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ce4d-123">Requirements</span></span>



| <span data-ttu-id="8ce4d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ce4d-124">Requirement</span></span> | <span data-ttu-id="8ce4d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8ce4d-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce4d-126">Versione</span><span class="sxs-lookup"><span data-stu-id="8ce4d-126">Version</span></span><br/>   | <span data-ttu-id="8ce4d-127">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8ce4d-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8ce4d-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8ce4d-128">Namespace</span></span><br/> | <span data-ttu-id="8ce4d-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8ce4d-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8ce4d-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="8ce4d-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8ce4d-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8ce4d-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ce4d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ce4d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ce4d-133">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8ce4d-133">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8ce4d-134">**IWMPMedia. setItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8ce4d-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





