---
description: Imposta lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: 'Metodo IVmApplicationHealthMonitor:: SetApplicationState'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 8e6c64ecec827f6f75f382fbca7aadf8fc0c7dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309506"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a><span data-ttu-id="b26a0-103">Metodo IVmApplicationHealthMonitor:: SetApplicationState</span><span class="sxs-lookup"><span data-stu-id="b26a0-103">IVmApplicationHealthMonitor::SetApplicationState method</span></span>

<span data-ttu-id="b26a0-104">Imposta lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b26a0-104">Sets the health state of an application that is running in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b26a0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b26a0-105">Syntax</span></span>


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a><span data-ttu-id="b26a0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b26a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b26a0-107">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b26a0-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b26a0-108">Rappresentazione **BSTR** del **GUID** che identifica l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b26a0-108">A **BSTR** representation of the **GUID** that identifies the application.</span></span> <span data-ttu-id="b26a0-109">È responsabilità dell'applicazione chiamante creare e gestire gli identificatori usati per le applicazioni monitorate.</span><span class="sxs-lookup"><span data-stu-id="b26a0-109">It is the calling application's responsibility to create and maintain the identifiers it uses for the applications being monitored.</span></span>

</dd> <dt>

<span data-ttu-id="b26a0-110">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b26a0-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b26a0-111">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b26a0-111">The display name of the application.</span></span> <span data-ttu-id="b26a0-112">Questo nome viene utilizzato in una voce del registro eventi informativa per la modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="b26a0-112">This name is used in an informational event log entry for the state change.</span></span>

</dd> <dt>

<span data-ttu-id="b26a0-113">*Stato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b26a0-113">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b26a0-114">Valore dell'enumerazione [**\_ dello stato dell'applicazione**](application-state.md) che specifica il nuovo stato di integrità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b26a0-114">A value of the [**APPLICATION\_STATE**](application-state.md) enumeration that specifies the new health state of the application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b26a0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b26a0-115">Return value</span></span>

<span data-ttu-id="b26a0-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b26a0-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b26a0-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b26a0-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b26a0-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b26a0-118">Remarks</span></span>

<span data-ttu-id="b26a0-119">Lo stato delle applicazioni in esecuzione nella macchina virtuale si riflette nel  \[ \] valore della proprietà OperationalStatus 1 della classe [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="b26a0-119">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span>

<span data-ttu-id="b26a0-120">Per utilizzare questo elemento di programmazione, è necessario installare i componenti di integrazione di Windows 8 nella macchina virtuale in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b26a0-120">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="b26a0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b26a0-121">Requirements</span></span>



| <span data-ttu-id="b26a0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b26a0-122">Requirement</span></span> | <span data-ttu-id="b26a0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b26a0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b26a0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b26a0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b26a0-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b26a0-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="b26a0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b26a0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b26a0-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b26a0-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b26a0-128">Versione</span><span class="sxs-lookup"><span data-stu-id="b26a0-128">Version</span></span><br/>                  | <span data-ttu-id="b26a0-129">Componenti di integrazione per Windows 8</span><span class="sxs-lookup"><span data-stu-id="b26a0-129">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="b26a0-130">IDL</span><span class="sxs-lookup"><span data-stu-id="b26a0-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b26a0-131"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b26a0-131"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b26a0-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b26a0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b26a0-133">**IVmApplicationHealthMonitor**</span><span class="sxs-lookup"><span data-stu-id="b26a0-133">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




