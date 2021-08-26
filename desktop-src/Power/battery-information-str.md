---
description: Contiene informazioni sulla batteria.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: BATTERY_INFORMATION struttura (Poclass.h)
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
ms.openlocfilehash: c449f325e03fb4ea81fe0aa148eaddcf65800b5a56356e22232477e0b6d4fa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033011"
---
# <a name="battery_information-structure"></a>Struttura BATTERY \_ INFORMATION

Contiene informazioni sulla batteria. Questa struttura viene restituita dal codice di controllo [**IOCTL \_ BATTERY \_ QUERY \_ INFORMATION**](ioctl-battery-query-information.md) quando viene richiesto il livello di informazioni BatteryInformation.

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

Funzionalità della batteria. Questo membro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <dt>**BATTERIA \_ CAPACITY \_ RELATIVE**</dt> <dt>0x40000000</dt> </dl>                    | Indica che le informazioni sulla capacità e sulla frequenza della batteria sono relative e non in unità specifiche. Se questo bit non è impostato, le unità di report sono milliwatt-hours (mWh) per la capacità e milliwatt (mW) per la velocità. Se questo bit è impostato, tutti i riferimenti alle unità nell'altra documentazione della batteria possono essere ignorati. Tutte le informazioni sulla tariffa vengono segnalate in unità all'ora. Ad esempio, se la capacità completamente addebitata viene indicata come 100, una frequenza di 200 indica che la batteria userà tutta la capacità in mezz'ora.<br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <dt>**BATTERIA \_ IS \_ SHORT \_ TERM**</dt> <dt>0x20000000</dt> </dl>                               | Indica che l'operazione normale è per una funzione non sicura. Se questo bit non è impostato, si prevede che la batteria verrà usata durante il normale utilizzo del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <dt>**BATTERIA \_ SET \_ CHARGE \_ SUPPORTED**</dt> <dt>0x00000001</dt> </dl>          | Indica che le richieste di informazioni impostate di tipo BatteryCharge sono supportate da questo dispositivo a batteria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <dt>**BATTERIA \_ SET \_ DISCHARGE \_ SUPPORTED**</dt> <dt>0x00000002</dt> </dl> | Indica che le richieste di informazioni impostate di tipo BatteryDischarge sono supportate da questo dispositivo a batteria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <dt>**BATTERIA \_ BATTERIA \_ DI**</dt> <dt>SISTEMA 0x80000000</dt> </dl>                             | Indica che la batteria può fornire alimentazione generale per eseguire il sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Tecnologia**
</dt> <dd>

Tecnologia della batteria. Questo membro può essere uno dei valori seguenti.



| Valore                                                                        | Significato                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Batteria non ricaricabile, ad esempio alcaline.<br/> |
| <dl> <dt>1</dt> </dl> | Batteria ricaricabile, ad esempio l'acidità del lead.<br/>   |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**Chimica**
</dt> <dd>

Stringa di caratteri abbreviata che indica la chimica della batteria. Questa stringa non è necessariamente con terminazione zero. Di seguito è riportato un elenco parziale di abbreviazioni che possono essere restituite e delle chimica associate.



| Stringa Unicode                                                                                                                                           | Significato                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <dt>**PbAc**</dt> </dl> | Piombo<br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <dt>**Leone**</dt> </dl>                        | Ioni di litio<br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <dt>**Li-I**</dt> </dl> | Ioni di litio<br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <dt>**Nicd**</dt> </dl> | Nickel Cadmium<br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <dt>**Nimh**</dt> </dl> | Hydride nichel metal<br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <dt>**Nizn**</dt> </dl> | Nichel di zinco<br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <dt>**RAM**</dt> </dl>                           | Ricaricabile Alkaline-Manganese<br/> |



 

In futuro potrebbero comparire altre chimica e il codice dovrebbe essere in grado di gestirle.

</dd> <dt>

**DesignedCapacity**
</dt> <dd>

Capacità teorica della batteria quando è nuova, in mWh, a meno che BATTERY \_ CAPACITY RELATIVE non sia \_ impostata. In tal caso, le unità non sono definite.

</dd> <dt>

**FullChargedCapacity**
</dt> <dd>

Capacità corrente completamente carica della batteria in mWh (o relativa). Confrontare questo valore con **DesignedCapacity** per stimare l'usura della batteria.

</dd> <dt>

**DefaultAlert1**
</dt> <dd>

Capacità suggerita dal produttore, in mWh, in cui deve verificarsi un avviso di batteria in esaurimento. Le definizioni di basso variano da produttore a produttore. In generale, uno stato di avviso si verificherà prima di uno stato basso, ma non è consigliabile presupporre che lo sia sempre. Per ridurre il rischio di perdita di dati, questo valore viene in genere usato come impostazione predefinita per l'allarme batteria critica.

</dd> <dt>

**DefaultAlert2**
</dt> <dd>

Capacità suggerita dal produttore, in mWh, in cui deve verificarsi un avviso di batteria. Le definizioni di avviso variano da produttore a produttore. In generale, uno stato di avviso si verificherà prima di uno stato basso, ma non è consigliabile presupporre che lo sia sempre. Per ridurre il rischio di perdita di dati, questo valore viene in genere usato come impostazione predefinita per l'allarme batteria in esaurimento.

</dd> <dt>

**CriticalBias**
</dt> <dd>

Distorsione da zero, in mWh, applicata alla segnalazione della batteria. Alcune batterie riservano un piccolo addebito che viene sbilanciato in base ai valori di capacità della batteria per mostrare "0" come livello critico della batteria. La distorsione critica è analoga all'impostazione di un misuratore del carburante per mostrare "vuoto" quando sono rimasti diversi litro di carburante.

</dd> <dt>

**CycleCount**
</dt> <dd>

Numero di cicli di carica/scarica riscontrati dalla batteria. Ciò consente di determinare l'usura della batteria. Se la batteria non supporta un contatore del ciclo, questo membro è zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

In genere, uno stato di avviso si verifica prima di uno stato basso, ma non è consigliabile presupporre che lo sia. È possibile eseguire il polling di una batteria e scoprire che non si è verificato alcun livello di avviso, quindi eseguire nuovamente il polling della batteria e trovarla scaricata nella misura in cui entrambi i livelli sono stati raggiunti. Ciò potrebbe indicare che il polling non viene eseguito abbastanza spesso. Può anche indicare che la batteria non è in grado di contenere una carica per molto tempo e sta scaricando più rapidamente del previsto. Una batteria di questo tipo potrebbe essere prossima alla fine della sua vita utile o potrebbe essere danneggiata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI SULLE \_ QUERY SULLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




