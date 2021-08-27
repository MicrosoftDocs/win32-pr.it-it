---
title: Metodo CreateInstanceFromPropertyData della MicrosoftDNS_WINSType classe
description: Il metodo CreateInstanceFromPropertyData crea un'istanza Windows record di risorse WINS (Internet Name Service).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- Metodo CreateInstanceFromPropertyData DNS, MicrosoftDNS_WINSType classe
- MicrosoftDNS_WINSType classe DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f39b360c29ca859c0d0fd0188f0b065dec58293207c27e0a0267572472aabe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077051"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a>Metodo CreateInstanceFromPropertyData della classe WINSType MicrosoftDNS \_

Il **metodo CreateInstanceFromPropertyData** crea un'istanza Windows record di risorse WINS (Internet Name Service).

## <a name="syntax"></a>Sintassi


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
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

*MappingFlag* \[ Pollici\]
</dt> <dd>

Flag di mapping WINS che specifica se il record deve essere incluso nella replica di zona. Può avere solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale). I valori seguenti sono validi.



| Valore                                                                                                                                               | Significato                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Flag di replica<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Flag di nessuna replica (record locale)<br/> |



 

</dd> <dt>

*LookupTimeout* \[ Pollici\]
</dt> <dd>

Tempo, in secondi, in cui un server DNS tenta di eseguire la risoluzione usando WINS Cerca.

</dd> <dt>

*CacheTimeout* \[ Pollici\]
</dt> <dd>

Tempo, in secondi, in cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.

</dd> <dt>

*WinsServers* \[ Pollici\]
</dt> <dd>

Elenco di indirizzi IP delimitati da virgole dei server WINS usati nelle ricerca WINS.

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

[**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)
</dt> <dt>

[**Metodo Modify della classe \_ WINSType MicrosoftDNS**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





