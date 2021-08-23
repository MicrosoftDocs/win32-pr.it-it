---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_SIGType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse Signature (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- Metodo CreateInstanceFromPropertyData DNS, MicrosoftDNS_SIGType classe
- MicrosoftDNS_SIGType classe DNS, metodo CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90501af2f6e492e56d17f88fb6bc74cc72522503760688457832a2374918100e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076725"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a>Metodo CreateInstanceFromPropertyData della classe SIGType MicrosoftDNS \_

Il **metodo CreateInstanceFromPropertyData** crea un'istanza di un record di risorse Signature (SIG).

## <a name="syntax"></a>Sintassi


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
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

*TypeCovered* \[ Pollici\]
</dt> <dd>

Tipo di RR coperto da questo SIG.

</dd> <dt>

*Algoritmo* \[ Pollici\]
</dt> <dd>

Algoritmo usato con la chiave specificata nel record di risorse. I valori assegnati sono indicati nella tabella seguente.



| Valore                                                                                                | Significato                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Crittografia a curva ellittica<br/> |



 

</dd> <dt>

*Etichette* \[ Pollici\]
</dt> <dd>

Conteggio senza segno delle etichette nel nome del proprietario RR SIG originale. Il conteggio non include l'etichetta NULL per la radice, né i caratteri jolly iniziali.

</dd> <dt>

*OriginalTTL* \[ Pollici\]
</dt> <dd>

TTL del set di RR firmato dal SIG.

</dd> <dt>

*SignatureExpiration* \[ Pollici\]
</dt> <dd>

Data di scadenza della firma, espressa in secondi dall'inizio del 1° gennaio 1970, ora media di Greenwich (GMT), esclusi i secondi intercalare.

</dd> <dt>

*SignatureInception* \[ Pollici\]
</dt> <dd>

Data e ora in cui la firma diventa valida, espressa in secondi dall'inizio del 1° gennaio 1970, ora media di Greenwich (GMT), esclusi i secondi intercalare.

</dd> <dt>

*KeyTag* \[ Pollici\]
</dt> <dd>

Metodo usato per scegliere una chiave che verifica un SIG. Vedere RFC 2535, Appendice C per il metodo usato per calcolare un KeyTag.

</dd> <dt>

*SignerName* \[ Pollici\]
</dt> <dd>

Nome di dominio del firmatario che ha generato l'errore SIG RR.

</dd> <dt>

*Firma* \[ Pollici\]
</dt> <dd>

Firma, rappresentata in base 64, formattata come definito in RFC 2535, Appendice A.

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

[**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)
</dt> <dt>

[**Metodo Modify della classe SIGType MicrosoftDNS \_**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





