---
title: Metodo Modify della classe MicrosoftDNS_WINSRType
description: Il metodo Modify aggiorna un record di risorse WINS Reverse Look up (WINSR).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_WINSRType classe
- MicrosoftDNS_WINSRType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db7865110b0e79642dc91671094c06dfbd10e07cd89684dab58623a9456cca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076665"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a>Metodo Modify della classe MICROSOFTDNS \_ WINSRType

Il **metodo Modify** aggiorna un record di risorse WINS Reverse Look up (WINSR).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*MappingFlag* \[ in, facoltativo\]
</dt> <dd>

Flag di mapping WINSR che specifica se il record deve essere incluso nella replica di zona. Può avere solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale).

</dd> <dt>

*LookupTimeout* \[ in, facoltativo\]
</dt> <dd>

Timeout, in secondi, per un server DNS che usa la ricerca inversa WINS.

</dd> <dt>

*CacheTimeout* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, un server DNS che usa WINS Look up può memorizzare nella cache la risposta del server WINS.

</dd> <dt>

*ResultDomain* \[ in, facoltativo\]
</dt> <dd>

Nome di dominio da aggiungere ai nomi NetBIOS restituiti.

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

[**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe \_ MICROSOFTDNS WINSRType**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





