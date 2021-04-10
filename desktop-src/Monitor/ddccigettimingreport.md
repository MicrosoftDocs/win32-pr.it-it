---
title: DDCCIGetTimingReport (funzione)
description: Ottiene le frequenze di sincronizzazione orizzontali e verticali di un monitoraggio.
ms.assetid: d490cb89-082a-42a1-ac0a-335c929cd5d7
keywords:
- Configurazione del monitoraggio della funzione DDCCIGetTimingReport
topic_type:
- apiref
api_name:
- DDCCIGetTimingReport
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b87cb4269c2cdff2303bbe763905cb572acfbb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964193"
---
# <a name="ddccigettimingreport-function"></a><span data-ttu-id="c6a63-104">DDCCIGetTimingReport (funzione)</span><span class="sxs-lookup"><span data-stu-id="c6a63-104">DDCCIGetTimingReport function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6a63-105">Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c6a63-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="c6a63-106">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="c6a63-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="c6a63-107">Ottiene le frequenze di sincronizzazione orizzontali e verticali di un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="c6a63-107">Gets the horizontal and vertical synchronization frequencies of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6a63-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6a63-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetTimingReport(
  _In_  HANDLE             hMonitor,
  _Out_ LPMC_TIMING_REPORT pmtr
);
```



## <a name="parameters"></a><span data-ttu-id="c6a63-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6a63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6a63-110">*hMonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6a63-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a63-111">Handle per un monitor fisico.</span><span class="sxs-lookup"><span data-stu-id="c6a63-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="c6a63-112">*PMTR* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c6a63-112">*pmtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a63-113">Un puntatore a una struttura del [**\_ \_ report temporizzato MC**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) che riceve le informazioni sull'intervallo.</span><span class="sxs-lookup"><span data-stu-id="c6a63-113">A pointer to an [**MC\_TIMING\_REPORT**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) structure that receives the timing information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6a63-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6a63-114">Return value</span></span>

<span data-ttu-id="c6a63-115">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="c6a63-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="c6a63-116">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="c6a63-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6a63-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6a63-117">Remarks</span></span>

<span data-ttu-id="c6a63-118">Le applicazioni devono chiamare [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) invece di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="c6a63-118">Applications should call [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) instead of calling this function.</span></span>

<span data-ttu-id="c6a63-119">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="c6a63-119">This function has no associated import library.</span></span> <span data-ttu-id="c6a63-120">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="c6a63-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a63-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6a63-121">Requirements</span></span>



| <span data-ttu-id="c6a63-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6a63-122">Requirement</span></span> | <span data-ttu-id="c6a63-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a63-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a63-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6a63-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c6a63-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6a63-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c6a63-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6a63-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c6a63-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6a63-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c6a63-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c6a63-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6a63-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6a63-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a63-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6a63-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a63-131">Monitorare le funzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="c6a63-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

