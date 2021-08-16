---
title: Metodo Modify della classe MicrosoftDNS_SIGType
description: Il metodo Modify aggiorna una firma (SIG) RR.
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_SIGType classe
- MicrosoftDNS_SIGType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be64eb494eb72ace437aeade8d7d01a6675f99b2b44c4fa461a8e60c8ed3de1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692281"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a>Metodo Modify della classe SIGType MicrosoftDNS \_

Il **metodo Modify** aggiorna una firma (SIG) RR.

## <a name="syntax"></a>Sintassi


```mof
void Modify(
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

## <a name="remarks"></a>Commenti

Qualsiasi parametro non specificato viene lasciato invariato nel record modificato.

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

[**Metodo CreateInstanceFromPropertyData della classe SIGType MicrosoftDNS \_**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





