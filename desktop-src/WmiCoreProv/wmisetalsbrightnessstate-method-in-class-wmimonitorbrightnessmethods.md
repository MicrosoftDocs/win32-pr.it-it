---
description: Usato per controllare lo stato di luminosità del sensore di luce dell'ambiente.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Metodo WmiSetALSBrightnessState della classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 593b007f75c7eb134de4bb4c9f83c7246e9a51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319327"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="ab2c5-103">Metodo WmiSetALSBrightnessState della classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="ab2c5-103">WmiSetALSBrightnessState method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="ab2c5-104">Il metodo **WmiSetALSBrightnessState** viene usato per controllare lo stato di luminosità del sensore di luce ambientale.</span><span class="sxs-lookup"><span data-stu-id="ab2c5-104">The **WmiSetALSBrightnessState** method is used to control the ambient light sensor brightness state.</span></span> <span data-ttu-id="ab2c5-105">Se è stato stabilito un override attivo della luminosità usando il metodo [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) , tale override avrà la precedenza sul set di luminosità als usando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ab2c5-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="ab2c5-106">Per rendere effettive le sostituzioni della luminosità ALS abilitata, è necessario ripristinare i criteri di luminosità usando il metodo [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .</span><span class="sxs-lookup"><span data-stu-id="ab2c5-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab2c5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab2c5-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a><span data-ttu-id="ab2c5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab2c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab2c5-109">*State*</span><span class="sxs-lookup"><span data-stu-id="ab2c5-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="ab2c5-110">Stato di luminosità ALS.</span><span class="sxs-lookup"><span data-stu-id="ab2c5-110">ALS brightness state.</span></span> <span data-ttu-id="ab2c5-111">False disabilita l'override della luminosità ALS e true lo Abilita.</span><span class="sxs-lookup"><span data-stu-id="ab2c5-111">False disables the ALS brightness override and true enables it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab2c5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab2c5-112">Return value</span></span>

<span data-ttu-id="ab2c5-113">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ab2c5-113">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="ab2c5-114">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="ab2c5-114">Any other number indicates an error.</span></span> <span data-ttu-id="ab2c5-115">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ab2c5-115">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab2c5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab2c5-116">Requirements</span></span>



| <span data-ttu-id="ab2c5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab2c5-117">Requirement</span></span> | <span data-ttu-id="ab2c5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ab2c5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab2c5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab2c5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab2c5-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab2c5-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ab2c5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab2c5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab2c5-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab2c5-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ab2c5-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ab2c5-123">Namespace</span></span><br/>                | <span data-ttu-id="ab2c5-124">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="ab2c5-124">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="ab2c5-125">MOF</span><span class="sxs-lookup"><span data-stu-id="ab2c5-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab2c5-126"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab2c5-126"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab2c5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ab2c5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab2c5-128"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab2c5-128"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab2c5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab2c5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab2c5-130">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="ab2c5-130">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="ab2c5-131">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="ab2c5-131">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

