---
title: Metodo IWMPStringCollection2 getAttributeCountByType
description: Il metodo getAttributeCountByType restituisce il numero di attributi associati all'indice della raccolta di stringhe, al nome dell'attributo e alla lingua specificati.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- Metodo getAttributeCountByType Windows Media Player
- Metodo getAttributeCountByType Windows Media Player, interfaccia IWMPStringCollection2
- Interfaccia IWMPStringCollection2 Windows Media Player, metodo getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bb60fdd843fb3f45b6e4e3aff444a8a915fa0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331730"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a><span data-ttu-id="3b89c-106">Metodo IWMPStringCollection2:: getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="3b89c-106">IWMPStringCollection2::getAttributeCountByType method</span></span>

<span data-ttu-id="3b89c-107">Il metodo **getAttributeCountByType** restituisce il numero di attributi associati all'indice della raccolta di stringhe, al nome dell'attributo e alla lingua specificati.</span><span class="sxs-lookup"><span data-stu-id="3b89c-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified string collection index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b89c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b89c-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="3b89c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b89c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b89c-110">*lCollectionIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b89c-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b89c-111">**System. Int32** che specifica l'indice in base zero dell'elemento della raccolta di stringhe da cui ottenere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="3b89c-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="3b89c-112">*bstrType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b89c-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b89c-113">**System. String** che rappresenta il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="3b89c-113">The **System.String** that is the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="3b89c-114">*bstrLanguage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b89c-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b89c-115">**System. String** che rappresenta il nome della lingua.</span><span class="sxs-lookup"><span data-stu-id="3b89c-115">The **System.String** that is the name of the language.</span></span> <span data-ttu-id="3b89c-116">Se il valore è impostato su null o su una stringa di lunghezza zero (""), viene utilizzata la stringa delle impostazioni locali corrente.</span><span class="sxs-lookup"><span data-stu-id="3b89c-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="3b89c-117">In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".</span><span class="sxs-lookup"><span data-stu-id="3b89c-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b89c-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b89c-118">Return value</span></span>

<span data-ttu-id="3b89c-119">**System. Int32** che rappresenta il conteggio.</span><span class="sxs-lookup"><span data-stu-id="3b89c-119">The **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b89c-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b89c-120">Remarks</span></span>

<span data-ttu-id="3b89c-121">Questo metodo viene utilizzato per individuare il numero di attributi corrispondente a un nome di attributo specifico per un determinato elemento **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="3b89c-121">This method is used to discover the number of attributes corresponding to a particular attribute name for a given **StringCollection** item.</span></span> <span data-ttu-id="3b89c-122">I numeri di indice possono quindi essere passati al quarto parametro del metodo **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="3b89c-122">Index numbers can then be passed to the fourth parameter of the **getItemInfoByType** method.</span></span>

<span data-ttu-id="3b89c-123">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="3b89c-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3b89c-124">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3b89c-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b89c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b89c-125">Requirements</span></span>



| <span data-ttu-id="3b89c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b89c-126">Requirement</span></span> | <span data-ttu-id="3b89c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3b89c-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b89c-128">Versione</span><span class="sxs-lookup"><span data-stu-id="3b89c-128">Version</span></span><br/>   | <span data-ttu-id="3b89c-129">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="3b89c-129">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="3b89c-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3b89c-130">Namespace</span></span><br/> | <span data-ttu-id="3b89c-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3b89c-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3b89c-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="3b89c-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3b89c-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3b89c-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b89c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b89c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b89c-135">**Interfaccia IWMPStringCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b89c-135">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b89c-136">**IWMPStringCollection2. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3b89c-136">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





