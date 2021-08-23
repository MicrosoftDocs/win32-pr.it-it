---
title: Metodo Modify della classe MicrosoftDNS_MINFOType
description: Il metodo Modify aggiorna un record di risorse MINFO (Mail Information).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_MINFOType classe
- MicrosoftDNS_MINFOType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954015ffdb01a8655a7762d3c364abe3440a8cfd19ec7eabf5ad8db5cf11c8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692561"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a>Metodo Modify della classe MicrosoftDNS \_ MINFOType

Il **metodo Modify** aggiorna un record di risorse MINFO (Mail Information).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*ResponsibleMailbox* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica una cassetta postale responsabile della mailing list o della cassetta postale specificata nel nome proprietario del record.

</dd> <dt>

*ErrorMailbox* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica una cassetta postale per ricevere messaggi di errore relativi alla lista di distribuzione o alla cassetta postale specificata dal nome del proprietario del record MINFO.

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

[**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe \_ MicrosoftDNS MINFOType**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





