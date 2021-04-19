---
title: Metodo Erase IWMPCdromBurn
description: Il metodo Erase Cancella il CD corrente.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- Metodo Erase Media Player Windows
- Metodo Erase Media Player Windows, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, metodo Erase
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4e168142a6ee77081871bb7dbefa79de8031d71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329661"
---
# <a name="iwmpcdromburnerase-method"></a><span data-ttu-id="1b228-106">Metodo IWMPCdromBurn:: erase</span><span class="sxs-lookup"><span data-stu-id="1b228-106">IWMPCdromBurn::erase method</span></span>

<span data-ttu-id="1b228-107">Il metodo **Erase** Cancella il CD corrente.</span><span class="sxs-lookup"><span data-stu-id="1b228-107">The **erase** method erases the current CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b228-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b228-108">Syntax</span></span>


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a><span data-ttu-id="1b228-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b228-109">Parameters</span></span>

<span data-ttu-id="1b228-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1b228-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b228-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b228-111">Return value</span></span>

<span data-ttu-id="1b228-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1b228-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b228-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b228-113">Remarks</span></span>

<span data-ttu-id="1b228-114">Questo metodo non funzionerà se il disco nell'unità non è riscrivibile.</span><span class="sxs-lookup"><span data-stu-id="1b228-114">This method will not work if the disc in the drive is not rewritable.</span></span> <span data-ttu-id="1b228-115">Utilizzare [IWMPCdromBurn. saavailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) per determinare se è possibile cancellare un CD.</span><span class="sxs-lookup"><span data-stu-id="1b228-115">Use [IWMPCdromBurn.isAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) to determine whether a CD can be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b228-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b228-116">Requirements</span></span>



| <span data-ttu-id="1b228-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b228-117">Requirement</span></span> | <span data-ttu-id="1b228-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1b228-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b228-119">Versione</span><span class="sxs-lookup"><span data-stu-id="1b228-119">Version</span></span><br/>   | <span data-ttu-id="1b228-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="1b228-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="1b228-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1b228-121">Namespace</span></span><br/> | <span data-ttu-id="1b228-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1b228-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1b228-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="1b228-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1b228-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1b228-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b228-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b228-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b228-126">**Interfaccia IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1b228-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





