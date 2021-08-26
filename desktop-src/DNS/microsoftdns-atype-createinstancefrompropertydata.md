---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_AType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse Address (A).
ms.assetid: 81d67eba-f2c6-49c0-af29-be3f3724a973
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- Metodo CreateInstanceFromPropertyData DNS, MicrosoftDNS_AType classe
- MicrosoftDNS_AType classe DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78a3841ed89a5e3cd0362675ba0c5d0e767471ba1beb7383f5a728e8bd825749
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984661"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atype-class"></a>Metodo CreateInstanceFromPropertyData della classe \_ MicrosoftDNS AType

Il **metodo CreateInstanceFromPropertyData** crea un'istanza di un record di risorse Address (A).

## <a name="syntax"></a>Sintassi


```mof
void CreateInstanceFromPropertyData(
  [in]           string             DnsServerName,
  [in]           string             ContainerName,
  [in]           string             OwnerName,
  [in, optional] uint32             RecordClass = 1,
  [in, optional] uint32             TTL,
  [in]           string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DnsServerName* \[ Pollici\]
</dt> <dd>

Nome di dominio completo (FQDN) o indirizzo IP del server DNS che contiene questo RR.

</dd> <dt>

*ContainerName* \[ Pollici\]
</dt> <dd>

Nome del contenitore per l'istanza di Zona, Cache o RootHints che contiene questo RR.

</dd> <dt>

*OwnerName* \[ Pollici\]
</dt> <dd>

FQDN del proprietario per RR.

> [!Note]  
> Non usare il nome NetBIOS proprietario.

 

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

*Indirizzo IP* \[ Pollici\]
</dt> <dd>

Stringa che rappresenta l'indirizzo IP dell'host.

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Metodo Modify della classe AType MicrosoftDNS \_**](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





