---
title: Proprietà Name di IWMPMedia
description: La proprietà Name ottiene o imposta il nome dell'elemento multimediale.
ms.assetid: d1057871-bccf-4f84-9b1d-74c41a8f7f7c
keywords:
- Proprietà nome Windows Media Player
- Proprietà nome Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, proprietà Name
topic_type:
- apiref
api_name:
- IWMPMedia.name
- IWMPMedia.get_name
- IWMPMedia.put_name
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c526fc9847b06d0f7b6f4ebadf71761fd29a9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332388"
---
# <a name="iwmpmedianame-property"></a><span data-ttu-id="b6f06-106">Proprietà IWMPMedia:: Name</span><span class="sxs-lookup"><span data-stu-id="b6f06-106">IWMPMedia::name property</span></span>

<span data-ttu-id="b6f06-107">La proprietà **Name** Ottiene o imposta il nome dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="b6f06-107">The **name** property gets or sets the name of the media item.</span></span>

<span data-ttu-id="b6f06-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b6f06-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6f06-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6f06-109">Syntax</span></span>


```CSharp
public System.String name {get; set;}
```


```VB

Public Property name As System.String
```





## <a name="property-value"></a><span data-ttu-id="b6f06-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b6f06-110">Property value</span></span>

<span data-ttu-id="b6f06-111">**System. String** che rappresenta il nome dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="b6f06-111">A **System.String** that is the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6f06-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6f06-112">Remarks</span></span>

<span data-ttu-id="b6f06-113">Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="b6f06-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="b6f06-114">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b6f06-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b6f06-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="b6f06-115">Examples</span></span>

<span data-ttu-id="b6f06-116">Nell'esempio seguente viene utilizzato **Name** per modificare il nome dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="b6f06-116">The following example uses **name** to change the name of the current media item.</span></span> <span data-ttu-id="b6f06-117">Una casella di testo consente all'utente di immettere un nuovo nome e il nome viene modificato in risposta all'evento Click di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="b6f06-117">A text box allows the user to enter a new name, and the name is changed in response to the Click event of a button.</span></span> <span data-ttu-id="b6f06-118">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="b6f06-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewName_Click(object sender, System.EventArgs e)
{
    // ...Add code to ensure that the TextBox contains a valid value.

    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Change the name. 
    cm.name = nameText.Text;
}
```


```VB

Public Sub setNewName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewName.Click

    &#39; ...Add code to ensure that the TextBox contains a valid value.

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Change the name. 
    cm.name = nameText.Text

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b6f06-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6f06-119">Requirements</span></span>



| <span data-ttu-id="b6f06-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6f06-120">Requirement</span></span> | <span data-ttu-id="b6f06-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b6f06-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f06-122">Versione</span><span class="sxs-lookup"><span data-stu-id="b6f06-122">Version</span></span><br/>   | <span data-ttu-id="b6f06-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b6f06-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b6f06-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6f06-124">Namespace</span></span><br/> | <span data-ttu-id="b6f06-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b6f06-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b6f06-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="b6f06-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b6f06-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b6f06-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6f06-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6f06-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6f06-129">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b6f06-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





