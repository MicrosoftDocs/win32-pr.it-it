---
title: DDCCISetVCPFeature (funzione)
description: Imposta il valore di un codice del pannello di controllo virtuale (VCP) per un monitoraggio.
ms.assetid: 1069588b-5f8a-49da-b857-6f0a0c737a11
keywords:
- Configurazione del monitoraggio della funzione DDCCISetVCPFeature
topic_type:
- apiref
api_name:
- DDCCISetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a72da2b2540c73e023a753a3fdb28507f8cbb40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119707"
---
# <a name="ddccisetvcpfeature-function"></a><span data-ttu-id="35692-104">DDCCISetVCPFeature (funzione)</span><span class="sxs-lookup"><span data-stu-id="35692-104">DDCCISetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35692-105">Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="35692-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="35692-106">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="35692-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="35692-107">Imposta il valore di un codice del pannello di controllo virtuale (VCP) per un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="35692-107">Sets the value of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="35692-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35692-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISetVCPFeature(
  _In_ HANDLE hMonitor,
  _In_ DWORD  dwVCPCode,
  _In_ DWORD  dwNewValue
);
```



## <a name="parameters"></a><span data-ttu-id="35692-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="35692-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35692-110">*hMonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35692-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35692-111">Handle per un monitor fisico.</span><span class="sxs-lookup"><span data-stu-id="35692-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="35692-112">*dwVCPCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35692-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35692-113">Codice VCP da impostare.</span><span class="sxs-lookup"><span data-stu-id="35692-113">The VCP code to set.</span></span>

</dd> <dt>

<span data-ttu-id="35692-114">*dwNewValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35692-114">*dwNewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35692-115">Valore del codice VCP.</span><span class="sxs-lookup"><span data-stu-id="35692-115">The value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35692-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35692-116">Return value</span></span>

<span data-ttu-id="35692-117">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="35692-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="35692-118">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="35692-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="35692-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="35692-119">Remarks</span></span>

<span data-ttu-id="35692-120">Le applicazioni devono chiamare [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) invece di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="35692-120">Applications should call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) instead of calling this function.</span></span>

<span data-ttu-id="35692-121">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="35692-121">This function has no associated import library.</span></span> <span data-ttu-id="35692-122">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="35692-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="35692-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35692-123">Requirements</span></span>



| <span data-ttu-id="35692-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="35692-124">Requirement</span></span> | <span data-ttu-id="35692-125">Valore</span><span class="sxs-lookup"><span data-stu-id="35692-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35692-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35692-126">Minimum supported client</span></span><br/> | <span data-ttu-id="35692-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35692-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="35692-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35692-128">Minimum supported server</span></span><br/> | <span data-ttu-id="35692-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35692-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="35692-130">DLL</span><span class="sxs-lookup"><span data-stu-id="35692-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35692-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35692-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35692-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35692-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35692-133">Monitorare le funzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="35692-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

