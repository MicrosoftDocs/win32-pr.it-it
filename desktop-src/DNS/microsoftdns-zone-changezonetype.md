---
title: Metodo ChangeZoneType della classe MicrosoftDNS_Zone
description: Il metodo ChangeZoneType modifica il tipo di una zona.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- DNS del metodo ChangeZoneType
- DNS del metodo ChangeZoneType, classe MicrosoftDNS_Zone
- Classe MicrosoftDNS_Zone DNS, metodo ChangeZoneType
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048242"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a>Metodo ChangeZoneType della classe di \_ zona MicrosoftDNS

Il metodo **ChangeZoneType** modifica il tipo di una zona.

## <a name="syntax"></a>Sintassi


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ZoneType* \[ in\]
</dt> <dd>

Tipo di zona. Di seguito sono riportati i valori validi:



| Valore                                                                        | Significato                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl> | Zona primaria.<br/>   |
| <dl> <dt>1</dt> </dl> | Zona secondaria.<br/> |
| <dl> <dt>2</dt> </dl> | Area stub.<br/>      |
| <dl> <dt>3</dt> </dl> | Server d'avanzamento della zona.<br/> |



 

</dd> <dt>

*DataFileName* \[ in, facoltativo\]
</dt> <dd>

Nome del file di dati associato alla zona.

</dd> <dt>

*IpAddr* \[ in, facoltativo\]
</dt> <dd>

Indirizzo IP del server DNS Mater per la zona.

</dd> <dt>

*AdminEmailName* \[ in, facoltativo\]
</dt> <dd>

Indirizzo di posta elettronica dell'amministratore responsabile della zona.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

RR di tipo **\_ zona MicrosoftDns**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Zona MicrosoftDNS**](microsoftdns-zone.md)
</dt> <dt>

[**Metodo AgeAllRecords della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Metodo CreateZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Metodo ForceRefresh della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Metodo getdistinguishname della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Metodo PauseZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Metodo ReloadZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Metodo ResetSecondaries della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Metodo ResumeZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Metodo UpdateFromDS della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Metodo WriteBackZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





