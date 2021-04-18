---
description: Contiene informazioni sulle condizioni in base alle quali deve essere recuperato lo stato della batteria.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: Struttura BATTERY_WAIT_STATUS (Poclass. h)
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
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312058"
---
# <a name="battery_wait_status-structure"></a>\_ \_ Struttura dello stato di attesa della batteria

Contiene informazioni sulle condizioni in base alle quali deve essere recuperato lo stato della batteria. Questa struttura viene utilizzata dal codice di controllo [**\_ \_ \_ dello stato delle query della batteria IOCTL**](ioctl-battery-query-status.md) .

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

Tag della batteria corrente per la batteria. Possono essere restituite solo le informazioni per una batteria corrispondente al tag. Ogni volta che questo valore non corrisponde al tag corrente della batteria, l'operazione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ha esito negativo e viene visualizzato un codice di errore \_ non trovato nel file di errore \_ \_ , che indica al chiamante che la batteria per cui ha un tag non è più installata. il chiamante può scegliere di usare l'operazione di [**tag di \_ query della batteria \_ \_ IOCTL**](ioctl-battery-query-tag.md) per determinare il tag della batteria appena installata. Inoltre, se la richiesta è in corso quando la batteria viene rimossa o il tag viene modificato, l'operazione viene interrotta con lo stato del file di errore \_ \_ non \_ trovato. Per ulteriori informazioni, vedere la pagina relativa ai [tag della batteria](battery-information.md) .

</dd> <dt>

**Timeout**
</dt> <dd>

Il numero di millisecondi di attesa della richiesta per la condizione specificata dai membri **PowerState**, **LowCapacity** e **HighCapacity** prima del completamento. Un valore pari a-1 indica che la richiesta attende indefinitamente che le condizioni vengano soddisfatte. Un valore pari a zero indica che le informazioni sulla batteria richieste devono essere restituite immediatamente, indipendentemente dalle altre condizioni. Qualsiasi altro valore indica che la richiesta deve attendere tale periodo di tempo o fino a quando non viene soddisfatta una delle altre condizioni.

Se il computer è entrato in modalità sospensione, l'orologio continuerà a essere eseguito, ma l'esaurimento del conteggio non riattiverà il computer. Se il conteggio viene esaurito quando il computer viene riattivato e le altre condizioni vengono soddisfatte, la chiamata verrà immediatamente restituita in fase di riattivazione.

</dd> <dt>

**PowerState**
</dt> <dd>

Zero, uno o più dei seguenti bit di stato, che indicano lo stato della batteria. È identico al membro **PowerState** della struttura [**\_ dello stato della batteria**](battery-status-str.md) .



| Valore                                                                                                                                                                                                                                                   | Significato                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**Batteria \_ CARICAMENTO**</dt> di <dt>0x00000004</dt> </dl>                  | Indica che la batteria è in fase di caricamento.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**Batteria \_**</dt> <dt>0x00000008</dt> critico </dl>                  | Indica che l'errore della batteria è imminente. Per altre informazioni, vedere la sezione Osservazioni.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**Batteria \_ Discaricamento**</dt> di <dt>0x00000002</dt> </dl>         | Indica che la batteria è in fase di disattivazione.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**Batteria \_ POWER \_ on \_ line**</dt> <dt>0x00000001</dt> </dl> | Indica che la batteria ha accesso alla rete elettrica.<br/>                                        |



 

</dd> <dt>

**LowCapacity**
</dt> <dd>

Capacità corrente della batteria, in mWh (o relativa). Questo valore è identico al membro **Capacity** della [**struttura \_ dello stato della batteria**](battery-status-str.md) .

</dd> <dt>

**HighCapacity**
</dt> <dd>

Capacità corrente della batteria, in mWh (o relativa). Questo valore è identico al membro **Capacity** della [**struttura \_ dello stato della batteria**](battery-status-str.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Le richieste di informazioni sulla batteria vengono posticipate fino a quando non si verifica una delle condizioni seguenti:

-   Scade il timeout (presupponendo che il **timeout** non sia-1).
-   Lo stato corrente della batteria non corrisponde a **PowerState**.
-   La capacità della batteria è inferiore a **LowCapacity**.
-   La capacità della batteria è superiore a **HighCapacity**.
-   Il tag della batteria viene modificato.

Quando viene soddisfatta una di queste condizioni, i dati vengono raccolti e l'operazione restituisce. Questo consente alle applicazioni di monitorare le informazioni tipiche della batteria dinamica senza eseguire il polling del dispositivo.

Prima di usare una delle due condizioni di capacità, assicurarsi che la batteria li supporti usando il codice di controllo [**\_ \_ \_ dello stato di query della batteria IOCTL**](ioctl-battery-query-status.md) con un timeout di zero. Esaminare i risultati per determinare se il membro di **capacità** è supportato (ovvero la \_ capacità sconosciuta della batteria \_ ).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**stato della batteria \_**](battery-status-str.md)
</dt> <dt>

[**\_stato della \_ query della batteria IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_tag di \_ query della batteria IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

