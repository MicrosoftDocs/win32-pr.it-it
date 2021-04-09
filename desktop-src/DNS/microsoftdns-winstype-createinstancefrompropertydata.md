---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_WINSType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse WINS (Windows Internet Name Service).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_WINSType
- Classe MicrosoftDNS_WINSType DNS, metodo CreateInstanceFromPropertyData
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
ms.openlocfilehash: bf584bd34f59391a49fd5f7ec13cb49e18ef68fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742247"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a>Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WINSType

Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse WINS (Windows Internet Name Service).

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

*DnsServerName* \[ in\]
</dt> <dd>

FQDN o indirizzo IP del server DNS che contiene questo RR.

</dd> <dt>

*ContainerName* \[ in\]
</dt> <dd>

Nome del contenitore per la zona, la cache o l'istanza di RootHints che contiene questo RR.

</dd> <dt>

*Proprietarioname* \[ in\]
</dt> <dd>

Nome del proprietario per l'RR.

</dd> <dt>

*RecordClass* \[ in, facoltativo\]
</dt> <dd>

Classe dell'RR. Il valore predefinito è 1. I valori seguenti sono validi.



| Valore                                                                                                | Significato                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Esiodo)<br/>   |



 

</dd> <dt>

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*MappingFlag* \[ in\]
</dt> <dd>

Flag di mapping WINS che specifica se il record deve essere incluso nella replica della zona. Potrebbero essere presenti solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale). I valori seguenti sono validi.



| Valore                                                                                                                                               | Significato                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Flag di replica<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Flag senza replica (record locale)<br/> |



 

</dd> <dt>

*LookupTimeout* \[ in\]
</dt> <dd>

Tempo, in secondi, durante il quale un server DNS tenta la risoluzione usando la ricerca di WINS.

</dd> <dt>

*CacheTimeout* \[ in\]
</dt> <dd>

Tempo, in secondi, per cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.

</dd> <dt>

*WinsServers* \[ in\]
</dt> <dd>

Elenco di indirizzi IP delimitati da virgole dei server WINS utilizzati nelle ricerche WINS.

</dd> <dt>

*RR* \[ out, Ref\]
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
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_WINSType MicrosoftDNS**](microsoftdns-winstype.md)
</dt> <dt>

[**Metodo Modify della \_ classe WINSType di MicrosoftDNS**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





