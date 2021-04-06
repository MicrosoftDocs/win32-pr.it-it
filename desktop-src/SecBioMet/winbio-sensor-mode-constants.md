---
title: Costanti WINBIO_SENSOR_MODE (tipi WinBio \_ . h)
description: Impostare la modalità adattatore del sensore.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743671"
---
# <a name="winbio_sensor_mode-constants"></a><span data-ttu-id="ed864-103">\_Costanti della \_ modalità sensore WINBIO</span><span class="sxs-lookup"><span data-stu-id="ed864-103">WINBIO\_SENSOR\_MODE Constants</span></span>

<span data-ttu-id="ed864-104">I valori seguenti vengono usati nella funzione [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) per impostare la modalità adattatore del sensore.</span><span class="sxs-lookup"><span data-stu-id="ed864-104">The following values are used in the [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) function to set the sensor adapter mode.</span></span>



| <span data-ttu-id="ed864-105">Costante</span><span class="sxs-lookup"><span data-stu-id="ed864-105">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="ed864-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed864-106">Description</span></span>                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <span data-ttu-id="ed864-107"><dt>**\_ \_ modalità sconosciuta del sensore WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed864-107"><dt>**WINBIO\_SENSOR\_UNKNOWN\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="ed864-108">La modalità operativa non è nota.</span><span class="sxs-lookup"><span data-stu-id="ed864-108">The operating mode is not known.</span></span><br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <span data-ttu-id="ed864-109"><dt>**\_modalità di \_ base del sensore WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed864-109"><dt>**WINBIO\_SENSOR\_BASIC\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="ed864-110">Usare il sensore in modalità di base.</span><span class="sxs-lookup"><span data-stu-id="ed864-110">Operate the sensor in basic mode.</span></span> <span data-ttu-id="ed864-111">Il sensore funge solo da dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="ed864-111">The sensor acts only as a capture device.</span></span> <span data-ttu-id="ed864-112">Non vengono usate le funzionalità di elaborazione onboarding o di archiviazione esistenti.</span><span class="sxs-lookup"><span data-stu-id="ed864-112">Any onboard processing or storage capabilities that exist are not used.</span></span><br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <span data-ttu-id="ed864-113"><dt>**\_ \_ modalità avanzata del sensore WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed864-113"><dt>**WINBIO\_SENSOR\_ADVANCED\_MODE**</dt></span></span> </dl>       | <span data-ttu-id="ed864-114">Usare il sensore in modalità avanzata.</span><span class="sxs-lookup"><span data-stu-id="ed864-114">Operate the sensor in advanced mode.</span></span> <span data-ttu-id="ed864-115">Il sensore può acquisire esempi ed eseguire funzioni di archiviazione e corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ed864-115">The sensor can capture samples and perform matching and storage functions.</span></span><br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <span data-ttu-id="ed864-116"><dt>**\_modalità di \_ navigazione del sensore WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed864-116"><dt>**WINBIO\_SENSOR\_NAVIGATION\_MODE**</dt></span></span> </dl> | <span data-ttu-id="ed864-117">Utilizzare il sensore come pad del mouse.</span><span class="sxs-lookup"><span data-stu-id="ed864-117">Operate the sensor as a mouse pad.</span></span> <span data-ttu-id="ed864-118">Questa opzione non è attualmente supportata.</span><span class="sxs-lookup"><span data-stu-id="ed864-118">This is not currently supported.</span></span><br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <span data-ttu-id="ed864-119"><dt>**\_ \_ modalità sospensione sensore \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="ed864-119"><dt>**WINBIO\_SENSOR\_SLEEP\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="ed864-120">Utilizzare il sensore in modalità sospensione.</span><span class="sxs-lookup"><span data-stu-id="ed864-120">Operate the sensor in sleep mode.</span></span><br/>                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="ed864-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed864-121">Requirements</span></span>



| <span data-ttu-id="ed864-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed864-122">Requirement</span></span> | <span data-ttu-id="ed864-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ed864-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed864-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed864-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ed864-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ed864-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="ed864-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed864-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ed864-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed864-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ed864-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed864-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed864-129"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed864-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed864-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed864-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed864-131">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="ed864-131">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





