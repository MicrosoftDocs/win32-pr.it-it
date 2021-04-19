---
title: Metodo IWMPCdromBurn getItemInfo
description: Il metodo getItemInfo Recupera il valore dell'attributo specificato per il CD.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, metodo getItemInfo
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329659"
---
# <a name="iwmpcdromburngetiteminfo-method"></a><span data-ttu-id="7ab69-106">Metodo IWMPCdromBurn:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="7ab69-106">IWMPCdromBurn::getItemInfo method</span></span>

<span data-ttu-id="7ab69-107">Il metodo **GetItemInfo** Recupera il valore dell'attributo specificato per il CD.</span><span class="sxs-lookup"><span data-stu-id="7ab69-107">The **getItemInfo** method retrieves the value of the specified attribute for the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ab69-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ab69-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="7ab69-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ab69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ab69-110">*bstrItem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ab69-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ab69-111">**System. String** che contiene uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ab69-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="7ab69-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7ab69-112">Value</span></span>         | <span data-ttu-id="7ab69-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ab69-113">Description</span></span>                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab69-114">Availabletime disponibile</span><span class="sxs-lookup"><span data-stu-id="7ab69-114">AvailableTime</span></span> | <span data-ttu-id="7ab69-115">Recupera l'ora disponibile sul CD, in secondi.</span><span class="sxs-lookup"><span data-stu-id="7ab69-115">Retrieves the time available on the CD, in seconds.</span></span>                                          |
| <span data-ttu-id="7ab69-116">Vuoto</span><span class="sxs-lookup"><span data-stu-id="7ab69-116">Blank</span></span>         | <span data-ttu-id="7ab69-117">Recupera un oggetto **System. Boolean** (rappresentato come stringa) che indica se il CD è vuoto.</span><span class="sxs-lookup"><span data-stu-id="7ab69-117">Retrieves a **System.Boolean** (represented as a string) indicating whether the CD is blank.</span></span> |
| <span data-ttu-id="7ab69-118">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="7ab69-118">FreeSpace</span></span>     | <span data-ttu-id="7ab69-119">Recupera lo spazio disponibile sul CD, in byte.</span><span class="sxs-lookup"><span data-stu-id="7ab69-119">Retrieves the free space on the CD, in bytes.</span></span>                                                |
| <span data-ttu-id="7ab69-120">TotalSpace</span><span class="sxs-lookup"><span data-stu-id="7ab69-120">TotalSpace</span></span>    | <span data-ttu-id="7ab69-121">Recupera lo spazio totale del CD, in byte.</span><span class="sxs-lookup"><span data-stu-id="7ab69-121">Retrieves the total space on the CD, in bytes.</span></span>                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ab69-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ab69-122">Return value</span></span>

<span data-ttu-id="7ab69-123">**System. String** che corrisponde al valore dell'attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="7ab69-123">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ab69-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ab69-124">Requirements</span></span>



| <span data-ttu-id="7ab69-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ab69-125">Requirement</span></span> | <span data-ttu-id="7ab69-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7ab69-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab69-127">Versione</span><span class="sxs-lookup"><span data-stu-id="7ab69-127">Version</span></span><br/>   | <span data-ttu-id="7ab69-128">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="7ab69-128">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="7ab69-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7ab69-129">Namespace</span></span><br/> | <span data-ttu-id="7ab69-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7ab69-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7ab69-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="7ab69-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7ab69-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7ab69-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ab69-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ab69-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab69-134">**Interfaccia IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7ab69-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





