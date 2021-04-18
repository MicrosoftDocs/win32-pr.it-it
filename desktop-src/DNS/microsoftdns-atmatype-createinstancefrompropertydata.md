---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_ATMAType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un indirizzo ATM per il nome (ATMA) del record di risorse.
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_ATMAType
- Classe MicrosoftDNS_ATMAType DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fada3759e6384ae6f42a78bd132b9b8ad16f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301643"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a>Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ ATMAType

Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un indirizzo ATM per il nome (ATMA) del record di risorse.

## <a name="syntax"></a>Sintassi


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
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

*Formato* \[ in\]
</dt> <dd>

Formato dell'indirizzo ATM. Due valori possibili per FORMAT sono: 0 che indica il formato AESA (ATM End System Address) e 1 indica il formato E. 164.

</dd> <dt>

*ATMAddress* \[ in\]
</dt> <dd>

Stringa di lunghezza variabile di ottetti che contiene l'indirizzo ATM del nodo/proprietario a cui si riferisce questo RR. I primi quattro byte della matrice vengono usati per archiviare le dimensioni della stringa di ottetto. Il byte più significativo viene archiviato nel byte 0.

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

[**\_ATMAType MicrosoftDNS**](microsoftdns-atmatype.md)
</dt> <dt>

[**Metodo Modify della \_ classe ATMAType di MicrosoftDNS**](microsoftdns-atmatype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





