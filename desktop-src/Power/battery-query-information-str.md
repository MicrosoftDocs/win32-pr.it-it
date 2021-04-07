---
description: Contiene informazioni sulle query della batteria.
ms.assetid: ef5466fe-7de8-48cd-ad48-5774d7a4bb46
title: Struttura BATTERY_QUERY_INFORMATION (Poclass. h)
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
ms.openlocfilehash: 511980dd4307077b8b160550c661a15a5714b96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881729"
---
# <a name="battery_query_information-structure"></a>\_ \_ Struttura delle informazioni sulle query della batteria

Contiene informazioni sulle query della batteria. Questa struttura viene utilizzata con il codice di controllo delle [**\_ informazioni di \_ query \_ della batteria IOCTL**](ioctl-battery-query-information.md) per specificare il tipo di informazioni da restituire.

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

Tag della batteria corrente per la batteria. Possono essere restituite solo le informazioni per una batteria corrispondente al tag. Ogni volta che questo valore non corrisponde al tag corrente della batteria, la richiesta IOCTL verrà completata con il \_ file di errore \_ non \_ trovato. Indica al chiamante che la batteria associata al tag esiste più. Il chiamante può scegliere di usare l'operazione di [**\_ tag di \_ query \_ della batteria IOCTL**](ioctl-battery-query-tag.md) per determinare il tag della batteria appena installata, se disponibile. Per ulteriori informazioni, vedere la pagina relativa ai [tag della batteria](battery-information.md) .

Quando viene eseguita una richiesta di informazioni sulle query, questo valore viene verificato. Inoltre, se la richiesta è in corso mentre questo valore viene modificato, la richiesta viene interrotta con lo stato del file di errore \_ \_ non \_ trovato.

</dd> <dt>

**InformationLevel**
</dt> <dd>

Livello delle informazioni sulla batteria sottoposte a query. I dati restituiti dall'IOCTL dipendono da questo valore. Il membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryDeviceName"></span><span id="batterydevicename"></span><span id="BATTERYDEVICENAME"></span><dl> <dt>**BatteryDeviceName**</dt> <dt>4</dt> </dl>                                                 | Stringa Unicode con terminazione null che contiene il nome della batteria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="BatteryEstimatedTime"></span><span id="batteryestimatedtime"></span><span id="BATTERYESTIMATEDTIME"></span><dl> <dt>**BatteryEstimatedTime**</dt> <dt>3</dt> </dl>                                     | **ULONG** che specifica il tempo di esecuzione stimato della batteria, in secondi. Se la frequenza di svuotamento fornita nel membro **AtRate** della struttura di **\_ \_ informazioni sulle query della batteria** è zero, questo calcolo è basato sulla velocità attuale di svuotamento. Se **AtRate** è diverso da zero, l'ora restituita è il tempo di esecuzione previsto per la velocità specificata. Se il tempo stimato è sconosciuto (ad esempio, la batteria non viene ricaricata e il **AtRate** specificato è zero), il valore restituito è l' \_ ora sconosciuta della batteria \_ . Si noti che questo valore non è molto accurato in alcuni sistemi di batteria e può variare notevolmente a seconda del consumo di energia attuale, che può essere influenzato dall'attività del disco e da altri fattori. Non esiste alcun meccanismo di notifica delle modifiche in questo valore.<br/> |
| <span id="BatteryGranularityInformation"></span><span id="batterygranularityinformation"></span><span id="BATTERYGRANULARITYINFORMATION"></span><dl> <dt>**BatteryGranularityInformation**</dt> <dt>1</dt> </dl> | Una matrice di strutture di [**\_ \_ scalabilità di report della batteria**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) , mai più di quattro voci.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BatteryInformation"></span><span id="batteryinformation"></span><span id="BATTERYINFORMATION"></span><dl> <dt>**BatteryInformation**</dt> <dt>0</dt> </dl>                                             | Struttura [**\_ delle informazioni sulla batteria**](battery-information-str.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BatteryManufactureDate"></span><span id="batterymanufacturedate"></span><span id="BATTERYMANUFACTUREDATE"></span><dl> <dt>**BatteryManufactureDate**</dt> <dt>5</dt> </dl>                             | Struttura [**della \_ \_ Data di produzione della batteria**](battery-manufacture-date-str.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="BatteryManufactureName"></span><span id="batterymanufacturename"></span><span id="BATTERYMANUFACTURENAME"></span><dl> <dt>**BatteryManufactureName**</dt> <dt>6</dt> </dl>                             | Stringa Unicode con terminazione null che specifica il nome del produttore della batteria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatterySerialNumber"></span><span id="batteryserialnumber"></span><span id="BATTERYSERIALNUMBER"></span><dl> <dt>**BatterySerialNumber**</dt> <dt>8</dt> </dl>                                         | Stringa Unicode con terminazione null che specifica il numero di serie della batteria.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryTemperature"></span><span id="batterytemperature"></span><span id="BATTERYTEMPERATURE"></span><dl> <dt>**BatteryTemperature**</dt> <dt>2</dt> </dl>                                             | **ULONG** che specifica la temperatura corrente della batteria, in decimi di grado Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryUniqueID"></span><span id="batteryuniqueid"></span><span id="BATTERYUNIQUEID"></span><dl> <dt>**BatteryUniqueID**</dt> <dt>7</dt> </dl>                                                         | Stringa Unicode con terminazione null che identifica in modo univoco la batteria. Questo valore può essere usato per tenere traccia di una batteria specifica. Nel caso di batterie intelligenti, questo ID è la concatenazione del nome del produttore, del nome del dispositivo, della data di produzione e di una rappresentazione stampabile del numero di serie. <br/> Questo valore non può essere visualizzato all'utente.<br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**AtRate**
</dt> <dd>

Questo membro viene usato solo se **InformationLevel** è BatteryEstimatedTime.

Se questo membro è diverso da zero, si tratta di una frequenza di svuotamento che verrà usata per calcolare il tempo fino a quando la batteria non viene caricata per la BatteryEstimatedTime di una singola batteria. Deve essere specificato in mW e deve essere un valore negativo per rappresentare una velocità di scaricamento della batteria.

</dd> </dl>

## <a name="remarks"></a>Commenti

Alcune informazioni sulle batterie sono facoltative o potrebbero non essere significative per alcune batterie. Se il tipo specifico di dati richiesti non è disponibile per la batteria corrente, \_ \_ viene restituita la funzione Error non valida.

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

[**\_Data di produzione della batteria \_**](battery-manufacture-date-str.md)
</dt> <dt>

[**\_ \_ scalabilità report batteria**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**\_ \_ informazioni sulle query della batteria IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_tag di \_ query della batteria IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

 




