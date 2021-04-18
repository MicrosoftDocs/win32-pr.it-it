---
description: Contiene informazioni sulla batteria.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: Struttura BATTERY_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 1e892a14263822ddd009b162c6343975e1689683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312063"
---
# <a name="battery_information-structure"></a>\_Struttura delle informazioni sulla batteria

Contiene informazioni sulla batteria. Questa struttura viene restituita dal codice di controllo delle [**\_ \_ \_ informazioni sulle query della batteria IOCTL**](ioctl-battery-query-information.md) quando è richiesto il livello di informazioni BatteryInformation.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a>Members

<dl> <dt>

**Capabilities**
</dt> <dd>

Funzionalità della batteria. Il membro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <dt>**Batteria \_ 0x40000000 \_ relativa alla capacità**</dt> <dt></dt> </dl>                    | Indica che le informazioni sulla capacità e sulla frequenza della batteria sono relative e non in unità specifiche. Se questo bit non è impostato, le unità di report sono milliwatt ore (mWh) per la capacità e milliwatt (mW) per la frequenza. Se questo bit è impostato, tutti i riferimenti alle unità nell'altra documentazione della batteria possono essere ignorati. Tutte le informazioni sulla frequenza sono indicate in unità all'ora. Se ad esempio la capacità completamente addebitata è indicata come 100, la velocità 200 indica che la batteria utilizzerà tutta la sua capacità in mezz'ora.<br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <dt>**Batteria \_ 0x20000000 a \_ breve \_ termine**</dt> <dt></dt> </dl>                               | Indica che l'operazione normale è per una funzione non affidabile. Se questo bit non è impostato, si prevede che la batteria venga utilizzata durante il normale utilizzo del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <dt>**Batteria \_ IMPOSTA \_ addebito 0x00000001 \_ supportato**</dt> <dt></dt> </dl>          | Indica che il dispositivo batteria supporta le richieste di impostazione delle informazioni del tipo BatteryCharge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <dt>**Batteria \_ IMPOSTA \_ \_**</dt> il <dt>0x00000002</dt> supportato </dl> | Indica che il dispositivo batteria supporta le richieste di impostazione delle informazioni del tipo BatteryDischarge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <dt>**Batteria \_ \_Batteria del sistema**</dt> <dt>0x80000000</dt> </dl>                             | Indica che la batteria può fornire l'alimentazione generale per l'esecuzione del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Tecnologia**
</dt> <dd>

Tecnologia della batteria. Il membro può essere uno dei valori seguenti.



| Valore                                                                        | Significato                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Batteria non ricaricabile, ad esempio, alcalina.<br/> |
| <dl> <dt>1</dt> </dl> | Batteria ricaricabile, ad esempio acido di piombo.<br/>   |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**Chimica**
</dt> <dd>

Stringa di caratteri abbreviata che indica la chimica della batteria. Questa stringa non è necessariamente con terminazione zero. Di seguito è riportato un elenco parziale delle abbreviazioni che possono essere restituite e del chimiche associato.



| Stringa Unicode                                                                                                                                           | Significato                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <dt>**PbAc**</dt> </dl> | Acido lead<br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <dt>**LION**</dt> </dl>                        | Ioni di litio<br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <dt>**Li-I**</dt> </dl> | Ioni di litio<br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <dt>**NiCd**</dt> </dl> | Nichel cadmio<br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <dt>**NiMH**</dt> </dl> | Idruro Nickel metal<br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <dt>**NiZn**</dt> </dl> | Zinco nichel<br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <dt>**RAM**</dt> </dl>                           | Alkaline-Manganese ricaricabile<br/> |



 

Altri chimiche possono essere visualizzati in futuro e il codice deve essere in grado di gestirli.

</dd> <dt>

**DesignedCapacity**
</dt> <dd>

Capacità teorica della batteria quando è nuova, in mWh, a meno che non \_ sia impostata la capacità della batteria \_ relativa. In tal caso, le unità non sono definite.

</dd> <dt>

**FullChargedCapacity**
</dt> <dd>

Capacità corrente completamente addebitata della batteria in mWh (o relativa). Confrontare questo valore con **DesignedCapacity** per stimare l'usura della batteria.

</dd> <dt>

**DefaultAlert1**
</dt> <dd>

Capacità consigliata dal produttore, in mWh, in cui deve verificarsi un avviso di batteria basso. Le definizioni del basso variano dal produttore al produttore. In generale, si verificherà uno stato di avviso prima di uno stato basso, ma è preferibile non presupporre che sia sempre. Per ridurre il rischio di perdita di dati, questo valore viene in genere usato come impostazione predefinita per l'allarme della batteria critica.

</dd> <dt>

**DefaultAlert2**
</dt> <dd>

Capacità consigliata dal produttore, in mWh, in corrispondenza della quale deve verificarsi un avviso di batteria. Le definizioni di avviso variano dal produttore al produttore. In generale, si verificherà uno stato di avviso prima di uno stato basso, ma è preferibile non presupporre che sia sempre. Per ridurre il rischio di perdita di dati, questo valore viene in genere usato come impostazione predefinita per l'allarme batteria basso.

</dd> <dt>

**CriticalBias**
</dt> <dd>

Distorsione da zero, in mWh, applicata alla funzionalità di segnalazione della batteria. Alcune batterie riservano un costo ridotto, che è prevenuto dai valori di capacità della batteria per mostrare "0" come livello di batteria critico. La distorsione critica è analoga all'impostazione di un misuratore di carburante per mostrare "Empty" quando ci sono più litri di carburante a sinistra.

</dd> <dt>

**CycleCount**
</dt> <dd>

Il numero di cicli di addebito/scaricamento che la batteria ha riscontrato. Questo consente di determinare il consumo della batteria. Se la batteria non supporta un contatore di cicli, questo membro è zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

In genere, uno stato di avviso si verifica prima di uno stato basso, ma è preferibile non presupporre che sia. È possibile eseguire il polling di una batteria e rilevare che non si è verificato alcun livello di avviso e quindi eseguire di nuovo il polling della batteria e individuarne l'addebito nella misura in cui sono stati realizzati entrambi i livelli. Questo può indicare che il polling non è abbastanza frequente. Potrebbe inoltre indicare che la batteria non è in grado di sostenere un addebito per molto tempo e viene ricaricata più velocemente del previsto. Una batteria di questo tipo può essere vicina alla fine della sua vita utile oppure potrebbe essere danneggiata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ informazioni sulle query della batteria IOCTL \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




