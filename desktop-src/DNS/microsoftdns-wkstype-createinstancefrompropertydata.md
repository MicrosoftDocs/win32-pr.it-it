---
title: Metodo CreateInstanceFromPropertyData della MicrosoftDNS_WKSType classe
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse Well-Known Services (WKS).
ms.assetid: 6d910716-74f9-48a0-b43c-3243f5518caf
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- Metodo CreateInstanceFromPropertyData DNS, MicrosoftDNS_WKSType classe
- MicrosoftDNS_WKSType classe DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 892e0fbd6d39d794c074c5070ac6065d4be8a1b3ed5cd8e9d7610021589aa2b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109071"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_wkstype-class"></a>Metodo CreateInstanceFromPropertyData della classe WKSType MicrosoftDNS \_

Il **metodo CreateInstanceFromPropertyData** crea un'istanza di un record Well-Known Services (WKS).

## <a name="syntax"></a>Sintassi


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               InternetAddress,
  [in]           string               IPProtocol,
  [in]           string               Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DnsServerName* \[ Pollici\]
</dt> <dd>

FQDN o indirizzo IP del server DNS che contiene questo RR.

</dd> <dt>

*ContainerName* \[ Pollici\]
</dt> <dd>

Nome del contenitore per l'istanza di Zone, Cache o RootHints che contiene questo RR.

</dd> <dt>

*OwnerName* \[ Pollici\]
</dt> <dd>

Nome del proprietario per RR.

</dd> <dt>

*RecordClass* \[ in, facoltativo\]
</dt> <dd>

Classe di RR. Il valore predefinito è 1. I valori seguenti sono validi.



| Valore                                                                                                | Significato                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*InternetAddress* \[ Pollici\]
</dt> <dd>

Indirizzo IP Internet per il proprietario del record.

</dd> <dt>

*IpProtocol* \[ Pollici\]
</dt> <dd>

Stringa che rappresenta il protocollo IP per questo record. I valori validi sono UDP o TCP.

</dd> <dt>

*Servizi* \[ Pollici\]
</dt> <dd>

Stringa contenente tutti i servizi usati dal record well known service (WKS).

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Riferimento al nuovo oggetto .

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

[**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)
</dt> <dt>

[**Metodo Modify della classe \_ WKSType MicrosoftDNS**](microsoftdns-wkstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





