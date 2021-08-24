---
description: Contiene informazioni sulla query della batteria.
ms.assetid: ef5466fe-7de8-48cd-ad48-5774d7a4bb46
title: BATTERY_QUERY_INFORMATION struttura (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 9049517108cbb31df1164cc88640a78e104e2902d3a8a4b8dec4b8bfb48e8a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143684"
---
# <a name="battery_query_information-structure"></a>STRUTTURA DELLE \_ INFORMAZIONI \_ SULLE QUERY BATTERY

Contiene informazioni sulla query della batteria. Questa struttura viene usata con il codice [**di controllo IOCTL \_ BATTERY QUERY \_ \_ INFORMATION**](ioctl-battery-query-information.md) per specificare il tipo di informazioni da restituire.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _BATTERY_QUERY_INFORMATION {
  ULONG                           BatteryTag;
  BATTERY_QUERY_INFORMATION_LEVEL InformationLevel;
  LONG                            AtRate;
} BATTERY_QUERY_INFORMATION, *PBATTERY_QUERY_INFORMATION;
```



## <a name="members"></a>Members

<dl> <dt>

**BatteryTag**
</dt> <dd>

Tag della batteria corrente per la batteria. È possibile restituire solo le informazioni relative a una batteria corrispondente al tag. Ogni volta che questo valore non corrisponde al tag corrente della batteria, la richiesta IOCTL verrà completata con ERRORE \_ FILE \_ NON \_ TROVATO. Ciò indica al chiamante che la batteria associata al tag esiste più a lungo. Il chiamante può scegliere di usare [**l'operazione IOCTL \_ BATTERY QUERY \_ \_ TAG**](ioctl-battery-query-tag.md) per determinare il tag della batteria appena installata, se presente. Per altre [informazioni, vedere Tag](battery-information.md) della batteria.

Quando viene eseguita una richiesta di informazioni sulla query, questo valore viene verificato. Inoltre, se la richiesta è in corso mentre questo valore cambia, la richiesta viene interrotta con lo stato ERROR \_ FILE \_ NOT \_ FOUND.

</dd> <dt>

**InformationLevel**
</dt> <dd>

Livello delle informazioni sulla batteria su cui viene eseguita la query. I dati restituiti da IOCTL dipendono da questo valore. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryDeviceName"></span><span id="batterydevicename"></span><span id="BATTERYDEVICENAME"></span><dl> <dt>**BatteryDeviceName**</dt> <dt>4</dt> </dl>                                                 | Stringa Unicode con terminazione Null che contiene il nome della batteria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="BatteryEstimatedTime"></span><span id="batteryestimatedtime"></span><span id="BATTERYESTIMATEDTIME"></span><dl> <dt>**BatteryEstimatedTime**</dt> <dt>3</dt> </dl>                                     | Valore **ULONG** che specifica il tempo stimato di esecuzione della batteria, espresso in secondi. Se la frequenza di svuotamento fornita nel membro **AtRate** della struttura **BATTERY QUERY \_ \_ INFORMATION** è zero, questo calcolo si basa sulla frequenza corrente di svuotamento. Se **AtRate** è diverso da zero, il tempo restituito è il tempo di esecuzione previsto per la frequenza specificata. Se il tempo stimato è sconosciuto (ad esempio, la batteria non viene scaricata e il valore **AtRate** specificato è zero), il valore restituito è BATTERY \_ UNKNOWN \_ TIME. Si noti che questo valore non è molto accurato in alcuni sistemi a batteria e può variare notevolmente a seconda dell'attuale utilizzo dell'alimentazione, che potrebbe essere influenzato dall'attività del disco e da altri fattori. Non esiste alcun meccanismo di notifica per le modifiche apportate a questo valore.<br/> |
| <span id="BatteryGranularityInformation"></span><span id="batterygranularityinformation"></span><span id="BATTERYGRANULARITYINFORMATION"></span><dl> <dt>**BatteryGranularityInformation**</dt> <dt>1</dt> </dl> | Matrice di strutture [**BATTERY \_ REPORTING \_ SCALE,**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) mai più di quattro voci.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BatteryInformation"></span><span id="batteryinformation"></span><span id="BATTERYINFORMATION"></span><dl> <dt>**BatteryInformation**</dt> <dt>0</dt> </dl>                                             | Struttura [**BATTERY \_ INFORMATION.**](battery-information-str.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BatteryManufactureDate"></span><span id="batterymanufacturedate"></span><span id="BATTERYMANUFACTUREDATE"></span><dl> <dt>**BatteryManufactureDate**</dt> <dt>5</dt> </dl>                             | Struttura [**BATTERY \_ MANUFACTURE \_ DATE.**](battery-manufacture-date-str.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="BatteryManufactureName"></span><span id="batterymanufacturename"></span><span id="BATTERYMANUFACTURENAME"></span><dl> <dt>**BatteryManufactureName**</dt> <dt>6</dt> </dl>                             | Stringa Unicode con terminazione Null che specifica il nome del produttore della batteria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatterySerialNumber"></span><span id="batteryserialnumber"></span><span id="BATTERYSERIALNUMBER"></span><dl> <dt>**BatterySerialNumber**</dt> <dt>8</dt> </dl>                                         | Stringa Unicode con terminazione Null che specifica il numero di serie della batteria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryTemperature"></span><span id="batterytemperature"></span><span id="BATTERYTEMPERATURE"></span><dl> <dt>**BatteryTemperature**</dt> <dt>2</dt> </dl>                                             | **ULONG** che specifica la temperatura corrente della batteria, in 10° di grado Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryUniqueID"></span><span id="batteryuniqueid"></span><span id="BATTERYUNIQUEID"></span><dl> <dt>**BatteryUniqueID**</dt> <dt>7</dt> </dl>                                                         | Stringa Unicode con terminazione Null che identifica in modo univoco la batteria. Questo valore può essere usato per tenere traccia di una batteria specifica. Nel caso di batterie intelligenti, questo ID è la concatenazione del nome del produttore, del nome del dispositivo, della data di produzione e di una rappresentazione stampabile del numero di serie. <br/> Questo valore non deve essere visualizzato all'utente.<br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**AtRate**
</dt> <dd>

Questo membro viene usato solo se **InformationLevel** è BatteryEstimatedTime.

Se questo membro è diverso da zero, si tratta di una frequenza di svuotamento che verrà usata per calcolare il tempo fino a quando la batteria non viene scaricata per BatteryEstimatedTime di una singola batteria. Deve essere specificato in mW e deve essere un valore negativo per rappresentare una frequenza di batteria.

</dd> </dl>

## <a name="remarks"></a>Commenti

Alcune informazioni sulle batterie sono facoltative o potrebbero non essere importanti per alcune batterie. Se il particolare tipo di dati richiesto non è disponibile per la batteria corrente, viene restituito ERROR \_ INVALID \_ FUNCTION.

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

[**DATA \_ DI PRODUZIONE DELLA \_ BATTERIA**](battery-manufacture-date-str.md)
</dt> <dt>

[**SCALA PER \_ LA SEGNALAZIONE \_ DELLA BATTERIA**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**INFORMAZIONI SULLA \_ QUERY DELLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**TAG DI \_ QUERY DELLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

 




