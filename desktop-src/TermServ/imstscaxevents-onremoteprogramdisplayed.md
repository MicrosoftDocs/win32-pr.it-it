---
title: Metodo IMsTscAxEvents OnRemoteProgramDisplayed
description: Chiamato quando viene visualizzato un programma RemoteApp.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRemoteProgramDisplayed
- Metodo OnRemoteProgramDisplayed Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRemoteProgramDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584e54c487ec24a3c165fdd5eb8e22f243e07f23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742111"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a><span data-ttu-id="9eb55-106">Metodo IMsTscAxEvents:: OnRemoteProgramDisplayed</span><span class="sxs-lookup"><span data-stu-id="9eb55-106">IMsTscAxEvents::OnRemoteProgramDisplayed method</span></span>

<span data-ttu-id="9eb55-107">Chiamato quando viene visualizzato un programma RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="9eb55-107">Called when a RemoteApp program is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb55-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eb55-108">Syntax</span></span>


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a><span data-ttu-id="9eb55-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9eb55-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb55-110">*vbDisplayed* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9eb55-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb55-111">Indica se il programma RemoteApp è visualizzato o nascosto.</span><span class="sxs-lookup"><span data-stu-id="9eb55-111">Indicates whether the RemoteApp program is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="9eb55-112">*uDisplayInformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9eb55-112">*uDisplayInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb55-113">Informazioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9eb55-113">The display information.</span></span>

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span data-ttu-id="9eb55-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**\_AUTORECONNECT APPDISPLAY \_ Rail**</span><span class="sxs-lookup"><span data-stu-id="9eb55-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAIL\_APPDISPLAY\_AUTORECONNECT**</span></span>


</dt> <dd>

<span data-ttu-id="9eb55-115">È in corso la riconnessione automatica.</span><span class="sxs-lookup"><span data-stu-id="9eb55-115">Automatic reconnect is in progress.</span></span>

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span data-ttu-id="9eb55-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**\_DESKTOPHOOKED APPDISPLAY \_ Rail**</span><span class="sxs-lookup"><span data-stu-id="9eb55-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAIL\_APPDISPLAY\_DESKTOPHOOKED**</span></span>


</dt> <dd>

<span data-ttu-id="9eb55-117">Il numero di RemoteApp è stato appena passato a zero.</span><span class="sxs-lookup"><span data-stu-id="9eb55-117">The RemoteApp count just went to zero.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb55-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9eb55-118">Return value</span></span>

<span data-ttu-id="9eb55-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9eb55-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb55-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="9eb55-120">Remarks</span></span>

<span data-ttu-id="9eb55-121">Implementare questo metodo nel sink di evento per ricevere una notifica che RemoteApp è stato visualizzato.</span><span class="sxs-lookup"><span data-stu-id="9eb55-121">Implement this method in your event sink to receive notification that a RemoteApp has been displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb55-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eb55-122">Requirements</span></span>



| <span data-ttu-id="9eb55-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb55-123">Requirement</span></span> | <span data-ttu-id="9eb55-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9eb55-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb55-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb55-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb55-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9eb55-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9eb55-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb55-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb55-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9eb55-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9eb55-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9eb55-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="9eb55-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb55-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9eb55-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9eb55-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eb55-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb55-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9eb55-133">IID</span><span class="sxs-lookup"><span data-stu-id="9eb55-133">IID</span></span><br/>                      | <span data-ttu-id="9eb55-134">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="9eb55-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



 

 





