---
title: Metodo Modify della classe MicrosoftDNS_WINSRType
description: Il metodo modify aggiorna un record di risorse WINS reverse look up (WINSr).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_WINSRType classe
- Classe MicrosoftDNS_WINSRType DNS, metodo modify
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
ms.openlocfilehash: e02d89c3cd191262136035f9006853e2f1a7f7dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121274"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a>Metodo Modify della \_ classe WINSRType di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse WINS reverse look up (WINSR).

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

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*MappingFlag* \[ in, facoltativo\]
</dt> <dd>

Flag di mapping WINSr che specifica se il record deve essere incluso nella replica della zona. Potrebbero essere presenti solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale).

</dd> <dt>

*LookupTimeout* \[ in, facoltativo\]
</dt> <dd>

Timeout, in secondi, per un server DNS che utilizza la ricerca inversa WINS.

</dd> <dt>

*CacheTimeout* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.

</dd> <dt>

*ResultDomain* \[ in, facoltativo\]
</dt> <dd>

Nome di dominio da aggiungere ai nomi NetBIOS restituiti.

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

[**\_WINSRType MicrosoftDNS**](microsoftdns-winsrtype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





