---
title: SystemMonitor. LoadSettings, metodo
description: Aggiunge i contatori nel file modello HTML al monitor di sistema.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Metodo LoadSettings SysMon
- Metodo LoadSettings SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, Metodo LoadSettings
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400649"
---
# <a name="systemmonitorloadsettings-method"></a><span data-ttu-id="83240-106">SystemMonitor. LoadSettings, metodo</span><span class="sxs-lookup"><span data-stu-id="83240-106">SystemMonitor.LoadSettings method</span></span>

<span data-ttu-id="83240-107">Aggiunge i contatori nel file modello HTML al monitor di sistema.</span><span class="sxs-lookup"><span data-stu-id="83240-107">Adds the counters in the HTML template file to the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="83240-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83240-108">Syntax</span></span>


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a><span data-ttu-id="83240-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="83240-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83240-110">*SettingsFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83240-110">*SettingsFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83240-111">Stringa HTML che specifica i contatori da aggiungere al monitor di sistema.</span><span class="sxs-lookup"><span data-stu-id="83240-111">HTML string that specifies the counters to add to the System Monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83240-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83240-112">Return value</span></span>

<span data-ttu-id="83240-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="83240-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83240-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="83240-114">Remarks</span></span>

<span data-ttu-id="83240-115">Per salvare i contatori correnti nel monitor di sistema in un file HTML, chiamare il metodo [**SystemMonitor. SaveAs**](systemmonitor-saveas.md) .</span><span class="sxs-lookup"><span data-stu-id="83240-115">To save the current counters in the System Monitor to an HTML file, call the [**SystemMonitor.SaveAs**](systemmonitor-saveas.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="83240-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83240-116">Requirements</span></span>



| <span data-ttu-id="83240-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="83240-117">Requirement</span></span> | <span data-ttu-id="83240-118">Valore</span><span class="sxs-lookup"><span data-stu-id="83240-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83240-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83240-119">Minimum supported client</span></span><br/> | <span data-ttu-id="83240-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83240-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83240-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83240-121">Minimum supported server</span></span><br/> | <span data-ttu-id="83240-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="83240-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83240-123">DLL</span><span class="sxs-lookup"><span data-stu-id="83240-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83240-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="83240-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83240-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83240-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83240-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="83240-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





