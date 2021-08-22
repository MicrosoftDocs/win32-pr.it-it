---
title: Metodo Modify della classe MicrosoftDNS_RPType
description: Il metodo Modify aggiorna un record di risorse della persona responsabile .RP.
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Modificare il DNS del metodo
- Modificare il DNS del metodo , MicrosoftDNS_RPType classe
- MicrosoftDNS_RPType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d237879b883e21c3c6289542e4eae7b9703be64931af788f042b6cdbec2ca49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587491"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a>Metodo Modify della classe \_ MicrosoftDNS RPType

Il **metodo Modify** aggiorna un record di risorse della persona responsabile .RP.

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*RP(RP)* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica la cassetta postale per la persona responsabile.

</dd> <dt>

*TXTDomainName* \[ in, facoltativo\]
</dt> <dd>

FQDN per cui esistono record di risorse TXT.

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

[**MicrosoftDNS \_ RPType**](microsoftdns-rptype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe \_ RPType MicrosoftDNS**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





