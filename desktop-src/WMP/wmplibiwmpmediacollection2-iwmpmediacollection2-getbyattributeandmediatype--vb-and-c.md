---
title: Metodo IWMPMediaCollection2 getByAttributeAndMediaType
description: Il metodo getByAttributeAndMediaType restituisce un'interfaccia IWMPPlaylist che fornisce l'accesso agli elementi multimediali con un attributo e un tipo di supporto specificati.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- Metodo getByAttributeAndMediaType Windows Media Player
- Metodo getByAttributeAndMediaType Windows Media Player, interfaccia IWMPMediaCollection2
- Interfaccia IWMPMediaCollection2 Windows Media Player, metodo getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333394"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a><span data-ttu-id="00bd6-106">Metodo IWMPMediaCollection2:: getByAttributeAndMediaType</span><span class="sxs-lookup"><span data-stu-id="00bd6-106">IWMPMediaCollection2::getByAttributeAndMediaType method</span></span>

<span data-ttu-id="00bd6-107">Il `getByAttributeAndMediaType` metodo restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali con un attributo e un tipo di supporto specificati.</span><span class="sxs-lookup"><span data-stu-id="00bd6-107">The `getByAttributeAndMediaType` method returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="00bd6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00bd6-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a><span data-ttu-id="00bd6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="00bd6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00bd6-110">*bstrAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00bd6-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00bd6-111">**System. String** che rappresenta l'attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="00bd6-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="00bd6-112">*bstrValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00bd6-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00bd6-113">**System. String** che corrisponde al valore specificato per l'attributo specificato in *bstrAttribute*.</span><span class="sxs-lookup"><span data-stu-id="00bd6-113">The **System.String** that is the specified value for the attribute that is specified in *bstrAttribute*.</span></span>

</dd> <dt>

<span data-ttu-id="00bd6-114">*bstrMediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00bd6-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00bd6-115">**System. String** che rappresenta il tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="00bd6-115">The **System.String** that is the specified media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00bd6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00bd6-116">Return value</span></span>

<span data-ttu-id="00bd6-117">Interfaccia **wmplib. IWMPPlaylist** per la playlist recuperata.</span><span class="sxs-lookup"><span data-stu-id="00bd6-117">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="00bd6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00bd6-118">Requirements</span></span>



| <span data-ttu-id="00bd6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="00bd6-119">Requirement</span></span> | <span data-ttu-id="00bd6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="00bd6-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00bd6-121">Versione</span><span class="sxs-lookup"><span data-stu-id="00bd6-121">Version</span></span><br/>   | <span data-ttu-id="00bd6-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="00bd6-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="00bd6-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="00bd6-123">Namespace</span></span><br/> | <span data-ttu-id="00bd6-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="00bd6-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="00bd6-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="00bd6-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="00bd6-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="00bd6-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00bd6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00bd6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00bd6-128">**Interfaccia IWMPMediaCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="00bd6-128">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="00bd6-129">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="00bd6-129">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





