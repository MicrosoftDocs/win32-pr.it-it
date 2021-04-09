---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_AFSDBType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse del server di database di file System Andrew (AFSDB).
ms.assetid: 2cd0434d-0c18-468f-95f3-7a77375596a3
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_AFSDBType
- Classe MicrosoftDNS_AFSDBType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04efd6e18ef4267d9887252f91e8a215fcf3ee88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964230"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_afsdbtype-class"></a>Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ AFSDBType

Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse del server di database di file System Andrew (AFSDB).

## <a name="syntax"></a>Sintassi


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint16                 Subtype,
  [in]           string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
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

*Sottotipo* \[ in\]
</dt> <dd>

Sottotipo del server AFS host. Per il sottotipo 1 (valore = 1), l'host dispone di un server del percorso del volume AFS versione 3,0 per la cella AFS denominata. Nel caso del sottotipo 2 (valore = 2), l'host dispone di un server dei nomi autenticato che contiene il nodo della directory radice della cella per la cella DCE/autorità di certificazione denominata.

</dd> <dt>

*Nomeserver* \[ in\]
</dt> <dd>

FQDN che specifica un host con un server per la cella AFS specificata nel nome del proprietario.

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

[**\_AFSDBType MicrosoftDNS**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**Metodo Modify della \_ classe AFSDBType di MicrosoftDNS**](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





