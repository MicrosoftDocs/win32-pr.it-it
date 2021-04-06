---
title: LogFiles. Remove (metodo)
description: Rimuove l'istanza di LogFileItem specificata dalla raccolta.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Rimuovere il metodo SysMon
- Metodo Remove SysMon, classe LogFiles
- Classe LogFiles SysMon, Remove (metodo)
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742935"
---
# <a name="logfilesremove-method"></a><span data-ttu-id="bbfb4-106">LogFiles. Remove (metodo)</span><span class="sxs-lookup"><span data-stu-id="bbfb4-106">LogFiles.Remove method</span></span>

<span data-ttu-id="bbfb4-107">Rimuove l'istanza di [**LogFileItem**](logfileitem.md) specificata dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-107">Removes the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbfb4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbfb4-108">Syntax</span></span>


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="bbfb4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbfb4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbfb4-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="bbfb4-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbfb4-111">Indice integer del file di log da rimuovere dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-111">Integer index of the log file to remove from the collection.</span></span> <span data-ttu-id="bbfb4-112">L'indice è in base uno.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbfb4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbfb4-113">Return value</span></span>

<span data-ttu-id="bbfb4-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbfb4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbfb4-115">Remarks</span></span>

<span data-ttu-id="bbfb4-116">**Prima di Windows Vista:** Non è possibile rimuovere i file di log dalla [**raccolta dei file di log**](systemmonitor-logfiles.md) se il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-116">**Prior to Windows Vista:** You cannot remove log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbfb4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbfb4-117">Requirements</span></span>



| <span data-ttu-id="bbfb4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbfb4-118">Requirement</span></span> | <span data-ttu-id="bbfb4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bbfb4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbfb4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbfb4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bbfb4-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bbfb4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bbfb4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbfb4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bbfb4-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bbfb4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbfb4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bbfb4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbfb4-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="bbfb4-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbfb4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbfb4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbfb4-127">LogFiles</span><span class="sxs-lookup"><span data-stu-id="bbfb4-127">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="bbfb4-128">**LogFileItem**</span><span class="sxs-lookup"><span data-stu-id="bbfb4-128">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="bbfb4-129">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="bbfb4-129">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





