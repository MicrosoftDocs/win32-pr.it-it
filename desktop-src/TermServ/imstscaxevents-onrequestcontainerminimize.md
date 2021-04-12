---
title: Metodo IMsTscAxEvents OnRequestContainerMinimize
description: Chiamato quando l'utente preme il pulsante Riduci a icona sulla barra delle connessioni in modalità schermo intero. L'attivazione di questo evento è una richiesta che l'applicazione contenitore è ridotta a icona.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRequestContainerMinimize
- Metodo OnRequestContainerMinimize Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRequestContainerMinimize
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85387e3b156eed29dc7068eac84280be521a934e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400734"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a><span data-ttu-id="87543-107">Metodo IMsTscAxEvents:: OnRequestContainerMinimize</span><span class="sxs-lookup"><span data-stu-id="87543-107">IMsTscAxEvents::OnRequestContainerMinimize method</span></span>

<span data-ttu-id="87543-108">Chiamato quando l'utente preme il pulsante **Riduci a icona** sulla barra delle connessioni in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="87543-108">Called when the user presses the **Minimize** button on the connection bar in full-screen mode.</span></span> <span data-ttu-id="87543-109">L'attivazione di questo evento è una richiesta che l'applicazione contenitore è ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="87543-109">The firing of this event is a request that the container application minimize itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="87543-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87543-110">Syntax</span></span>


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a><span data-ttu-id="87543-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="87543-111">Parameters</span></span>

<span data-ttu-id="87543-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="87543-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87543-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87543-113">Return value</span></span>

<span data-ttu-id="87543-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="87543-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87543-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="87543-115">Remarks</span></span>

<span data-ttu-id="87543-116">Questo metodo verrà chiamato solo se la modalità a schermo intero gestita dal contenitore è abilitata. per ulteriori informazioni, vedere [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="87543-116">This method will only be called if the container-handled full-screen mode is enabled - see [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="87543-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87543-117">Requirements</span></span>



| <span data-ttu-id="87543-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="87543-118">Requirement</span></span> | <span data-ttu-id="87543-119">Valore</span><span class="sxs-lookup"><span data-stu-id="87543-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87543-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87543-120">Minimum supported client</span></span><br/> | <span data-ttu-id="87543-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87543-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="87543-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87543-122">Minimum supported server</span></span><br/> | <span data-ttu-id="87543-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87543-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="87543-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="87543-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="87543-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87543-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="87543-126">DLL</span><span class="sxs-lookup"><span data-stu-id="87543-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87543-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87543-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="87543-128">IID</span><span class="sxs-lookup"><span data-stu-id="87543-128">IID</span></span><br/>                      | <span data-ttu-id="87543-129">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="87543-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="87543-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87543-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87543-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="87543-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





