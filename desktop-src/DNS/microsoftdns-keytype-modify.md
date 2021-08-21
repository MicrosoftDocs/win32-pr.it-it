---
title: Metodo Modify della classe MicrosoftDNS_KEYType
description: Il metodo Modify aggiorna un record di risorse KEY.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Modificare il DNS del metodo
- Modificare il DNS del metodo , MicrosoftDNS_KEYType classe
- MicrosoftDNS_KEYType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5b657e940716a7afa2113dcbdc6836ab3680c1dfe37b88a454d9bdd0c7bc28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163257"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a>Metodo Modify della classe KEYType MicrosoftDNS \_

Il **metodo Modify** aggiorna un record di risorse KEY.

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*Flag* \[ in, facoltativo\]
</dt> <dd>

Flag usati per specificare il mapping, come descritto in IETF RFC 2535.

</dd> <dt>

*Protocollo* \[ in, facoltativo\]
</dt> <dd>

Protocollo per il quale è possibile usare la chiave specificata in RR. I valori assegnati sono illustrati nella tabella seguente.



| Valore                                                                                                    | Significato                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | Posta elettronica<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>     | Dnssec<br/>        |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | Tutti i protocolli<br/> |



 

</dd> <dt>

*Algoritmo* \[ in, facoltativo\]
</dt> <dd>

Algoritmo utilizzato con la chiave specificata nel record di risorse. I valori assegnati sono illustrati nella tabella seguente.



| Valore                                                                                                | Significato                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Crittografia a curva ellittica<br/> |



 

</dd> <dt>

*PublicKey* \[ in, facoltativo\]
</dt> <dd>

Chiave pubblica, rappresentata in base 64 come descritto nell'Appendice A di RFC 2535.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Riferimento al nuovo oggetto .

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

[**MicrosoftDNS \_ KEYType**](microsoftdns-keytype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe KEYType MicrosoftDNS \_**](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





