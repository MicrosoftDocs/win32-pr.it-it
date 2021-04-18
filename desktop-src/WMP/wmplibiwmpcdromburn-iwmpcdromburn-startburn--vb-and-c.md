---
title: Metodo IWMPCdromBurn startBurn
description: Il metodo startBurn brucia il CD.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- Metodo startBurn Windows Media Player
- Metodo startBurn Windows Media Player, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, metodo startBurn
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe185d8993286e4be3935b43f6c1e9757623309d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329654"
---
# <a name="iwmpcdromburnstartburn-method"></a><span data-ttu-id="caf2c-106">Metodo IWMPCdromBurn:: startBurn</span><span class="sxs-lookup"><span data-stu-id="caf2c-106">IWMPCdromBurn::startBurn method</span></span>

<span data-ttu-id="caf2c-107">Il metodo **startBurn** brucia il CD.</span><span class="sxs-lookup"><span data-stu-id="caf2c-107">The **startBurn** method burns the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="caf2c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="caf2c-108">Syntax</span></span>


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a><span data-ttu-id="caf2c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="caf2c-109">Parameters</span></span>

<span data-ttu-id="caf2c-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="caf2c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="caf2c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="caf2c-111">Return value</span></span>

<span data-ttu-id="caf2c-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="caf2c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="caf2c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="caf2c-113">Remarks</span></span>

<span data-ttu-id="caf2c-114">Prima di chiamare questo metodo, il valore di **burnstate** deve essere WmpbsReady o wmpbsStopped.</span><span class="sxs-lookup"><span data-stu-id="caf2c-114">The value of **burnstate** should be wmpbsReady or wmpbsStopped before calling this method.</span></span>

<span data-ttu-id="caf2c-115">Questo metodo non funzionerà se l'unità CD non è un masterizzatore o se il disco nell'unità non è scrivibile.</span><span class="sxs-lookup"><span data-stu-id="caf2c-115">This method will not work if the CD drive is not a burner, or if the disc in the drive is not writable.</span></span> <span data-ttu-id="caf2c-116">Utilizzare **l'** oggetto per determinare se è possibile masterizzare un CD.</span><span class="sxs-lookup"><span data-stu-id="caf2c-116">Use **isAvailable** to determine whether a CD can be burned.</span></span>

## <a name="requirements"></a><span data-ttu-id="caf2c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="caf2c-117">Requirements</span></span>



| <span data-ttu-id="caf2c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="caf2c-118">Requirement</span></span> | <span data-ttu-id="caf2c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="caf2c-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf2c-120">Versione</span><span class="sxs-lookup"><span data-stu-id="caf2c-120">Version</span></span><br/>   | <span data-ttu-id="caf2c-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="caf2c-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="caf2c-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="caf2c-122">Namespace</span></span><br/> | <span data-ttu-id="caf2c-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="caf2c-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="caf2c-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="caf2c-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="caf2c-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="caf2c-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caf2c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="caf2c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf2c-127">**Interfaccia IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="caf2c-127">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="caf2c-128">**IWMPCdromBurn. burnState (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="caf2c-128">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="caf2c-129">**IWMPCdromBurn. disavailable (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="caf2c-129">**IWMPCdromBurn.isAvailable (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="caf2c-130">**IWMPCdromBurn. stopBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="caf2c-130">**IWMPCdromBurn.stopBurn (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





