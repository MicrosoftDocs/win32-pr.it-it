---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_SRVType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse del servizio (SRV).
ms.assetid: ef55faa8-1109-4c96-98ac-2b01b940fa5c
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_SRVType
- Classe MicrosoftDNS_SRVType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 607ed606bf12e9e2a6f90a6e7f309aa708b7f230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743383"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_srvtype-class"></a>Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SRVType

Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse del servizio (SRV).

## <a name="syntax"></a>Sintassi


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Priority,
  [in]           uint16               Weight,
  [in]           uint16               Port,
  [in]           string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
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

*Priorità* \[ di in\]
</dt> <dd>

Priorità dell'host di destinazione specificato nel nome del proprietario. I numeri più bassi implicano priorità più elevate.

</dd> <dt>

*Peso* \[ in\]
</dt> <dd>

Peso dell'host di destinazione. Questa operazione è utile quando si seleziona tra gli host con la stessa priorità. La possibilità di utilizzare questo host deve essere proporzionale al suo peso.

</dd> <dt>

*Porta* \[ in\]
</dt> <dd>

Porta utilizzata nell'host di destinazione di un servizio del protocollo.

</dd> <dt>

*SRVDomainName* \[ in\]
</dt> <dd>

FQDN dell'host di destinazione. Destinazione di \\ . \\ indica che il servizio non è disponibile in questo dominio.

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

[**\_SRVType MicrosoftDNS**](microsoftdns-srvtype.md)
</dt> <dt>

[**Metodo Modify della \_ classe SRVType di MicrosoftDNS**](microsoftdns-srvtype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





