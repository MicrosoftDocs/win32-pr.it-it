---
description: Contiene lo stato corrente della batteria.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: BATTERY_STATUS struttura (Poclass.h)
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
ms.openlocfilehash: 28b75a8eb1c7abf647f3f8ea61b29dedb40978f3ea639fc505364a12ae5e57cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143604"
---
# <a name="battery_status-structure"></a>Struttura BATTERY \_ STATUS

Contiene lo stato corrente della batteria. Questa struttura viene usata dal codice di controllo DELLO STATO [**DELLA QUERY \_ IOCTL BATTERY. \_ \_**](ioctl-battery-query-status.md)

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
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**BATTERIA \_ ADDEBITO**</dt> <dt>0x00000004</dt> </dl>                  | Indica che la batteria è attualmente in carica.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**BATTERIA \_ ERRORE CRITICO**</dt> <dt>0x00000008</dt> </dl>                  | Indica che l'errore della batteria è imminente. Per altre informazioni, vedere la sezione Osservazioni.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**BATTERIA \_ DISCHARGING**</dt> <dt>0x00000002</dt> </dl>         | Indica che la batteria è attualmente in fase di scaricamento.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**BATTERIA \_ ALIMENTAZIONE \_ ON \_ LINE**</dt> <dt>0x00000001</dt> </dl> | Indica che il sistema ha accesso all'alimentazione CA, in modo che non vengano scaricate batterie.<br/>   |



 

</dd> <dt>

**Capacity**
</dt> <dd>

Capacità corrente della batteria, in mWh (o relativa). Questo valore può essere usato per generare una visualizzazione "misuratore gas" dividendo il misuratore per il membro **FullChargedCapacity** della struttura [**BATTERY \_ INFORMATION.**](battery-information-str.md) Se la capacità non è disponibile, questo membro è BATTERY \_ UNKNOWN \_ CAPACITY.

</dd> <dt>

**Tensione**
</dt> <dd>

La tensione corrente della batteria tra i terminali della batteria, in millivolts (mv). Se la tensione non è disponibile, questo membro è BATTERY \_ UNKNOWN \_ VOLTAGE.

</dd> <dt>

**Frequenza di campionamento**
</dt> <dd>

Frequenza corrente di carica o scarica della batteria. Questo valore sarà espresso in milliwatt, a meno che le informazioni sulla frequenza della batteria non siano relative, nel qual caso saranno in unità arbitrarie all'ora. Per determinare se le informazioni sulla batteria sono relative, esaminare il flag BATTERY \_ CAPACITY RELATIVE nel membro \_ **Capabilities** della struttura [**BATTERY \_ INFORMATION.**](battery-information-str.md) Una tariffa positiva diversa da zero indica l'addebito; un tasso negativo indica la discarica. Alcune batterie segnalano solo tariffe di scaricamento. Se la frequenza non è disponibile, questo membro è BATTERY \_ UNKNOWN \_ RATE. Se lo stato della batteria o della fonte di alimentazione cambia, la velocità potrebbe diventare disponibile.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il flag BATTERY \_ CRITICAL nel membro **PowerState** di questa struttura indica una condizione hardware "batteria critica". Questo livello critico viene impostato dal produttore della batteria, non dall'utente nell'"allarme batteria critica". In genere significa che il sistema a batteria ha calcolato che la batteria è completamente scaricata e che l'eventuale potenza estratta è superiore a quella prevista.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI SULLA \_ BATTERIA**](battery-information-str.md)
</dt> <dt>

[**STATO QUERY BATTERIA IOCTL \_ \_ \_**](ioctl-battery-query-status.md)
</dt> </dl>

 

 




