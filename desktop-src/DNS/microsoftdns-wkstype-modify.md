---
title: Metodo Modify della classe MicrosoftDNS_WKSType
description: Il metodo Modify aggiorna un record di risorse Well-Known Services (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_WKSType classe
- MicrosoftDNS_WKSType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f58a71b7d3a3237a744d42c90bc437714ed50553639253bafb0b2b9fb2977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692239"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a>Metodo Modify della classe WKSType di MicrosoftDNS \_

Il **metodo Modify** aggiorna un record di risorse Well-Known Services (WKS).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*InternetAddress* \[ in, facoltativo\]
</dt> <dd>

Indirizzo IP Internet per il proprietario del record.

</dd> <dt>

*IPProtocol* \[ in, facoltativo\]
</dt> <dd>

Stringa che rappresenta il protocollo IP per questo record. I valori validi sono UDP o TCP.

</dd> <dt>

*Servizi* \[ in, facoltativo\]
</dt> <dd>

Stringa contenente tutti i servizi usati dal record servizio noto (WKS).

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

[**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe \_ WKSType MicrosoftDNS**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





