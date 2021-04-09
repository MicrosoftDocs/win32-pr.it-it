---
description: La categoria dei sensori \_ \_ biometrici contiene sensori che forniscono informazioni sugli esseri viventi.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71660c7bc94037c21502c91e017a8eba369766a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128746"
---
# <a name="sensor_category_biometric"></a><span data-ttu-id="22b4e-103">\_biometria categoria \_ sensore</span><span class="sxs-lookup"><span data-stu-id="22b4e-103">SENSOR\_CATEGORY\_BIOMETRIC</span></span>

<span data-ttu-id="22b4e-104">La categoria dei sensori \_ \_ biometrici contiene sensori che forniscono informazioni sugli esseri viventi.</span><span class="sxs-lookup"><span data-stu-id="22b4e-104">The SENSOR\_CATEGORY\_BIOMETRIC category contains sensors that provide information about living beings.</span></span>

<span data-ttu-id="22b4e-105">**Tipi di sensore definiti dalla piattaforma**</span><span class="sxs-lookup"><span data-stu-id="22b4e-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="22b4e-106">Questa categoria include i tipi di sensore definiti dalla piattaforma seguenti.</span><span class="sxs-lookup"><span data-stu-id="22b4e-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="22b4e-107">Tipo di sensore</span><span class="sxs-lookup"><span data-stu-id="22b4e-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="22b4e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22b4e-108">Description</span></span>                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <span data-ttu-id="22b4e-109"><dt>**Sensore \_ di Digitare \_ la \_ presenza umana**</dt> <dt>{C138C12B-AD52-451c-9375-87F518FF10C6}</dt></span><span class="sxs-lookup"><span data-stu-id="22b4e-109"><dt>**SENSOR\_TYPE\_HUMAN\_PRESENCE**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt></span></span> </dl>    | <span data-ttu-id="22b4e-110">Sensori che rilevano la presenza umana.</span><span class="sxs-lookup"><span data-stu-id="22b4e-110">Sensors that detect human presence.</span></span><br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <span data-ttu-id="22b4e-111"><dt>**Sensore \_ di Digitare \_ \_ prossimità umana**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt></span><span class="sxs-lookup"><span data-stu-id="22b4e-111"><dt>**SENSOR\_TYPE\_HUMAN\_PROXIMITY**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt></span></span> </dl> | <span data-ttu-id="22b4e-112">Sensori che rilevano la vicinanza umana.</span><span class="sxs-lookup"><span data-stu-id="22b4e-112">Sensors that detect human proximity.</span></span><br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <span data-ttu-id="22b4e-113"><dt>**Sensore \_ di Digitare \_ touch**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt></span><span class="sxs-lookup"><span data-stu-id="22b4e-113"><dt>**SENSOR\_TYPE\_TOUCH**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt></span></span> </dl>                                | <span data-ttu-id="22b4e-114">Sensori di tocco.</span><span class="sxs-lookup"><span data-stu-id="22b4e-114">Touch sensors.</span></span><br/>                       |



<span data-ttu-id="22b4e-115">**Campi dati definiti dalla piattaforma**</span><span class="sxs-lookup"><span data-stu-id="22b4e-115">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="22b4e-116">Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate sul \_ tipo di dati Sensor \_ \_ Biometric \_ GUID:</span><span class="sxs-lookup"><span data-stu-id="22b4e-116">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_BIOMETRIC\_GUID:</span></span>

<span data-ttu-id="22b4e-117">{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}</span><span class="sxs-lookup"><span data-stu-id="22b4e-117">{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}</span></span>

<span data-ttu-id="22b4e-118">Questa categoria include i campi dati definiti dalla piattaforma seguenti.</span><span class="sxs-lookup"><span data-stu-id="22b4e-118">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="22b4e-119">Nome del campo dati e PID</span><span class="sxs-lookup"><span data-stu-id="22b4e-119">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="22b4e-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22b4e-120">Description</span></span>                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <span data-ttu-id="22b4e-121"><dt>**Sensore \_ di \_ \_ \_ Presenza umana del tipo di dati**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="22b4e-121"><dt>**SENSOR\_DATA\_TYPE\_HUMAN\_PRESENCE**</dt> <dt>(PID = 2) </dt></span></span> </dl>                          | <span data-ttu-id="22b4e-122">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="22b4e-122">**VT\_BOOL**</span></span><br/> <span data-ttu-id="22b4e-123">**True** quando un uomo utilizza il computer.</span><span class="sxs-lookup"><span data-stu-id="22b4e-123">**TRUE** when a human is using the computer.</span></span><br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <span data-ttu-id="22b4e-124"><dt>**Sensore \_ di Tipo di dati \_ \_ \_ \_ contatori di prossimità umana**</dt> <dt>(PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="22b4e-124"><dt>**SENSOR\_DATA\_TYPE\_HUMAN\_PROXIMITY\_METERS**</dt> <dt>(PID = 3) </dt></span></span> </dl> | <span data-ttu-id="22b4e-125">**\_R4 VT**</span><span class="sxs-lookup"><span data-stu-id="22b4e-125">**VT\_R4**</span></span><br/> <span data-ttu-id="22b4e-126">Distanza tra un uomo e il computer, in metri.</span><span class="sxs-lookup"><span data-stu-id="22b4e-126">Distance between a human and the computer, in meters.</span></span><br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <span data-ttu-id="22b4e-127"><dt>**Sensore \_ di \_ \_ \_ Stato tocco del tipo di dati**</dt> <dt>(PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="22b4e-127"><dt>**SENSOR\_DATA\_TYPE\_TOUCH\_STATE**</dt> <dt>(PID = 4) </dt></span></span> </dl>                                   | <span data-ttu-id="22b4e-128">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="22b4e-128">**VT\_BOOL**</span></span><br/> <span data-ttu-id="22b4e-129">**True** quando viene toccato il sensore tattile; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="22b4e-129">**TRUE** when the touch sensor is being touched; otherwise, **FALSE**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="22b4e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22b4e-130">Requirements</span></span>



| <span data-ttu-id="22b4e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="22b4e-131">Requirement</span></span> | <span data-ttu-id="22b4e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="22b4e-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="22b4e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22b4e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="22b4e-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="22b4e-134">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="22b4e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22b4e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="22b4e-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="22b4e-136">None supported</span></span><br/>                                                            |
| <span data-ttu-id="22b4e-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22b4e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="22b4e-138"><dt>Sensori. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b4e-138"><dt>Sensors.h</dt></span></span> </dl> |



 

 




