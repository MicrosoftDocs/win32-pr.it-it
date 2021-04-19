---
title: Metodo IWMPLibraryServices getCountByType
description: Il metodo getCountByType restituisce il conteggio delle librerie disponibili di un tipo specificato.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- Metodo getCountByType Windows Media Player
- Metodo getCountByType Windows Media Player, interfaccia IWMPLibraryServices
- Interfaccia IWMPLibraryServices Windows Media Player, metodo getCountByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332413"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a><span data-ttu-id="d2ae2-106">Metodo IWMPLibraryServices:: getCountByType</span><span class="sxs-lookup"><span data-stu-id="d2ae2-106">IWMPLibraryServices::getCountByType method</span></span>

<span data-ttu-id="d2ae2-107">Il metodo **getCountByType** restituisce il conteggio delle librerie disponibili di un tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="d2ae2-107">The **getCountByType** method returns the count of available libraries of a specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ae2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2ae2-108">Syntax</span></span>


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a><span data-ttu-id="d2ae2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2ae2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ae2-110">*wmplt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2ae2-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ae2-111">Valore dell'enumerazione **wmplib. WMPLibraryType** che specifica il tipo di libreria da contare.</span><span class="sxs-lookup"><span data-stu-id="d2ae2-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ae2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2ae2-112">Return value</span></span>

<span data-ttu-id="d2ae2-113">**System. Int32** che rappresenta il conteggio delle librerie.</span><span class="sxs-lookup"><span data-stu-id="d2ae2-113">A **System.Int32** that is the library count.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ae2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2ae2-114">Requirements</span></span>



| <span data-ttu-id="d2ae2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2ae2-115">Requirement</span></span> | <span data-ttu-id="d2ae2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d2ae2-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ae2-117">Versione</span><span class="sxs-lookup"><span data-stu-id="d2ae2-117">Version</span></span><br/>   | <span data-ttu-id="d2ae2-118">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="d2ae2-118">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="d2ae2-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2ae2-119">Namespace</span></span><br/> | <span data-ttu-id="d2ae2-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d2ae2-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d2ae2-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="d2ae2-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d2ae2-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d2ae2-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2ae2-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2ae2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ae2-124">**Interfaccia IWMPLibraryServices (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d2ae2-124">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d2ae2-125">**WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="d2ae2-125">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





