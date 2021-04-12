---
description: Usato per impostare il valore di luminosità del sensore di luce di ambiente.
ms.assetid: 8b3ec692-4043-42b3-8dd6-7a147620e382
title: Metodo WmiSetALSBrightness della classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 0768917f9197b6ee3de52877e031acbbdc8f9aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234163"
---
# <a name="wmisetalsbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="44863-103">Metodo WmiSetALSBrightness della classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="44863-103">WmiSetALSBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="44863-104">Il metodo **WmiSetALSBrightness** viene usato per impostare il valore di luminosità del sensore di luce di ambiente.</span><span class="sxs-lookup"><span data-stu-id="44863-104">The **WmiSetALSBrightness** method is used to set the ambient light sensor brightness value.</span></span> <span data-ttu-id="44863-105">Se è stato stabilito un override attivo della luminosità usando il metodo [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) , tale override avrà la precedenza sul set di luminosità als usando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="44863-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="44863-106">Per rendere effettive le sostituzioni della luminosità ALS abilitata, è necessario ripristinare i criteri di luminosità usando il metodo [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .</span><span class="sxs-lookup"><span data-stu-id="44863-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="44863-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44863-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightness(
   uint8 Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="44863-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="44863-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44863-109">*Luminosità*</span><span class="sxs-lookup"><span data-stu-id="44863-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="44863-110">Luminosità del ALS come percentuale.</span><span class="sxs-lookup"><span data-stu-id="44863-110">The ALS brightness as a percentage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44863-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44863-111">Return value</span></span>

<span data-ttu-id="44863-112">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="44863-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="44863-113">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="44863-113">Any other number indicates an error.</span></span> <span data-ttu-id="44863-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="44863-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="44863-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44863-115">Requirements</span></span>



| <span data-ttu-id="44863-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44863-116">Requirement</span></span> | <span data-ttu-id="44863-117">Valore</span><span class="sxs-lookup"><span data-stu-id="44863-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44863-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44863-118">Minimum supported client</span></span><br/> | <span data-ttu-id="44863-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44863-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="44863-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44863-120">Minimum supported server</span></span><br/> | <span data-ttu-id="44863-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44863-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="44863-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="44863-122">Namespace</span></span><br/>                | <span data-ttu-id="44863-123">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="44863-123">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="44863-124">MOF</span><span class="sxs-lookup"><span data-stu-id="44863-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44863-125"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44863-125"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="44863-126">DLL</span><span class="sxs-lookup"><span data-stu-id="44863-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44863-127"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44863-127"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44863-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44863-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44863-129">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="44863-129">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="44863-130">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="44863-130">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

