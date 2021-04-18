---
title: Metodo IMsTscAxEvents OnIdleTimeoutNotification
description: Chiamato quando l'utente non dispone di input del mouse o della tastiera durante il periodo di tempo impostato dal metodo IMsRdpClientAdvancedSettings put \_ MinutesToIdleTimeout.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnIdleTimeoutNotification
- Metodo OnIdleTimeoutNotification Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnIdleTimeoutNotification
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e305b0ed22e733053e33451aa35d3b8f8d6c138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301878"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a><span data-ttu-id="7c19b-106">Metodo IMsTscAxEvents:: OnIdleTimeoutNotification</span><span class="sxs-lookup"><span data-stu-id="7c19b-106">IMsTscAxEvents::OnIdleTimeoutNotification method</span></span>

<span data-ttu-id="7c19b-107">Chiamato quando l'utente non dispone di input del mouse o della tastiera durante il periodo di tempo impostato dal metodo [**IMsRdpClientAdvancedSettings::p UT \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="7c19b-107">Called when there has been no mouse or keyboard input by the user during the period of time set by the [**IMsRdpClientAdvancedSettings::put\_MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c19b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c19b-108">Syntax</span></span>


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a><span data-ttu-id="7c19b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c19b-109">Parameters</span></span>

<span data-ttu-id="7c19b-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7c19b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c19b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c19b-111">Return value</span></span>

<span data-ttu-id="7c19b-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7c19b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c19b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c19b-113">Remarks</span></span>

<span data-ttu-id="7c19b-114">Per impostazione predefinita, il valore della proprietà [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) è impostato su zero e il sistema non monitora i timeout di inattività.</span><span class="sxs-lookup"><span data-stu-id="7c19b-114">By default, the value of the [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) property is set to zero and the system does not monitor for idle time-outs.</span></span> <span data-ttu-id="7c19b-115">Questo evento si verifica solo se la proprietà è impostata su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="7c19b-115">This event occurs only if the property is set to a nonzero value.</span></span>

<span data-ttu-id="7c19b-116">Il valore di [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) viene reimpostato automaticamente ogni volta che si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="7c19b-116">The value of [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) is automatically reset each time the event occurs.</span></span>

<span data-ttu-id="7c19b-117">Le applicazioni possono utilizzare [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in situazioni in cui è utile disconnettere un utente. ad esempio, in un chiosco multimediale o in un altro scenario di terminale pubblico.</span><span class="sxs-lookup"><span data-stu-id="7c19b-117">Applications can use [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in situations where it is useful to disconnect a user; for example, in a kiosk or other public terminal scenario.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c19b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c19b-118">Requirements</span></span>



| <span data-ttu-id="7c19b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c19b-119">Requirement</span></span> | <span data-ttu-id="7c19b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7c19b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c19b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c19b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7c19b-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c19b-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7c19b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c19b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7c19b-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c19b-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7c19b-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7c19b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c19b-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c19b-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c19b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7c19b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c19b-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c19b-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c19b-129">IID</span><span class="sxs-lookup"><span data-stu-id="7c19b-129">IID</span></span><br/>                      | <span data-ttu-id="7c19b-130">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="7c19b-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="7c19b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c19b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c19b-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="7c19b-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





