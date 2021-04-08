---
title: Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS_SIGType
description: Il metodo CreateInstanceFromPropertyData crea un'istanza di un record di risorse di firma (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- DNS del metodo CreateInstanceFromPropertyData
- DNS del metodo CreateInstanceFromPropertyData, classe MicrosoftDNS_SIGType
- Classe MicrosoftDNS_SIGType DNS, metodo CreateInstanceFromPropertyData
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
ms.openlocfilehash: c21660572d9557e6425b459c5694a7eeee4722cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047985"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a>Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SIGType

Il metodo **CreateInstanceFromPropertyData** crea un'istanza di un record di risorse di firma (SIG).

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

*TypeCovered* \[ in\]
</dt> <dd>

Tipo di RR coperto da questo SIG.

</dd> <dt>

*Algoritmo* \[ di in\]
</dt> <dd>

Algoritmo utilizzato con la chiave specificata nel record di risorse. I valori assegnati sono riportati nella tabella seguente.



| Valore                                                                                                | Significato                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Crittografia a curva ellittica<br/> |



 

</dd> <dt>

*Etichette* \[ in\]
</dt> <dd>

Conteggio senza segno delle etichette nel nome originale del proprietario del record di firma. Il conteggio non include l'etichetta NULL per la radice, né i caratteri jolly iniziali.

</dd> <dt>

*OriginalTTL* \[ in\]
</dt> <dd>

TTL del set di RR firmato dal SIG.

</dd> <dt>

*SignatureExpiration* \[ in\]
</dt> <dd>

Data di scadenza della firma, espressa in secondi dall'inizio del 1 gennaio 1970, ora di Greenwich (GMT), esclusi i secondi intercalari.

</dd> <dt>

*SignatureInception* \[ in\]
</dt> <dd>

Data e ora in cui la firma diventa valida, espressa in secondi a partire dall'inizio del 1 ° gennaio 1970, ora di Greenwich (GMT), esclusi i secondi intercalari.

</dd> <dt>

*KeyTag* \[ in\]
</dt> <dd>

Metodo usato per scegliere una chiave che verifica un SIG. Vedere RFC 2535, Appendice C per il metodo usato per calcolare un KeyTag.

</dd> <dt>

*SignerName* \[ in\]
</dt> <dd>

Nome di dominio del firmatario che ha generato il record SIG.

</dd> <dt>

*Firma* \[ di in\]
</dt> <dd>

Firma, rappresentata in base 64, formattata come definito nella RFC 2535, Appendice A.

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

[**\_SIGType MicrosoftDNS**](microsoftdns-sigtype.md)
</dt> <dt>

[**Metodo Modify della \_ classe SIGType di MicrosoftDNS**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





