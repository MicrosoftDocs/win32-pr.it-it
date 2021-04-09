---
title: Metodo Modify della classe MicrosoftDNS_PTRType
description: Il metodo modify aggiorna un record di risorse puntatore (PTR).
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_PTRType classe
- Classe MicrosoftDNS_PTRType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 840bf100ea5cdbbb606837e90d8fa9fcebab57fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964375"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a>Metodo Modify della \_ classe PTRType di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse puntatore (PTR).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*PTRDomainName* \[ in, facoltativo\]
</dt> <dd>

Indirizzo del nome di dominio del record PTR.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Riferimento all'oggetto modificato.

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

[**\_PTRType MicrosoftDNS**](microsoftdns-ptrtype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





