---
title: Metodo Modify della classe MicrosoftDNS_TXTType
description: Il metodo Modify aggiorna un record di risorse di testo (TXT).
ms.assetid: af61057e-95be-4290-83da-a63f01ead476
keywords:
- Modificare il DNS del metodo
- Modificare il DNS del metodo , MicrosoftDNS_TXTType classe
- MicrosoftDNS_TXTType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e565d4c48b048b4d72b11c939b644752cb14f1993c2810f127bb14f60bec929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957300"
---
# <a name="modify-method-of-the-microsoftdns_txttype-class"></a>Metodo Modify della classe TXTType MicrosoftDNS \_

Il **metodo Modify** aggiorna un record di risorse di testo (TXT).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*Testo descrittivo* \[ Pollici\]
</dt> <dd>

Testo descrittivo, la cui semantica dipende dal dominio del proprietario.

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

[**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe TxtType MicrosoftDNS \_**](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





