---
title: Metodo Modify della classe MicrosoftDNS_RPType
description: Il metodo modify aggiorna un record di risorse responsabile (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_RPType classe
- Classe MicrosoftDNS_RPType DNS, metodo modify
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
ms.openlocfilehash: 10ec575424e6e26c79f8d6a27e62732cad6ddc57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873994"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a>Metodo Modify della \_ classe RPType di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse responsabile (RP).

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

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*RPMailbox* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica la cassetta postale per la persona responsabile.

</dd> <dt>

*TXTDomainName* \[ in, facoltativo\]
</dt> <dd>

FQDN per cui sono presenti record di risorse TXT.

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

[**\_RPType MicrosoftDNS**](microsoftdns-rptype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ RPType**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





