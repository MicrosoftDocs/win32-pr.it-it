---
title: WINBIO_PRESENCE_CHANGE costanti (Winbio \_ types.h)
description: Descrive i tipi di modifiche che possono verificarsi quando il Windows Biometric Framework monitora la presenza di individui.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08cce9cc74bafdba6cf8d1aa11abccdaf7315370223ff6edf47eaba167af84f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909721"
---
# <a name="winbio_presence_change-constants"></a>Costanti WINBIO \_ PRESENCE \_ CHANGE

Descrive i tipi di modifiche che possono verificarsi quando il Windows Biometric Framework monitora la presenza di individui.



| Costante/valore                                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <dt>**WINBIO \_ TIPO \_ DI MODIFICA DELLA PRESENZA \_ \_ SCONOSCIUTO**</dt> <dt>0</dt> </dl>           | Il tipo di evento è sconosciuto. Questo valore viene utilizzato per la struttura non inizializzata.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <dt>**WINBIO \_ PRESENCE \_ CHANGE TYPE UPDATE \_ \_ \_ ALL**</dt> <dt>1</dt> </dl> | Fornisce informazioni su tutti i visi correnti nel fotogramma della fotocamera.<br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <dt>**WINBIO \_ ARRIVO \_ DEL TIPO DI MODIFICA \_ \_ DELLA**</dt> <dt>PRESENZA 2</dt> </dl>              | Un nuovo viso è stato inserito nel fotogramma della fotocamera.<br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <dt>**WINBIO \_ RICONOSCIMENTO \_ DEL TIPO DI MODIFICA DELLA \_ \_ PRESENZA**</dt> <dt>3</dt> </dl>     | Un viso è stato abbinato a un utente registrato.<br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <dt>**WINBIO \_ TIPO \_ DI MODIFICA DELLA PRESENZA \_ \_ 4**</dt> <dt></dt> </dl>              | Un viso rilevato in precedenza è stato fuori dal fotogramma della fotocamera per un periodo di tempo.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <dt>**WINBIO \_ RILEVAMENTO \_ DEL TIPO DI MODIFICA DELLA \_ \_ PRESENZA**</dt> <dt>5</dt> </dl>                 | Fornisce informazioni aggiornate sul rettangolo di selezione e rifiuta i valori di dettaglio per un subset dei visi attualmente presenti nel fotogramma della fotocamera.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Winbio \_ adapters.h per gli adapter)</dt> </dl> |



 

 





