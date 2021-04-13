---
title: Metodo IRemoteDesktopClientEvents OnKeyCombinationPressed
description: Chiamato quando vengono premuti combinazioni di tasti speciali nella sessione remota.
ms.assetid: 0A4EAD6C-5DA9-4ED3-BA79-92AE5AE81C9F
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnKeyCombinationPressed
- Metodo OnKeyCombinationPressed Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo OnKeyCombinationPressed
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnKeyCombinationPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cad6323578a9bde9fe38af1d2b1d2cf83473c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400440"
---
# <a name="iremotedesktopclienteventsonkeycombinationpressed-method"></a><span data-ttu-id="e27bd-106">Metodo IRemoteDesktopClientEvents:: OnKeyCombinationPressed</span><span class="sxs-lookup"><span data-stu-id="e27bd-106">IRemoteDesktopClientEvents::OnKeyCombinationPressed method</span></span>

<span data-ttu-id="e27bd-107">Chiamato quando vengono premuti combinazioni di tasti speciali nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="e27bd-107">Called when special key combinations are pressed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="e27bd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e27bd-108">Syntax</span></span>


```C++
void OnKeyCombinationPressed(
  [in] long keyCombination
);
```



## <a name="parameters"></a><span data-ttu-id="e27bd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e27bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e27bd-110">*combinazione* \[ di tasti in\]</span><span class="sxs-lookup"><span data-stu-id="e27bd-110">*keyCombination* \[in\]</span></span>
<span data-ttu-id="e27bd-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e27bd-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="e27bd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e27bd-112">Return value</span></span>

<span data-ttu-id="e27bd-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e27bd-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e27bd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e27bd-114">Requirements</span></span>



| <span data-ttu-id="e27bd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e27bd-115">Requirement</span></span> | <span data-ttu-id="e27bd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e27bd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e27bd-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e27bd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e27bd-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e27bd-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="e27bd-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e27bd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e27bd-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e27bd-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="e27bd-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e27bd-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e27bd-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e27bd-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e27bd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e27bd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e27bd-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e27bd-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e27bd-125">IID</span><span class="sxs-lookup"><span data-stu-id="e27bd-125">IID</span></span><br/>                      | <span data-ttu-id="e27bd-126">DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="e27bd-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e27bd-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e27bd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e27bd-128">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="e27bd-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





