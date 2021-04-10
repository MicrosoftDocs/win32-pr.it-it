---
description: Il metodo WmiRevertToPolicyBrightness viene usato per ripristinare la luminosità nell'impostazione dei criteri. Questo metodo non ha alcun effetto sulle impostazioni di luminosità di ALS.
ms.assetid: 9a520c3f-3563-4ef4-b397-14e487c8e8bb
title: Metodo WmiRevertToPolicyBrightness della classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiRevertToPolicyBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 03e1ed74486c7a5a2f2c61dc858e715850ec516e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232024"
---
# <a name="wmireverttopolicybrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="279b0-104">Metodo WmiRevertToPolicyBrightness della classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="279b0-104">WmiRevertToPolicyBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="279b0-105">Il metodo **WmiRevertToPolicyBrightness** viene usato per ripristinare la luminosità nell'impostazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="279b0-105">The **WmiRevertToPolicyBrightness** method is used to revert the brightness to the policy setting.</span></span> <span data-ttu-id="279b0-106">Questo metodo non ha alcun effetto sulle impostazioni di luminosità di ALS.</span><span class="sxs-lookup"><span data-stu-id="279b0-106">This method has no effect on the ALS brightness settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="279b0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="279b0-107">Syntax</span></span>


```mof
uint32 WmiRevertToPolicyBrightness();
```



## <a name="parameters"></a><span data-ttu-id="279b0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="279b0-108">Parameters</span></span>

<span data-ttu-id="279b0-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="279b0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="279b0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="279b0-110">Return value</span></span>

<span data-ttu-id="279b0-111">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="279b0-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="279b0-112">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="279b0-112">Any other number indicates an error.</span></span> <span data-ttu-id="279b0-113">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="279b0-113">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="279b0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="279b0-114">Requirements</span></span>



| <span data-ttu-id="279b0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="279b0-115">Requirement</span></span> | <span data-ttu-id="279b0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="279b0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="279b0-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="279b0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="279b0-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="279b0-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="279b0-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="279b0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="279b0-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="279b0-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="279b0-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="279b0-121">Namespace</span></span><br/>                | <span data-ttu-id="279b0-122">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="279b0-122">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="279b0-123">MOF</span><span class="sxs-lookup"><span data-stu-id="279b0-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="279b0-124"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="279b0-124"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="279b0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="279b0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="279b0-126"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="279b0-126"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="279b0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="279b0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="279b0-128">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="279b0-128">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="279b0-129">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="279b0-129">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

