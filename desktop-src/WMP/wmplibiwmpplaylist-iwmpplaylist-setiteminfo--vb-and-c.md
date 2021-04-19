---
title: Metodo IWMPPlaylist setItemInfo
description: Il metodo setItemInfo imposta il valore di un attributo della playlist corrente.
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- Metodo setItemInfo Windows Media Player
- Metodo setItemInfo Windows Media Player, interfaccia IWMPPlaylist
- Interfaccia IWMPPlaylist Windows Media Player, metodo setItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce882d050f1ce7839fe3589fced3a87d9052fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330343"
---
# <a name="iwmpplaylistsetiteminfo-method"></a><span data-ttu-id="f0c08-106">Metodo IWMPPlaylist:: setItemInfo</span><span class="sxs-lookup"><span data-stu-id="f0c08-106">IWMPPlaylist::setItemInfo method</span></span>

<span data-ttu-id="f0c08-107">Il metodo **setItemInfo** imposta il valore di un attributo della playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="f0c08-107">The **setItemInfo** method sets the value of an attribute of the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c08-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0c08-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="f0c08-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0c08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c08-110">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0c08-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c08-111">**System. String** che rappresenta il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="f0c08-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="f0c08-112">*bstrValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0c08-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c08-113">**System. String** che corrisponde al valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="f0c08-113">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c08-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0c08-114">Return value</span></span>

<span data-ttu-id="f0c08-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f0c08-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0c08-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0c08-116">Remarks</span></span>

<span data-ttu-id="f0c08-117">Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="f0c08-117">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="f0c08-118">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f0c08-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f0c08-119">Per il codice di esempio che usa questa proprietà, vedere la proprietà [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="f0c08-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c08-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0c08-120">Requirements</span></span>



| <span data-ttu-id="f0c08-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0c08-121">Requirement</span></span> | <span data-ttu-id="f0c08-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f0c08-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c08-123">Versione</span><span class="sxs-lookup"><span data-stu-id="f0c08-123">Version</span></span><br/>   | <span data-ttu-id="f0c08-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f0c08-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f0c08-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f0c08-125">Namespace</span></span><br/> | <span data-ttu-id="f0c08-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f0c08-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f0c08-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="f0c08-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f0c08-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f0c08-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c08-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0c08-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c08-130">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f0c08-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f0c08-131">**IWMPPlaylist. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f0c08-131">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f0c08-132">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f0c08-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f0c08-133">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f0c08-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





