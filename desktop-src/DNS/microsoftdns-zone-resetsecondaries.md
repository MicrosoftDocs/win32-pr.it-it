---
title: Metodo ResetSecondaries della classe MicrosoftDNS_Zone
description: Il metodo ResetSecondaries Reimposta gli indirizzi IP per i server DNS secondari nella zona.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- DNS del metodo ResetSecondaries
- DNS del metodo ResetSecondaries, classe MicrosoftDNS_Zone
- Classe MicrosoftDNS_Zone DNS, metodo ResetSecondaries
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
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964539"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a>Metodo ResetSecondaries della classe di \_ zona MicrosoftDNS

Il metodo **ResetSecondaries** Reimposta gli indirizzi IP per i server DNS secondari nella zona.

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

*SecondaryServers* \[ in\]
</dt> <dd>

Matrice di indirizzi IP per i server DNS secondari.

</dd> <dt>

*SecureSecondaries* \[ in\]
</dt> <dd>

Specifica la sicurezza da applicare e deve essere uno dei seguenti:

-   SECSECURE della zona \_ \_ senza \_ sicurezza
-   ZONA \_ \_ solo NS \_ SECSECURE
-   \_ \_ solo elenco SECSECURE \_ zona
-   AREA \_ SECSECURE \_ No \_ XFR

</dd> <dt>

*NotifyServers* \[ in\]
</dt> <dd>

Indirizzo IP dei server DNS a cui ricevere una notifica in caso di modifica della zona.

</dd> <dt>

*Invia notifica* \[ in\]
</dt> <dd>

L'impostazione di notifica deve essere una delle seguenti:

-   \_notifica zona \_ disattivata
-   notifica zona a \_ \_ tutti i database \_ secondari
-   \_ \_ solo elenco notifiche \_ zone

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

RR di tipo [**\_ zona MicrosoftDNS**](microsoftdns-zone.md).

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

[**Metodo ResumeZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Metodo UpdateFromDS della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Metodo WriteBackZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





