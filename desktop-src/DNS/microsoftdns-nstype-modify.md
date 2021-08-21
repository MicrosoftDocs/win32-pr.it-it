---
title: Metodo Modify della classe MicrosoftDNS_NSType
description: Il metodo Modify aggiorna un record di risorse del server dei nomi(NS).
ms.assetid: da625231-cf4e-4526-b713-737e6b9f5831
keywords:
- Modificare il DNS del metodo
- Modificare il DNS del metodo , MicrosoftDNS_NSType classe
- MicrosoftDNS_NSType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8adcebb06aa7d796b9d4c79282fe04ec9047d54a0be1c69a302fdcddf78ca34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573781"
---
# <a name="modify-method-of-the-microsoftdns_nstype-class"></a>Metodo Modify della classe NSType MicrosoftDNS \_

Il **metodo Modify** aggiorna un record di risorse del server dei nomi(NS).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              NSHost,
  [out, ref]     MicrosoftDNS_NSType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*NSHost* \[ in, facoltativo\]
</dt> <dd>

Host autorevole per il dominio.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Riferimento all'oggetto modificato.

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

[**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe PTRType MicrosoftDNS \_**](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





