---
description: Contiene le informazioni sulla batteria da impostare.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: Struttura BATTERY_SET_INFORMATION (Poclass. h)
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
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131674"
---
# <a name="battery_set_information-structure"></a>\_ \_ Struttura delle informazioni sui set di batterie

Contiene le informazioni sulla batteria da impostare. Questa struttura viene utilizzata con il codice di controllo [**\_ \_ \_ delle informazioni del set di batterie IOCTL**](ioctl-battery-set-information.md) .

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

Tag della batteria corrente per la batteria. Le informazioni per una batteria che corrispondono al tag possono essere restituite solo. Ogni volta che questo valore non corrisponde al tag corrente della batteria, la richiesta IOCTL viene completata con il \_ file di errore \_ non \_ trovato, che indica al chiamante che la batteria per cui è presente un tag non esiste più. Il chiamante può scegliere di usare l'operazione di [**\_ tag di \_ query \_ della batteria IOCTL**](ioctl-battery-query-tag.md) per determinare il tag della batteria appena installata, se disponibile. Per ulteriori informazioni, vedere la pagina relativa ai [tag della batteria](battery-information.md) .

Quando viene eseguita una richiesta di informazioni sulle query, questo valore viene verificato. Inoltre, se la richiesta è in corso mentre questo valore viene modificato, la richiesta viene interrotta con lo stato del file di errore \_ \_ non \_ trovato.

</dd> <dt>

**InformationLevel**
</dt> <dd>

Informazioni sulla batteria da impostare. Il tipo di dati nel membro del **buffer** dipende dal valore di questo membro. Il membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <dt>**BatteryCharge**</dt> <dt>1</dt> </dl>                         | Informa il dispositivo della batteria che l'utente ha richiesto la ricarica della batteria in questo momento. Ad esempio, con uno Smart Battery/Charger/Selector, l'applicazione potrebbe addebitare una batteria alla volta. Il membro **buffer** di questa struttura viene ignorato.<br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <dt>**BatteryCriticalBias**</dt> <dt>0</dt> </dl> | Imposta la regolazione della distorsione critica della batteria. Si noti che non è previsto che questo valore venga normalmente modificato dal software ed è presente nelle interfacce solo come funzionalità di manutenzione. Non tutte le batterie possono mantenere questa impostazione e le informazioni sulla batteria devono essere lette per confermare che la batteria ha accettato l'impostazione.<br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <dt>**BatteryDischarge**</dt> <dt>2</dt> </dl>             | Informa il dispositivo della batteria che l'utente ha richiesto di scaricare la batteria in questo momento. Ad esempio, questo può essere usato per indicare la batteria che l'utente attualmente vuole potenziare al sistema. Il membro **buffer** di questa struttura viene ignorato.<br/>                                                                          |



 

</dd> <dt>

**Buffer**
</dt> <dd>

Informazioni sulla batteria da impostare. I dati dipendono dal valore di **InformationLevel**.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura delle **\_ \_ informazioni sul set di batterie** è una struttura a lunghezza variabile ed è necessario allocare un buffer di dimensioni appropriate per le informazioni da includere nella struttura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ informazioni sui set di batterie IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

 




