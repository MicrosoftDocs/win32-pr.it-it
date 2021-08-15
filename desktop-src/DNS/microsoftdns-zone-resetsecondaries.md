---
title: Metodo ResetSecondaries della classe MicrosoftDNS_Zone
description: Il metodo ResetSecondaries reimposta gli indirizzi IP per i server DNS secondari nella zona.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- DNS del metodo ResetSecondaries
- Metodo ResetSecondaries DNS , MicrosoftDNS_Zone classe
- MicrosoftDNS_Zone classe DNS, metodo ResetSecondaries
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ab3737bc8143f712560e5ea253237c97da4e2401b98886428642210805ca586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957290"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a>Metodo ResetSecondaries della classe MicrosoftDNS \_ Zone

Il **metodo ResetSecondaries** reimposta gli indirizzi IP per i server DNS secondari nella zona.

## <a name="syntax"></a>Sintassi


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SecondaryServers* \[ Pollici\]
</dt> <dd>

Matrice di indirizzi IP per i server DNS secondari.

</dd> <dt>

*SecureSecondaries* \[ Pollici\]
</dt> <dd>

Specifica la sicurezza da applicare e deve essere una delle seguenti:

-   ZONA \_ SECSECURE \_ NO \_ SECURITY
-   SOLO \_ \_ NS ZONE SECSECURE \_
-   SOLO \_ ELENCO ZONE SECSECURE \_ \_
-   ZONA \_ SECSECURE \_ NO \_ XFR

</dd> <dt>

*NotifyServers* \[ Pollici\]
</dt> <dd>

Indirizzo IP dei server DNS da notificare quando la zona cambia.

</dd> <dt>

*Notifica* \[ Pollici\]
</dt> <dd>

L'impostazione di notifica e deve essere una delle seguenti:

-   NOTIFICA \_ ZONA \_ DISATTIVATA
-   ZONE \_ NOTIFY \_ ALL SECONDARIES (NOTIFICA A \_ TUTTI I DATABASE SECONDARI)
-   SOLO ELENCO \_ \_ NOTIFICHE \_ ZONA

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

RR di tipo [**MicrosoftDNS \_ Zone**](microsoftdns-zone.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Area \_ MicrosoftDNS**](microsoftdns-zone.md)
</dt> <dt>

[**Metodo AgeAllRecords della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Metodo ChangeZoneType della classe Zona \_ MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Metodo CreateZone della classe Zona \_ MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Metodo ForceRefresh della classe Zona \_ MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Metodo GetDistinguishedName della classe Zona \_ MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Metodo PauseZone della classe Zona \_ MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Metodo ReloadZone della classe Zona \_ MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Metodo ResumeZone della classe Zona \_ MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Metodo UpdateFromDS della classe zona \_ MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Metodo WriteBackZone della classe Zona \_ MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





