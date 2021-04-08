---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_X25Type
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse X. 25 (x25).
ms.assetid: fe89f829-79b9-457e-b455-899b2706ef04
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_X25Type
- Classe MicrosoftDNS_X25Type DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f198bf7b843b5633acd0b1515e9e3573f5ebb55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048511"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_x25type-class"></a>Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ X25Type

Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse X. 25 (x25).

## <a name="syntax"></a>Sintassi


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
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

*PSDNAddress* \[ in\]
</dt> <dd>

Indirizzo PSDN del proprietario dell'RR.

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

[**\_X25Type MicrosoftDNS**](microsoftdns-x25type.md)
</dt> <dt>

[**Metodo Modify della \_ classe X25Type di MicrosoftDNS**](microsoftdns-x25type-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





