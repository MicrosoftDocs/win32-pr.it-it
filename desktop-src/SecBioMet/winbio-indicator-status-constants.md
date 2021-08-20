---
title: WINBIO_INDICATOR_STATUS costanti (Winbio \_ types.h)
description: Impostare una luce indicatore.
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
ms.openlocfilehash: 9fd05d279bd11eafda89eed436c94d6141e97ad0eb9d2fc426d5c89000f36414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910014"
---
# <a name="winbio_indicator_status-constants"></a>Costanti DI STATO INDICATORE WINBIO \_ \_

I valori seguenti possono essere usati per impostare una luce indicatore. Per impostazione predefinita, i sensori non avranno una luce accese, ma le applicazioni possono usare questi valori per abilitare o disabilitare le luci degli indicatori. Il **valore WINBIO \_ SENSOR STATUS \_ (STATO SENSORE WINBIO)** fornisce informazioni più dettagliate sullo stato di una luce indicatore acceda. Per altre informazioni, vedere le funzioni seguenti:

-   [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| Costante                                                                                                                                                                            | Descrizione                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <dt>**INDICATORE WINBIO \_ \_ ON**</dt> </dl>    | La luce dell'indicatore del sensore è accerta.<br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <dt>**INDICATORE WINBIO \_ \_ DISATTIVATO**</dt> </dl> | La luce dell'indicatore del sensore è spenta.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





