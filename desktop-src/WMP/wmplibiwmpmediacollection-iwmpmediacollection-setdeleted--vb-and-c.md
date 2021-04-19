---
title: IWMPMediaCollection metodo sedeleted
description: Il metodo sedeleted sposta l'elemento multimediale specificato nella cartella degli elementi eliminati. | IWMPMediaCollection metodo sedeleted
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- Metodo sedeleted Media Player Windows
- Metodo sedeleted Media Player Windows, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo sedeleted
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ccf8cf2d36ab7e4aaf76fdbe5c28582650fcda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333400"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a><span data-ttu-id="02c3f-107">Metodo IWMPMediaCollection:: sedeleted</span><span class="sxs-lookup"><span data-stu-id="02c3f-107">IWMPMediaCollection::setDeleted method</span></span>

<span data-ttu-id="02c3f-108">Il `setDeleted` metodo sposta l'elemento multimediale specificato nella cartella degli elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="02c3f-108">The `setDeleted` method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c3f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02c3f-109">Syntax</span></span>


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a><span data-ttu-id="02c3f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="02c3f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02c3f-111">*pItem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02c3f-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02c3f-112">Interfaccia **wmplib. IWMPMedia** per l'elemento da spostare.</span><span class="sxs-lookup"><span data-stu-id="02c3f-112">A **WMPLib.IWMPMedia** interface for the item to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="02c3f-113">*varfIsDeleted* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02c3f-113">*varfIsDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02c3f-114">Valore **System. Boolean** che specifica se l'elemento deve essere spostato nella cartella degli elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="02c3f-114">A **System.Boolean** value that specifies whether the item should be moved to the deleted items folder.</span></span> <span data-ttu-id="02c3f-115">Questo valore deve essere sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="02c3f-115">This value must always be **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02c3f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02c3f-116">Return value</span></span>

<span data-ttu-id="02c3f-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="02c3f-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02c3f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="02c3f-118">Remarks</span></span>

<span data-ttu-id="02c3f-119">Questo metodo non rimuove i file dal computer dell'utente, ma li sposta nella cartella elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="02c3f-119">This method does not remove files from the user's computer, it just moves them to the deleted items folder.</span></span>

<span data-ttu-id="02c3f-120">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="02c3f-120">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="02c3f-121">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="02c3f-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="02c3f-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="02c3f-122">Examples</span></span>

<span data-ttu-id="02c3f-123">Nell'esempio seguente viene usato `setDeleted` per spostare un particolare elemento multimediale nella cartella elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="02c3f-123">The following example uses `setDeleted` to move a particular media item to the deleted items folder.</span></span> <span data-ttu-id="02c3f-124">Il metodo **undeleted** verifica prima di tutto se l'elemento è già stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="02c3f-124">The **isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="02c3f-125">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="02c3f-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="02c3f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02c3f-126">Requirements</span></span>



| <span data-ttu-id="02c3f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="02c3f-127">Requirement</span></span> | <span data-ttu-id="02c3f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="02c3f-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02c3f-129">Versione</span><span class="sxs-lookup"><span data-stu-id="02c3f-129">Version</span></span><br/>   | <span data-ttu-id="02c3f-130">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="02c3f-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="02c3f-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="02c3f-131">Namespace</span></span><br/> | <span data-ttu-id="02c3f-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="02c3f-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="02c3f-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="02c3f-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="02c3f-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="02c3f-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02c3f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02c3f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c3f-136">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="02c3f-136">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="02c3f-137">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="02c3f-137">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





