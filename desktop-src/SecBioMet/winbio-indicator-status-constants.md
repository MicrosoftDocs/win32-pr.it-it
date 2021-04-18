---
title: Costanti WINBIO_INDICATOR_STATUS (tipi WinBio \_ . h)
description: Imposta la luce di un indicatore.
ms.assetid: 1e00ff9d-6693-4763-8ac3-b42d2a3e987d
topic_type:
- apiref
api_name:
- WINBIO_INDICATOR_ON
- WINBIO_INDICATOR_OFF
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7693fbd2b9b37067738774d172f4bb482edb06e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302752"
---
# <a name="winbio_indicator_status-constants"></a><span data-ttu-id="fc7fa-103">Costanti di stato dell' \_ indicatore WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="fc7fa-103">WINBIO\_INDICATOR\_STATUS Constants</span></span>

<span data-ttu-id="fc7fa-104">Per impostare la luce di un indicatore, è possibile utilizzare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fc7fa-104">The following values can be used to set an indicator light.</span></span> <span data-ttu-id="fc7fa-105">Per impostazione predefinita, i sensori non avranno una luce accesa, ma le applicazioni possono usare questi valori per abilitare o disabilitare gli indicatori luminosi.</span><span class="sxs-lookup"><span data-stu-id="fc7fa-105">By default, sensors will not have a light on, but applications can use these values to enable or disable indicator lights.</span></span> <span data-ttu-id="fc7fa-106">Il valore di **\_ \_ stato del sensore WINBIO** fornisce maggiori dettagli sullo stato di una luce indicatore accesa.</span><span class="sxs-lookup"><span data-stu-id="fc7fa-106">The **WINBIO\_SENSOR\_STATUS** value provides more detail about the status of an indicator light that is on.</span></span> <span data-ttu-id="fc7fa-107">Per ulteriori informazioni, vedere le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc7fa-107">For more information, see the following functions:</span></span>

-   [<span data-ttu-id="fc7fa-108">**SensorAdapterSetIndicatorStatus**</span><span class="sxs-lookup"><span data-stu-id="fc7fa-108">**SensorAdapterSetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [<span data-ttu-id="fc7fa-109">**SensorAdapterGetIndicatorStatus**</span><span class="sxs-lookup"><span data-stu-id="fc7fa-109">**SensorAdapterGetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [<span data-ttu-id="fc7fa-110">**SensorAdapterQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="fc7fa-110">**SensorAdapterQueryStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| <span data-ttu-id="fc7fa-111">Costante</span><span class="sxs-lookup"><span data-stu-id="fc7fa-111">Constant</span></span>                                                                                                                                                                            | <span data-ttu-id="fc7fa-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc7fa-112">Description</span></span>                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <span data-ttu-id="fc7fa-113"><dt>**\_indicatore WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc7fa-113"><dt>**WINBIO\_INDICATOR\_ON**</dt></span></span> </dl>    | <span data-ttu-id="fc7fa-114">La luce dell'indicatore del sensore è accesa.</span><span class="sxs-lookup"><span data-stu-id="fc7fa-114">The sensor indicator light is on.</span></span><br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <span data-ttu-id="fc7fa-115"><dt>**\_indicatore WINBIO \_ disattivato**</dt></span><span class="sxs-lookup"><span data-stu-id="fc7fa-115"><dt>**WINBIO\_INDICATOR\_OFF**</dt></span></span> </dl> | <span data-ttu-id="fc7fa-116">La luce dell'indicatore del sensore è disattivata.</span><span class="sxs-lookup"><span data-stu-id="fc7fa-116">The sensor indicator light is off.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fc7fa-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc7fa-117">Requirements</span></span>



| <span data-ttu-id="fc7fa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc7fa-118">Requirement</span></span> | <span data-ttu-id="fc7fa-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fc7fa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc7fa-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc7fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fc7fa-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fc7fa-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="fc7fa-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc7fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fc7fa-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc7fa-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fc7fa-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc7fa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc7fa-125"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc7fa-125"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc7fa-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc7fa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc7fa-127">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="fc7fa-127">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





