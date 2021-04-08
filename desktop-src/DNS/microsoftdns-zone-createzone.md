---
title: Metodo CreateZone della classe MicrosoftDNS_Zone
description: Il Metodo CreateZone crea una zona DNS.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- DNS del Metodo CreateZone
- DNS del Metodo CreateZone, classe MicrosoftDNS_Zone
- Classe MicrosoftDNS_Zone DNS, Metodo CreateZone
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048540"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a>Metodo CreateZone della classe di \_ zona MicrosoftDNS

Il metodo **CreateZone** crea una zona DNS.

## <a name="syntax"></a>Sintassi


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Zonename* \[ in\]
</dt> <dd>

Stringa che rappresenta il nome della zona.

</dd> <dt>

*ZoneType* \[ in\]
</dt> <dd>

Tipo di zona. Di seguito sono riportati i valori validi:



| Valore                                                                        | Significato                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>1</dt> </dl> | Integrazione con Active Directory.<br/>                                                                                           |
| <dl> <dt>2</dt> </dl> | Zona secondaria.<br/>                                                                                          |
| <dl> <dt>3</dt> </dl> | Area stub.<br/> **Windows Server 2003:** Questo tipo di zona è stato introdotto in Windows Server 2003.<br/>      |
| <dl> <dt>4</dt> </dl> | Server d'avanzamento della zona.<br/> **Windows Server 2003:** Questo tipo di zona è stato introdotto in Windows Server 2003.<br/> |



 

</dd> <dt>

*DsIntegrated* \[ in\]
</dt> <dd>

Indica se i dati della zona vengono archiviati nel Active Directory o nei file. Se TRUE, i dati vengono archiviati nella Active Directory; Se FALSE, i dati vengono archiviati in file.

</dd> <dt>

*DataFileName* \[ in, facoltativo\]
</dt> <dd>

Nome del file di dati associato alla zona.

</dd> <dt>

*IpAddr* \[ in, facoltativo\]
</dt> <dd>

Indirizzo IP del server DNS master per la zona.

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

[**Metodo ChangeZoneType della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
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

 

 





