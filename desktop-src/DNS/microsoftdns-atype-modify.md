---
title: Metodo Modify della classe MicrosoftDNS_AType
description: Il metodo Modify aggiorna la durata (TTL) e l'indirizzo IP di un record di risorse indirizzo host (A).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_AType classe
- MicrosoftDNS_AType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d9f4740aeec92726796943e53b4d2143a6378341b061aaa7d3f3f6bf6dc7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163482"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a>Metodo Modify della classe \_ MicrosoftDNS AType

Il **metodo Modify** aggiorna la durata (TTL) e l'indirizzo IP di un record di risorse indirizzo host (A).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*Indirizzo IP* \[ in, facoltativo\]
</dt> <dd>

Stringa che rappresenta l'indirizzo IP dell'host.

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe AType MicrosoftDNS \_**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





