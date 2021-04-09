---
title: Metodo Modify della classe MicrosoftDNS_KEYType
description: Il metodo modify aggiorna un record di risorse chiave.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_KEYType classe
- Classe MicrosoftDNS_KEYType DNS, metodo modify
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
ms.openlocfilehash: 44ee9182925f3f1d53fb90a4beefeb421f01c24f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121402"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a>Metodo Modify della classe di \_ tipo MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse chiave.

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

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*Flag* \[ in, facoltativo\]
</dt> <dd>

Flag utilizzati per specificare il mapping, come descritto in IETF RFC 2535.

</dd> <dt>

*Protocollo* \[ di in, facoltativo\]
</dt> <dd>

Protocollo per il quale è possibile utilizzare la chiave specificata nell'RR. I valori assegnati sono riportati nella tabella seguente.



| Valore                                                                                                    | Significato                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | Posta elettronica<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>     | DNSSEC<br/>        |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | Tutti i protocolli<br/> |



 

</dd> <dt>

*Algoritmo* \[ di in, facoltativo\]
</dt> <dd>

Algoritmo utilizzato con la chiave specificata nel record di risorse. I valori assegnati sono riportati nella tabella seguente.



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

*RR* \[ out, Ref\]
</dt> <dd>

Riferimento al nuovo oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Tutti i parametri non specificati rimangono invariati nel record modificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipo di MicrosoftDNS \_**](microsoftdns-keytype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe di \_ tipo MicrosoftDNS**](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





