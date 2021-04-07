---
title: DDCCIGetVCPFeature (funzione)
description: Ottiene il valore corrente, il valore massimo e il tipo di codice di un codice del pannello di controllo virtuale (VCP) per un monitoraggio.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Configurazione del monitoraggio della funzione DDCCIGetVCPFeature
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5758bbd1c86b9f228b64063fdd05c04cb05bedcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964192"
---
# <a name="ddccigetvcpfeature-function"></a><span data-ttu-id="b97eb-104">DDCCIGetVCPFeature (funzione)</span><span class="sxs-lookup"><span data-stu-id="b97eb-104">DDCCIGetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b97eb-105">Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b97eb-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="b97eb-106">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b97eb-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="b97eb-107">Ottiene il valore corrente, il valore massimo e il tipo di codice di un codice del pannello di controllo virtuale (VCP) per un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b97eb-107">Gets the current value, maximum value, and code type of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="b97eb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b97eb-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
);
```



## <a name="parameters"></a><span data-ttu-id="b97eb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b97eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b97eb-110">*hMonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b97eb-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b97eb-111">Handle per un monitor fisico.</span><span class="sxs-lookup"><span data-stu-id="b97eb-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b97eb-112">*dwVCPCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b97eb-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b97eb-113">Codice VCP per la query.</span><span class="sxs-lookup"><span data-stu-id="b97eb-113">The VCP code to query.</span></span>

</dd> <dt>

<span data-ttu-id="b97eb-114">*pvct* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b97eb-114">*pvct* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b97eb-115">Riceve il tipo di codice VCP come membro dell'enumerazione del [**\_ tipo di \_ codice \_ MC VCP**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) .</span><span class="sxs-lookup"><span data-stu-id="b97eb-115">Receives the VCP code type, as a member of the [**MC\_VCP\_CODE\_TYPE**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="b97eb-116">*pdwCurrentValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b97eb-116">*pdwCurrentValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b97eb-117">Riceve il valore corrente del codice VCP.</span><span class="sxs-lookup"><span data-stu-id="b97eb-117">Receives the current value of the VCP code.</span></span>

</dd> <dt>

<span data-ttu-id="b97eb-118">*pdwMaximumValue* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b97eb-118">*pdwMaximumValue* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b97eb-119">Riceve il valore massimo del codice VCP.</span><span class="sxs-lookup"><span data-stu-id="b97eb-119">Receives the maximum value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b97eb-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b97eb-120">Return value</span></span>

<span data-ttu-id="b97eb-121">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="b97eb-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="b97eb-122">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="b97eb-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b97eb-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="b97eb-123">Remarks</span></span>

<span data-ttu-id="b97eb-124">Le applicazioni devono chiamare [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) invece di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b97eb-124">Applications should call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) instead of calling this function.</span></span>

<span data-ttu-id="b97eb-125">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="b97eb-125">This function has no associated import library.</span></span> <span data-ttu-id="b97eb-126">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="b97eb-126">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="b97eb-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b97eb-127">Requirements</span></span>



| <span data-ttu-id="b97eb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b97eb-128">Requirement</span></span> | <span data-ttu-id="b97eb-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b97eb-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b97eb-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b97eb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b97eb-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b97eb-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b97eb-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b97eb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b97eb-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b97eb-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b97eb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b97eb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b97eb-135"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b97eb-135"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b97eb-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b97eb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b97eb-137">Monitorare le funzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="b97eb-137">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

