---
description: Contiene lo stato corrente della batteria.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: Struttura BATTERY_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: d6e68f5cec0215687fe4fde66698ea1be0d62c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312059"
---
# <a name="battery_status-structure"></a>\_Struttura dello stato della batteria

Contiene lo stato corrente della batteria. Questa struttura viene utilizzata dal codice di controllo [**\_ \_ \_ dello stato delle query della batteria IOCTL**](ioctl-battery-query-status.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a>Members

<dl> <dt>

**PowerState**
</dt> <dd>

Stato della batteria. Questo membro può essere zero, uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**Batteria \_ CARICAMENTO**</dt> di <dt>0x00000004</dt> </dl>                  | Indica che la batteria è in fase di caricamento.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**Batteria \_**</dt> <dt>0x00000008</dt> critico </dl>                  | Indica che l'errore della batteria è imminente. Per altre informazioni, vedere la sezione Osservazioni.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**Batteria \_ Discaricamento**</dt> di <dt>0x00000002</dt> </dl>         | Indica che la batteria è in fase di disattivazione.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**Batteria \_ POWER \_ on \_ line**</dt> <dt>0x00000001</dt> </dl> | Indica che il sistema ha accesso alla rete elettrica, quindi nessuna batteria viene ricaricata.<br/>   |



 

</dd> <dt>

**Capacity**
</dt> <dd>

Capacità corrente della batteria, in mWh (o relativa). Questo valore può essere usato per generare una visualizzazione "misuratore di gas" dividendo il membro **FullChargedCapacity** della struttura delle [**\_ informazioni sulla batteria**](battery-information-str.md) . Se la capacità non è disponibile, questo membro è una \_ capacità sconosciuta a batteria \_ .

</dd> <dt>

**Tensione**
</dt> <dd>

Tensione della batteria corrente nei terminali della batteria, in millivolt (MV). Se la tensione non è disponibile, il membro è una \_ tensione sconosciuta a batteria \_ .

</dd> <dt>

**Frequenza di campionamento**
</dt> <dd>

Frequenza corrente di carica o scaricamento della batteria. Questo valore sarà in milliwatt, a meno che le informazioni sulla frequenza della batteria siano relative, nel qual caso saranno in unità arbitrarie all'ora. Per determinare se le informazioni sulla batteria sono relative, esaminare il \_ flag relativo di capacità della batteria \_ nel membro delle **funzionalità** della struttura delle [**\_ informazioni sulla batteria**](battery-information-str.md) . Un tasso positivo diverso da zero indica una ricarica; una frequenza negativa indica la discaricamento. Alcune batterie segnalano solo le tariffe di discarico. Se la frequenza non è disponibile, il membro è una \_ frequenza sconosciuta della batteria \_ . Se viene modificato lo stato della batteria o dell'alimentazione, è possibile che la velocità diventi disponibile.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il \_ flag critico della batteria nel membro **PowerState** della struttura indica una condizione hardware "batteria critica". Questo livello critico viene impostato dal produttore della batteria, non dall'utente nell'"allarme batteria critica". In genere significa che il sistema di batteria ha calcolato che la batteria è completamente scaricata e qualsiasi potenza disegnata è superiore a quanto previsto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_informazioni sulla batteria**](battery-information-str.md)
</dt> <dt>

[**\_stato della \_ query della batteria IOCTL \_**](ioctl-battery-query-status.md)
</dt> </dl>

 

 




