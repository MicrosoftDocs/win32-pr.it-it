---
description: Contiene informazioni sulle condizioni in cui deve essere recuperato lo stato della batteria.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: BATTERY_WAIT_STATUS struttura (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 52885b75c7f9afba7ff336b3210ecf1b852f85b0091afe13026616816e43d7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143594"
---
# <a name="battery_wait_status-structure"></a>Struttura STATO BATTERY \_ WAIT \_

Contiene informazioni sulle condizioni in cui deve essere recuperato lo stato della batteria. Questa struttura viene usata dal codice di controllo DELLO STATO [**DELLA QUERY \_ IOCTL BATTERY. \_ \_**](ioctl-battery-query-status.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a>Members

<dl> <dt>

**BatteryTag**
</dt> <dd>

Tag della batteria corrente per la batteria. È possibile restituire solo le informazioni relative a una batteria corrispondente al tag. Ogni volta che questo valore non corrisponde al tag corrente della batteria, l'operazione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avrà esito negativo con un codice di errore FILE DI ERRORE NON TROVATO, che indica al chiamante che la batteria per cui ha un tag non è più installata Il chiamante può scegliere di usare l'operazione \_ \_ \_ [**IOCTL \_ BATTERY QUERY \_ \_ TAG**](ioctl-battery-query-tag.md) per determinare l'eventuale tag della batteria appena installata. Inoltre, se la richiesta è in corso quando la batteria viene rimossa o il tag cambia, l'operazione viene interrotta con lo stato \_ ERRORE FILE \_ NON \_ TROVATO. Per altre [informazioni, vedere Tag](battery-information.md) della batteria.

</dd> <dt>

**Timeout**
</dt> <dd>

Numero di millisecondi di attesa della richiesta per la condizione specificata dai membri **PowerState,** **LowCapacity** **e HighCapacity** prima del completamento. Il valore -1 indica che la richiesta attenderà per un tempo indefinito che le condizioni siano soddisfatte. Il valore zero indica che le informazioni sulla batteria richieste devono essere restituite immediatamente, indipendentemente dalle altre condizioni. Qualsiasi altro valore indica che la richiesta deve attendere tale periodo di tempo o fino a quando non viene soddisfatta una delle altre condizioni.

Se il computer è in modalità sospensione, l'orologio continuerà a essere eseguito, ma l'esaurimento del conteggio non riattiva il computer. Se il conteggio si esaurisce quando il computer viene riesaurito e vengono soddisfatte altre condizioni, la chiamata restituirà immediatamente il controllo.

</dd> <dt>

**PowerState**
</dt> <dd>

Zero, uno o più dei bit di stato seguenti, che indicano lo stato della batteria. È identico al membro **PowerState** della struttura [**BATTERY \_ STATUS.**](battery-status-str.md)



| Valore                                                                                                                                                                                                                                                   | Significato                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**BATTERIA \_ ADDEBITO**</dt> <dt>0x00000004</dt> </dl>                  | Indica che la batteria è attualmente in carica.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**BATTERIA \_ ERRORE CRITICO**</dt> <dt>0x00000008</dt> </dl>                  | Indica che l'errore della batteria è imminente. Per altre informazioni, vedere la sezione Osservazioni.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**BATTERIA \_ DISCHARGING**</dt> <dt>0x00000002</dt> </dl>         | Indica che la batteria è attualmente in fase di scaricamento.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**BATTERIA \_ POWER \_ ON \_ LINE**</dt> <dt>0x00000001</dt> </dl> | Indica che la batteria ha accesso all'alimentazione CA.<br/>                                        |



 

</dd> <dt>

**LowCapacity**
</dt> <dd>

Capacità corrente della batteria, in mWh (o relativa). Questo valore è identico al **membro Capacity** della struttura [**BATTERY \_ STATUS.**](battery-status-str.md)

</dd> <dt>

**HighCapacity**
</dt> <dd>

Capacità corrente della batteria, in mWh (o relativa). Questo valore è identico al **membro Capacity** della struttura [**BATTERY \_ STATUS.**](battery-status-str.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Le richieste di informazioni sulla batteria vengono posticipate fino a quando non si verifica una delle condizioni seguenti:

-   Il timeout scade (presupponendo che **Timeout** non sia -1).
-   Lo stato corrente della batteria non corrisponde a **PowerState.**
-   La capacità della batteria è inferiore a **LowCapacity.**
-   La capacità della batteria è superiore a **HighCapacity.**
-   Il tag della batteria cambia.

Quando una di queste condizioni viene soddisfatta, i dati vengono raccolti e l'operazione viene restituita. In questo modo le applicazioni possono monitorare le informazioni tipiche della batteria dinamica senza eseguire il polling del dispositivo.

Prima di usare una delle due condizioni di capacità, assicurarsi che la batteria le supporti usando il codice di controllo STATO QUERY BATTERY [**IOCTL \_ \_ \_**](ioctl-battery-query-status.md) con un timeout pari a zero. Esaminare i risultati per determinare se il **membro Capacity** è supportato, ovvero non BATTERY \_ UNKNOWN \_ CAPACITY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**STATO DELLA \_ BATTERIA**](battery-status-str.md)
</dt> <dt>

[**STATO QUERY BATTERIA IOCTL \_ \_ \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**TAG DI \_ QUERY DELLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

