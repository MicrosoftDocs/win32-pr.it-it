---
title: Metodo UpdateFromDS della classe MicrosoftDNS_Zone
description: Il metodo UpdateFromDS forza un aggiornamento della zona dal servizio directory.
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- DNS del metodo UpdateFromDS
- Metodo UpdateFromDS DNS , MicrosoftDNS_Zone classe
- MicrosoftDNS_Zone classe DNS , metodo UpdateFromDS
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca537c6440ae14d0e15dea28f62bdb919f3ed7e3348f3a64a2339e0668b5c8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957190"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a>Metodo UpdateFromDS della classe MicrosoftDNS \_ Zone

Il **metodo UpdateFromDS** forza un aggiornamento della zona dal servizio directory.

## <a name="syntax"></a>Sintassi


```mof
void UpdateFromDS();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per eseguire correttamente questo metodo, ZoneType deve essere zero e la zona deve essere archiviata in DS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Zona \_ MicrosoftDNS**](microsoftdns-zone.md)
</dt> <dt>

[**Metodo AgeAllRecords della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Metodo ChangeZoneType della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Metodo CreateZone della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Metodo ForceRefresh della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Metodo GetDistinguishedName della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Metodo PauseZone della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Metodo ReloadZone della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Metodo ResetSecondaries della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Metodo ResumeZone della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Metodo WriteBackZone della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





