---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_WINSRType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse WINS Reverse Lookup (WINSR).
ms.assetid: e14e81be-fc5c-4a6f-b6d1-cb3ce5005e00
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- Metodo CreateInstanceFromPropertyData DNS, MicrosoftDNS_WINSRType classe
- MicrosoftDNS_WINSRType classe DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8bc5103c9a7034b79500496cc7a066c1fbc65aa32d20dd29ea3160dfbaf0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162942"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winsrtype-class"></a>Metodo CreateInstanceFromPropertyData della classe \_ MICROSOFTDNS WINSRType

Il **metodo CreateInstanceFromPropertyData** crea un'istanza di un record di risorse WINS Reverse Lookup (WINSR).

## <a name="syntax"></a>Sintassi


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint32                 MappingFlag,
  [in]           uint32                 LookupTimeout,
  [in]           uint32                 CacheTimeout,
  [in]           string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
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

Nome del contenitore per l'istanza di Zona, Cache o RootHints che contiene questo RR.

</dd> <dt>

*OwnerName* \[ Pollici\]
</dt> <dd>

Nome del proprietario per il RR.

</dd> <dt>

*RecordClass* \[ in, facoltativo\]
</dt> <dd>

Classe dell'oggetto RR. Il valore predefinito è 1. I valori seguenti sono validi.



| Valore                                                                                                | Significato                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*MappingFlag* \[ Pollici\]
</dt> <dd>

Flag di mapping WINSR che specifica se il record deve essere incluso nella replica di zona. Può avere solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale).

</dd> <dt>

*LookupTimeout* \[ Pollici\]
</dt> <dd>

Timeout, in secondi, per un server DNS che usa la ricerca inversa WINS.

</dd> <dt>

*CacheTimeout* \[ Pollici\]
</dt> <dd>

Tempo, in secondi, un server DNS che usa WINS Look up può memorizzare nella cache la risposta del server WINS.

</dd> <dt>

*ResultDomain* \[ Pollici\]
</dt> <dd>

Nome di dominio da aggiungere ai nomi NetBIOS restituiti.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Riferimento al nuovo oggetto.

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

[**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md)
</dt> <dt>

[**Metodo Modify della classe MICROSOFTDNS \_ WINSRType**](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





