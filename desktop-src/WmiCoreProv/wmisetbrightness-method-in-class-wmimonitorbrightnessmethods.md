---
description: Imposta la luminosità di visualizzazione di un monitor del computer.
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: Metodo WmiSetBrightness della classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 599610b0d81de283d97ca347486c4adcbe0103dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050233"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="c16ae-103">Metodo WmiSetBrightness della classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="c16ae-103">WmiSetBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="c16ae-104">Il metodo **WmiSetBrightness** imposta la luminosità di visualizzazione di un monitor del computer.</span><span class="sxs-lookup"><span data-stu-id="c16ae-104">The **WmiSetBrightness** method sets the display brightness of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="c16ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c16ae-105">Syntax</span></span>


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="c16ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c16ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c16ae-107">*Timeout*</span><span class="sxs-lookup"><span data-stu-id="c16ae-107">*Timeout*</span></span> 
</dt> <dd>

<span data-ttu-id="c16ae-108">Timeout, in secondi.</span><span class="sxs-lookup"><span data-stu-id="c16ae-108">Timeout, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="c16ae-109">*Luminosità*</span><span class="sxs-lookup"><span data-stu-id="c16ae-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="c16ae-110">Luminosità, espressa in percentuale.</span><span class="sxs-lookup"><span data-stu-id="c16ae-110">Brightness, in percent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c16ae-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c16ae-111">Return value</span></span>

<span data-ttu-id="c16ae-112">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c16ae-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="c16ae-113">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="c16ae-113">Any other number indicates an error.</span></span> <span data-ttu-id="c16ae-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c16ae-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="c16ae-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="c16ae-115">Examples</span></span>

<span data-ttu-id="c16ae-116">Per una descrizione approfondita del recupero e dell'impostazione della luminosità del monitoraggio, vedere l'argomento relativo all' [uso di PowerShell per segnalare e impostare la luminosità](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) del monitoraggio da parte degli Scripting Guy.</span><span class="sxs-lookup"><span data-stu-id="c16ae-116">For an extended discussion of retrieving and setting monitor brightness, see the Scripting Guy's [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) blog topic.</span></span>

<span data-ttu-id="c16ae-117">Il seguente esempio di PowerShell imposta la luminosità del monitor su 50%.</span><span class="sxs-lookup"><span data-stu-id="c16ae-117">The following PowerShell sample sets the brightness of the monitor to 50%.</span></span>


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



## <a name="requirements"></a><span data-ttu-id="c16ae-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c16ae-118">Requirements</span></span>



| <span data-ttu-id="c16ae-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c16ae-119">Requirement</span></span> | <span data-ttu-id="c16ae-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c16ae-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c16ae-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c16ae-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c16ae-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c16ae-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c16ae-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c16ae-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c16ae-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c16ae-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c16ae-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c16ae-125">Namespace</span></span><br/>                | <span data-ttu-id="c16ae-126">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="c16ae-126">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="c16ae-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c16ae-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c16ae-128"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c16ae-128"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="c16ae-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c16ae-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c16ae-130"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c16ae-130"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c16ae-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c16ae-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c16ae-132">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="c16ae-132">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="c16ae-133">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="c16ae-133">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

