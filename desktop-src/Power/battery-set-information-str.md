---
description: Contiene le informazioni sulla batteria da impostare.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: BATTERY_SET_INFORMATION struttura (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: c53e9c539f8ef20b184c6c056999c7c541f3c1718bafaa58c0b1e20dcef16a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143614"
---
# <a name="battery_set_information-structure"></a>Struttura BATTERY \_ SET \_ INFORMATION

Contiene le informazioni sulla batteria da impostare. Questa struttura viene usata con il codice [**di controllo IOCTL \_ BATTERY SET \_ \_ INFORMATION.**](ioctl-battery-set-information.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a>Members

<dl> <dt>

**BatteryTag**
</dt> <dd>

Tag della batteria corrente per la batteria. Le informazioni relative a una batteria corrispondente al tag possono essere restituite solo. Ogni volta che questo valore non corrisponde al tag corrente della batteria, la richiesta IOCTL verrà completata con ERROR FILE NOT FOUND, che indica al chiamante che la batteria per cui ha un tag per non esiste \_ \_ \_ più. Il chiamante può scegliere di usare [**l'operazione IOCTL \_ BATTERY QUERY \_ \_ TAG**](ioctl-battery-query-tag.md) per determinare il tag della batteria appena installata, se presente. Per altre [informazioni, vedere Tag](battery-information.md) della batteria.

Quando viene eseguita una richiesta di informazioni sulla query, questo valore viene verificato. Inoltre, se la richiesta è in corso mentre questo valore cambia, la richiesta viene interrotta con lo stato ERROR \_ FILE \_ NOT \_ FOUND.

</dd> <dt>

**InformationLevel**
</dt> <dd>

Informazioni sulla batteria da impostare. Il tipo di dati nel **membro Buffer** dipende dal valore di questo membro. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <dt>**BatteryCharge**</dt> <dt>1</dt> </dl>                         | Informa il dispositivo a batteria che l'utente ha richiesto che la batteria sia in carica in questo momento. Ad esempio, con una batteria/carica/selettore intelligente, l'applicazione potrebbe caricare una batteria alla volta. Il **membro Buffer** di questa struttura viene ignorato.<br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <dt>**BatteryCriticalBias**</dt> <dt>0</dt> </dl> | Imposta la regolazione della distorsione critica della batteria. Si noti che in genere questo valore viene modificato dal software ed è presente nelle interfacce solo come funzionalità di manutenzione. Non tutte le batterie possono mantenere tale impostazione e le informazioni sulla batteria devono essere lette per confermare che la batteria ha accettato l'impostazione.<br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <dt>**BatteryDischarge**</dt> <dt>2</dt> </dl>             | Informa il dispositivo a batteria che l'utente ha richiesto che la batteria sia scarica in questo momento. Ad esempio, questa opzione può essere usata per indicare la batteria che l'utente vuole attualmente alimentare nel sistema. Il **membro Buffer** di questa struttura viene ignorato.<br/>                                                                          |



 

</dd> <dt>

**Buffer**
</dt> <dd>

Informazioni sulla batteria da impostare. I dati dipendono dal valore di **InformationLevel.**

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura BATTERY SET \_ \_ INFORMATION** è una struttura a lunghezza variabile ed è necessario allocare un buffer di dimensioni adeguate per le informazioni da includere nella struttura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI SUL \_ SET DI \_ BATTERIA IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

 




