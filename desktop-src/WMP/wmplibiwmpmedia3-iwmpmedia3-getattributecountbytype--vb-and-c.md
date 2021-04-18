---
title: Metodo IWMPMedia3 getAttributeCountByType
description: Il metodo getAttributeCountByType restituisce il numero di attributi associati al tipo di attributo specificato.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- Metodo getAttributeCountByType Windows Media Player
- Metodo getAttributeCountByType Windows Media Player, interfaccia IWMPMedia3
- Interfaccia IWMPMedia3 Windows Media Player, metodo getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324369"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a><span data-ttu-id="f547e-106">Metodo IWMPMedia3:: getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="f547e-106">IWMPMedia3::getAttributeCountByType method</span></span>

<span data-ttu-id="f547e-107">Il metodo **getAttributeCountByType** restituisce il numero di attributi associati al tipo di attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="f547e-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified attribute type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f547e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f547e-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="f547e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f547e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f547e-110">*bstrType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f547e-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f547e-111">**System. String** che rappresenta il tipo di attributo.</span><span class="sxs-lookup"><span data-stu-id="f547e-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="f547e-112">*bstrLanguage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f547e-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f547e-113">**System. String** che rappresenta il linguaggio.</span><span class="sxs-lookup"><span data-stu-id="f547e-113">A **System.String** that is the language.</span></span> <span data-ttu-id="f547e-114">Se il valore è impostato su null o su una stringa di lunghezza zero (""), viene utilizzata la stringa delle impostazioni locali corrente.</span><span class="sxs-lookup"><span data-stu-id="f547e-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="f547e-115">In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".</span><span class="sxs-lookup"><span data-stu-id="f547e-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f547e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f547e-116">Return value</span></span>

<span data-ttu-id="f547e-117">**System. Int32** che rappresenta il numero di attributi associati al tipo.</span><span class="sxs-lookup"><span data-stu-id="f547e-117">A **System.Int32** that is the count of attributes that are associated with the type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f547e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f547e-118">Remarks</span></span>

<span data-ttu-id="f547e-119">Questo metodo viene utilizzato per individuare il numero di attributi corrispondente a un nome di attributo specifico per un determinato elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="f547e-119">This method is used to discover the number of attributes corresponding to a particular attribute name for a given media item.</span></span> <span data-ttu-id="f547e-120">I numeri di indice possono quindi essere passati al metodo **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="f547e-120">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="f547e-121">Questa operazione è utile, ad esempio, quando un elemento multimediale è stato categorizzato in più generi.</span><span class="sxs-lookup"><span data-stu-id="f547e-121">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="f547e-122">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="f547e-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="f547e-123">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f547e-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f547e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f547e-124">Requirements</span></span>



| <span data-ttu-id="f547e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f547e-125">Requirement</span></span> | <span data-ttu-id="f547e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f547e-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f547e-127">Versione</span><span class="sxs-lookup"><span data-stu-id="f547e-127">Version</span></span><br/>   | <span data-ttu-id="f547e-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f547e-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f547e-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f547e-129">Namespace</span></span><br/> | <span data-ttu-id="f547e-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f547e-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f547e-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="f547e-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f547e-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f547e-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f547e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f547e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f547e-134">**Interfaccia IWMPMedia3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f547e-134">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f547e-135">**IWMPMedia3. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f547e-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





