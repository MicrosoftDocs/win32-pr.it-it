---
description: La \_ categoria Sensor \_ other Category contiene sensori che supportano la classe personalizzata nel driver della classe HID.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049422"
---
# <a name="sensor_category_other"></a><span data-ttu-id="d1878-103">categoria di sensori \_ \_ altro</span><span class="sxs-lookup"><span data-stu-id="d1878-103">SENSOR\_CATEGORY\_OTHER</span></span>

<span data-ttu-id="d1878-104">La \_ categoria Sensor \_ other Category contiene sensori che supportano la classe personalizzata nel driver della classe HID.</span><span class="sxs-lookup"><span data-stu-id="d1878-104">The SENSOR\_CATEGORY\_OTHER category contains sensors that support the Custom class in the HID Class driver.</span></span>

<dl> <dt>

<span data-ttu-id="d1878-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**tipo di sensore \_ \_ personalizzato**</span><span class="sxs-lookup"><span data-stu-id="d1878-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**SENSOR\_TYPE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1878-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span><span class="sxs-lookup"><span data-stu-id="d1878-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span></span>
</dt> <dt>



<span data-ttu-id="d1878-107">Sensore personalizzato che supporta la classe personalizzata nel driver della classe HID.</span><span class="sxs-lookup"><span data-stu-id="d1878-107">Custom sensor that supports the Custom class in the HID Class driver.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="d1878-108">**Campi dati definiti dalla piattaforma**</span><span class="sxs-lookup"><span data-stu-id="d1878-108">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="d1878-109">Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate \_ sul \_ GUID personalizzato del tipo di dati del sensore \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="d1878-109">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_CUSTOM\_GUID:</span></span>

<span data-ttu-id="d1878-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span><span class="sxs-lookup"><span data-stu-id="d1878-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span></span>

<span data-ttu-id="d1878-111">Questa categoria include i campi dati definiti dalla piattaforma seguenti.</span><span class="sxs-lookup"><span data-stu-id="d1878-111">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="d1878-112">Nome del campo dati e PID</span><span class="sxs-lookup"><span data-stu-id="d1878-112">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="d1878-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1878-113">Description</span></span>                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <span data-ttu-id="d1878-114"><dt>**Sensore \_ di \_ \_ \_ Utilizzo personalizzato del tipo di dati**</dt> <dt> (PID = 5)</dt></span><span class="sxs-lookup"><span data-stu-id="d1878-114"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_USAGE**</dt> <dt> (PID = 5) </dt></span></span> </dl>                          | <span data-ttu-id="d1878-115">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="d1878-115">**VT\_UI4**</span></span><br/> <span data-ttu-id="d1878-116">Utilizzo HID che può essere utilizzato per distinguere più sensori personalizzati.</span><span class="sxs-lookup"><span data-stu-id="d1878-116">A HID usage which can be used to distinguish multiple, custom sensors.</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <span data-ttu-id="d1878-117"><dt>**Sensore \_ di \_ \_ \_ \_ Matrice booleana personalizzata del tipo di dati**</dt> <dt> (PID = 6)</dt></span><span class="sxs-lookup"><span data-stu-id="d1878-117"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_BOOLEAN\_ARRAY**</dt> <dt> (PID = 6) </dt></span></span> </dl> | <span data-ttu-id="d1878-118">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="d1878-118">**VT\_UI4**</span></span><br/> <span data-ttu-id="d1878-119">Matrice di valori booleani per un sensore personalizzato specificato.</span><span class="sxs-lookup"><span data-stu-id="d1878-119">An array of Boolean values for a given custom sensor.</span></span><br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <span data-ttu-id="d1878-120"><dt>**Sensore \_ di Tipo di dati \_ \_ personalizzato \_ value1**</dt> <dt> (PID = 7)</dt></span><span class="sxs-lookup"><span data-stu-id="d1878-120"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE1**</dt> <dt> (PID = 7) </dt></span></span> </dl>                       | <span data-ttu-id="d1878-121">**VT \_ UI4 VT \| \| \_ R4**</span><span class="sxs-lookup"><span data-stu-id="d1878-121">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="d1878-122">Uno dei sei valori disponibili per un sensore personalizzato specificato.</span><span class="sxs-lookup"><span data-stu-id="d1878-122">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <span data-ttu-id="d1878-123"><dt>**Sensore \_ di \_Tipo di \_ dati \_ value2 personalizzato**</dt> <dt> (PID = 8)</dt></span><span class="sxs-lookup"><span data-stu-id="d1878-123"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE2**</dt> <dt> (PID = 8) </dt></span></span> </dl>                       | <span data-ttu-id="d1878-124">**VT \_ UI4 VT \| \| \_ R4**</span><span class="sxs-lookup"><span data-stu-id="d1878-124">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="d1878-125">Uno dei sei valori disponibili per un sensore personalizzato specificato.</span><span class="sxs-lookup"><span data-stu-id="d1878-125">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <span data-ttu-id="d1878-126"><dt>**Sensore \_ di Tipo di dati \_ \_ personalizzato \_ valore3**</dt> <dt> (PID = 9)</dt></span><span class="sxs-lookup"><span data-stu-id="d1878-126"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE3**</dt> <dt> (PID = 9) </dt></span></span> </dl>                       | <span data-ttu-id="d1878-127">**VT \_ UI4 VT \| \| \_ R4**</span><span class="sxs-lookup"><span data-stu-id="d1878-127">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="d1878-128">Uno dei sei valori disponibili per un sensore personalizzato specificato.</span><span class="sxs-lookup"><span data-stu-id="d1878-128">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <span data-ttu-id="d1878-129"><dt>**Sensore \_ di Tipo di dati \_ \_ personalizzato \_ VALUE4**</dt> <dt> (PID = 10)</dt></span><span class="sxs-lookup"><span data-stu-id="d1878-129"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE4**</dt> <dt> (PID = 10) </dt></span></span> </dl>                      | <span data-ttu-id="d1878-130">**VT \_ UI4 VT \| \| \_ R4**</span><span class="sxs-lookup"><span data-stu-id="d1878-130">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="d1878-131">Uno dei sei valori disponibili per un sensore personalizzato specificato.</span><span class="sxs-lookup"><span data-stu-id="d1878-131">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <span data-ttu-id="d1878-132"><dt>**Sensore \_ di Tipo di dati \_ \_ personalizzato \_ VALUE5**</dt> <dt> (PID = 11)</dt></span><span class="sxs-lookup"><span data-stu-id="d1878-132"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE5**</dt> <dt> (PID = 11) </dt></span></span> </dl>                      | <span data-ttu-id="d1878-133">**VT \_ UI4 VT \| \| \_ R4**</span><span class="sxs-lookup"><span data-stu-id="d1878-133">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="d1878-134">Uno dei sei valori disponibili per un sensore personalizzato specificato.</span><span class="sxs-lookup"><span data-stu-id="d1878-134">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <span data-ttu-id="d1878-135"><dt>**Sensore \_ di Tipo di dati \_ \_ personalizzato \_ VALUE6**</dt> <dt> (PID = 12)</dt></span><span class="sxs-lookup"><span data-stu-id="d1878-135"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE6**</dt> <dt> (PID = 12) </dt></span></span> </dl>                      | <span data-ttu-id="d1878-136">**VT \_ UI4 VT \| \| \_ R4**</span><span class="sxs-lookup"><span data-stu-id="d1878-136">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="d1878-137">Uno dei sei valori disponibili per un sensore personalizzato specificato.</span><span class="sxs-lookup"><span data-stu-id="d1878-137">One of six available values for a given custom sensor.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="d1878-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1878-138">Remarks</span></span>

<span data-ttu-id="d1878-139">Un sensore che supporta la classe generica nel driver della classe HID viene mappato a una delle altre categorie definite (biometrica, elettrica, ambientale e così via).</span><span class="sxs-lookup"><span data-stu-id="d1878-139">A sensor that supports the Generic class in the HID class driver will map to one of the other defined categories (biometric, electrical, environmental, and so on).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1878-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1878-140">Requirements</span></span>



| <span data-ttu-id="d1878-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1878-141">Requirement</span></span> | <span data-ttu-id="d1878-142">Valore</span><span class="sxs-lookup"><span data-stu-id="d1878-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d1878-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1878-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d1878-144">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d1878-144">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d1878-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1878-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d1878-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d1878-146">None supported</span></span><br/>                                                            |
| <span data-ttu-id="d1878-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1878-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1878-148"><dt>Sensori. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1878-148"><dt>Sensors.h</dt></span></span> </dl> |



 

 




