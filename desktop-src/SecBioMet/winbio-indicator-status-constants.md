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
# <a name="winbio_indicator_status-constants"></a>Costanti di stato dell' \_ indicatore WINBIO \_

Per impostare la luce di un indicatore, è possibile utilizzare i valori seguenti. Per impostazione predefinita, i sensori non avranno una luce accesa, ma le applicazioni possono usare questi valori per abilitare o disabilitare gli indicatori luminosi. Il valore di **\_ \_ stato del sensore WINBIO** fornisce maggiori dettagli sullo stato di una luce indicatore accesa. Per ulteriori informazioni, vedere le funzioni seguenti:

-   [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| Costante                                                                                                                                                                            | Descrizione                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <dt>**\_indicatore WINBIO \_**</dt> </dl>    | La luce dell'indicatore del sensore è accesa.<br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <dt>**\_indicatore WINBIO \_ disattivato**</dt> </dl> | La luce dell'indicatore del sensore è disattivata.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





