---
title: Metodo chingLock SystemMonitor.Bat
description: Blocca il monitor di sistema per impedirne il campionamento dei dati del contatore o del file di log appena aggiunto.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Metodo BatchingLock SysMon
- Metodo BatchingLock SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo BatchingLock
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301791"
---
# <a name="systemmonitorbatchinglock-method"></a><span data-ttu-id="dc540-106">Metodo chingLock SystemMonitor.Bat</span><span class="sxs-lookup"><span data-stu-id="dc540-106">SystemMonitor.BatchingLock method</span></span>

<span data-ttu-id="dc540-107">Blocca il monitor di sistema per impedirne il campionamento dei dati del contatore o del file di log appena aggiunto.</span><span class="sxs-lookup"><span data-stu-id="dc540-107">Locks the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc540-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc540-108">Syntax</span></span>


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a><span data-ttu-id="dc540-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc540-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc540-110">*blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc540-110">*lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc540-111">Impostare su true per bloccare il monitor di sistema in modo da impedire il campionamento dei dati del contatore dal nuovo contatore o dal file di log appena aggiunto.</span><span class="sxs-lookup"><span data-stu-id="dc540-111">Set to True to lock the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span> <span data-ttu-id="dc540-112">Impostare su false per rimuovere il blocco.</span><span class="sxs-lookup"><span data-stu-id="dc540-112">Set to False to remove the lock.</span></span>

</dd> <dt>

<span data-ttu-id="dc540-113">*batchReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc540-113">*batchReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc540-114">Identifica l'origine dei dati che si stanno bloccando.</span><span class="sxs-lookup"><span data-stu-id="dc540-114">Identifies the source of the data that you are locking.</span></span> <span data-ttu-id="dc540-115">Utilizzare lo stesso valore motivo per bloccare e sbloccare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="dc540-115">Use the same reason value when locking and unlocking the resource.</span></span> <span data-ttu-id="dc540-116">Per i valori possibili, vedere l'enumerazione [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) .</span><span class="sxs-lookup"><span data-stu-id="dc540-116">For possible values, see the [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc540-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc540-117">Return value</span></span>

<span data-ttu-id="dc540-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="dc540-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc540-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc540-119">Remarks</span></span>

<span data-ttu-id="dc540-120">È necessario chiamare questo metodo due volte, una volta per bloccare l'origine (true) e una volta per sbloccare l'origine (false).</span><span class="sxs-lookup"><span data-stu-id="dc540-120">You must call this method twice, once to lock the source (True) and once to unlock the source (False).</span></span>

<span data-ttu-id="dc540-121">È possibile inserire un solo blocco.</span><span class="sxs-lookup"><span data-stu-id="dc540-121">You can place only one lock.</span></span> <span data-ttu-id="dc540-122">Se ad esempio si imposta il blocco per SysmonBatchAddFiles e quindi si effettua una seconda chiamata usando SysmonBatchAddCounters come motivo, la seconda chiamata rimuove il blocco inserito dalla prima chiamata.</span><span class="sxs-lookup"><span data-stu-id="dc540-122">For example, if you set the lock for SysmonBatchAddFiles and then make a second call using SysmonBatchAddCounters as the reason, the second call removes the lock placed by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc540-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc540-123">Requirements</span></span>



| <span data-ttu-id="dc540-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc540-124">Requirement</span></span> | <span data-ttu-id="dc540-125">Valore</span><span class="sxs-lookup"><span data-stu-id="dc540-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc540-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc540-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dc540-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc540-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc540-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc540-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dc540-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc540-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc540-130">DLL</span><span class="sxs-lookup"><span data-stu-id="dc540-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc540-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="dc540-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc540-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc540-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc540-133">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="dc540-133">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





