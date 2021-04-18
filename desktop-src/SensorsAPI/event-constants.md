---
description: La piattaforma sensore e posizione di Windows definisce le costanti per gli eventi del driver. Il sensore manfuactureres può anche definire le proprie costanti.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Costanti evento (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315332"
---
# <a name="event-constants-sensorsh"></a><span data-ttu-id="7d0df-104">Costanti evento (Sensors. h)</span><span class="sxs-lookup"><span data-stu-id="7d0df-104">Event Constants (Sensors.h)</span></span>

<span data-ttu-id="7d0df-105">La piattaforma sensore e posizione di Windows definisce le costanti per gli eventi del driver.</span><span class="sxs-lookup"><span data-stu-id="7d0df-105">The Windows Sensor and Location platform defines constants for driver events.</span></span> <span data-ttu-id="7d0df-106">Il sensore manfuactureres può anche definire le proprie costanti.</span><span class="sxs-lookup"><span data-stu-id="7d0df-106">Sensor manfuactureres can also define their own constants.</span></span>

<span data-ttu-id="7d0df-107">**Tipi di eventi del sensore**</span><span class="sxs-lookup"><span data-stu-id="7d0df-107">**Sensor Event Types**</span></span>

<span data-ttu-id="7d0df-108">La piattaforma definisce gli identificatori del tipo di evento del sensore seguenti.</span><span class="sxs-lookup"><span data-stu-id="7d0df-108">The platform defines the following sensor event type identifiers.</span></span>



| <span data-ttu-id="7d0df-109">Tipo di evento del sensore</span><span class="sxs-lookup"><span data-stu-id="7d0df-109">Sensor event type</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="7d0df-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d0df-110">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <span data-ttu-id="7d0df-111"><dt>**Sensore \_ di \_ \_ Scuotimento dell'accelerometro evento**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span><span class="sxs-lookup"><span data-stu-id="7d0df-111"><dt>**SENSOR\_EVENT\_ACCELEROMETER\_SHAKE**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span></span> </dl> | <span data-ttu-id="7d0df-112">Indica che il dispositivo è stato agitato.</span><span class="sxs-lookup"><span data-stu-id="7d0df-112">Indicates that the device was shaken.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <span data-ttu-id="7d0df-113"><dt>**Sensore \_ di \_Dati evento \_ aggiornati**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span><span class="sxs-lookup"><span data-stu-id="7d0df-113"><dt>**SENSOR\_EVENT\_DATA\_UPDATED**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span></span> </dl>                      | <span data-ttu-id="7d0df-114">Indica che i nuovi dati sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="7d0df-114">Indicates that new data is available.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <span data-ttu-id="7d0df-115"><dt>**Sensore \_ di \_Proprietà evento \_ modificata**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span><span class="sxs-lookup"><span data-stu-id="7d0df-115"><dt>**SENSOR\_EVENT\_PROPERTY\_CHANGED**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span></span> </dl>          | <span data-ttu-id="7d0df-116">Indica che un valore della proprietà è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="7d0df-116">Indicates that a property value changed.</span></span> <span data-ttu-id="7d0df-117">Controllare l'interfaccia [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) , passata tramite il parametro *PEventData* a [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), per determinare quale proprietà è stata modificata e il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="7d0df-117">Check the [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface, passed through the *pEventData* parameter to [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), to determine which property changed and its new value.</span></span><br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <span data-ttu-id="7d0df-118"><dt>**Sensore \_ di \_Stato evento \_ modificato**</dt> <dt>{BFD96016-6BD7-4560-ad34-F2F6607E8F81}</dt></span><span class="sxs-lookup"><span data-stu-id="7d0df-118"><dt>**SENSOR\_EVENT\_STATE\_CHANGED**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span></span> </dl>                   | <span data-ttu-id="7d0df-119">Indica una modifica dello stato operativo, ad esempio, dall' \_ inizializzazione dello stato del sensore \_ allo stato del sensore \_ \_ pronto.</span><span class="sxs-lookup"><span data-stu-id="7d0df-119">Indicates a change of operational state, for example, from SENSOR\_STATE\_INITIALIZING to SENSOR\_STATE\_READY.</span></span><br/>                                                                                                                                                                                            |



<span data-ttu-id="7d0df-120">**PROPERTYKEYs evento sensore**</span><span class="sxs-lookup"><span data-stu-id="7d0df-120">**Sensor Event PROPERTYKEYs**</span></span>

<span data-ttu-id="7d0df-121">Le chiavi di proprietà definite dalla piattaforma per gli eventi si basano sul GUID seguente:</span><span class="sxs-lookup"><span data-stu-id="7d0df-121">Platform-defined property keys for events are based on the following GUID:</span></span>

<span data-ttu-id="7d0df-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span><span class="sxs-lookup"><span data-stu-id="7d0df-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span></span>

<span data-ttu-id="7d0df-123">La piattaforma del sensore definisce i **PropertyKey** seguenti che identificano i parametri degli eventi del sensore.</span><span class="sxs-lookup"><span data-stu-id="7d0df-123">The sensor platform defines the following **PROPERTYKEY** s that identify sensor event parameters.</span></span>



| <span data-ttu-id="7d0df-124">Evento del sensore PROPERTYKEY e PID</span><span class="sxs-lookup"><span data-stu-id="7d0df-124">Sensor event PROPERTYKEY and PID</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="7d0df-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d0df-125">Description</span></span>                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <span data-ttu-id="7d0df-126"><dt>**Sensore \_ di \_ \_ \_ ID evento parametro evento**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="7d0df-126"><dt>**SENSOR\_EVENT\_PARAMETER\_EVENT\_ID**</dt> <dt>(PID = 2)</dt></span></span> </dl> | <span data-ttu-id="7d0df-127">Indica che il valore **GUID** in [IPORTABLEDEVICEVALUES](/previous-versions//ms740012(v=vs.85)) è un ID del tipo di evento, ad esempio \_ i dati degli eventi del sensore \_ \_ aggiornati.</span><span class="sxs-lookup"><span data-stu-id="7d0df-127">Indicates that the **GUID** value in [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) is an event type ID, such as SENSOR\_EVENT\_DATA\_UPDATED.</span></span><br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <span data-ttu-id="7d0df-128"><dt>**Sensore \_ di \_ \_ Stato parametro evento**</dt> <dt>(PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="7d0df-128"><dt>**SENSOR\_EVENT\_PARAMETER\_STATE**</dt> <dt>(PID = 3)</dt></span></span> </dl>           | <span data-ttu-id="7d0df-129">Indica che il valore Unsigned Integer in **IPortableDeviceValues** è uno stato del sensore, ad esempio \_ stato del sensore \_ pronto.</span><span class="sxs-lookup"><span data-stu-id="7d0df-129">Indicates that the unsigned integer value in **IPortableDeviceValues** is a sensor state, such as SENSOR\_STATE\_READY.</span></span><br/>                                                  |



<span data-ttu-id="7d0df-130">**Errore del sensore PROPERTYKEYs**</span><span class="sxs-lookup"><span data-stu-id="7d0df-130">**Sensor Error PROPERTYKEYs**</span></span>

<span data-ttu-id="7d0df-131">Le chiavi di proprietà definite dalla piattaforma per gli errori saranno basate sul GUID seguente:</span><span class="sxs-lookup"><span data-stu-id="7d0df-131">Platform-defined property keys for errors will be based on the following GUID:</span></span>

<span data-ttu-id="7d0df-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span><span class="sxs-lookup"><span data-stu-id="7d0df-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span></span>

<span data-ttu-id="7d0df-133">La piattaforma del sensore riserva questo GUID per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="7d0df-133">The sensor platform reserves this GUID for future use.</span></span>

<dl></dl>

## <a name="requirements"></a><span data-ttu-id="7d0df-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d0df-134">Requirements</span></span>



| <span data-ttu-id="7d0df-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d0df-135">Requirement</span></span> | <span data-ttu-id="7d0df-136">Valore</span><span class="sxs-lookup"><span data-stu-id="7d0df-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7d0df-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d0df-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7d0df-138">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7d0df-138">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7d0df-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d0df-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7d0df-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7d0df-140">None supported</span></span><br/>                                                            |
| <span data-ttu-id="7d0df-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d0df-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d0df-142"><dt>Sensori. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d0df-142"><dt>Sensors.h</dt></span></span> </dl> |



 

