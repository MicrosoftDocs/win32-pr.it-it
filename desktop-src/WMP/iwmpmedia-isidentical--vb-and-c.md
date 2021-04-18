---
title: IWMPMedia. è identico (VB e C)
description: La proprietà IsValid (il metodo Get è \_ identico in C \) ottiene un valore che indica se l'elemento multimediale specificato è uguale a quello corrente.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- Windows Media Player IWMPMedia. è identico (VB e C)
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331390"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a><span data-ttu-id="cd882-104">IWMPMedia. è identico (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="cd882-104">IWMPMedia.isIdentical (VB and C#)</span></span>

<span data-ttu-id="cd882-105">La **proprietà IsValid (il** metodo **Get è \_ identico** in C#) ottiene un valore che indica se l'elemento multimediale specificato è uguale a quello corrente.</span><span class="sxs-lookup"><span data-stu-id="cd882-105">The **isIdentical** property (the **get\_isIdentical** method in C#) gets a value indicating whether the specified media item is the same as the current one.</span></span>


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a><span data-ttu-id="cd882-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd882-106">Parameters</span></span>

<span data-ttu-id="cd882-107">*pIWMPMedia*</span><span class="sxs-lookup"><span data-stu-id="cd882-107">*pIWMPMedia*</span></span>

<span data-ttu-id="cd882-108">Interfaccia **wmplib. IWMPMedia** per l'elemento multimediale da confrontare con l'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="cd882-108">A **WMPLib.IWMPMedia** interface to the media item to be compared with the current media item.</span></span>

## <a name="property-value"></a><span data-ttu-id="cd882-109">Valore della proprietà</span><span class="sxs-lookup"><span data-stu-id="cd882-109">Property Value</span></span>

<span data-ttu-id="cd882-110">Valore **System. Boolean** che indica se i due elementi multimediali sono identici.</span><span class="sxs-lookup"><span data-stu-id="cd882-110">A **System.Boolean** value that indicates whether the two media items are identical.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd882-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd882-111">Remarks</span></span>

<span data-ttu-id="cd882-112">**IWMPMedia. is identico** è una proprietà in Visual Basic che accetta un parametro.</span><span class="sxs-lookup"><span data-stu-id="cd882-112">**IWMPMedia.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="cd882-113">In C# viene indicato come il metodo **IWMPMedia. Get è \_ identico** .</span><span class="sxs-lookup"><span data-stu-id="cd882-113">In C# it is referred to as the **IWMPMedia.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="cd882-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="cd882-114">Examples</span></span>

<span data-ttu-id="cd882-115">Nell'esempio seguente viene utilizzata **la proprietà IsValid** ( **get \_ unidential** Method in C#) per verificare se un elemento multimediale denominato newMedia è uguale all'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="cd882-115">The following example uses the **isIdentical** property (the **get\_isIdentical** method in C#) to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="cd882-116">Se non sono uguali, viene riprodotto il nuovo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="cd882-116">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="cd882-117">In caso contrario, i supporti correnti continueranno a essere riprodotti senza interruzioni.</span><span class="sxs-lookup"><span data-stu-id="cd882-117">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="cd882-118">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="cd882-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

End If
```





## <a name="requirements"></a><span data-ttu-id="cd882-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd882-119">Requirements</span></span>



| <span data-ttu-id="cd882-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd882-120">Requirement</span></span> | <span data-ttu-id="cd882-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cd882-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd882-122">Versione</span><span class="sxs-lookup"><span data-stu-id="cd882-122">Version</span></span><br/>   | <span data-ttu-id="cd882-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cd882-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cd882-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd882-124">Namespace</span></span><br/> | <span data-ttu-id="cd882-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cd882-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cd882-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="cd882-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cd882-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cd882-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd882-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd882-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd882-129">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cd882-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





