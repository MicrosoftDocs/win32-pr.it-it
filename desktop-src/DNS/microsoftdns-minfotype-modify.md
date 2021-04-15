---
title: Metodo Modify della classe MicrosoftDNS_MINFOType
description: Il metodo modify aggiorna un record di risorse MINFO (mail Information).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_MINFOType classe
- Classe MicrosoftDNS_MINFOType DNS, metodo modify
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
ms.openlocfilehash: 2b59d7d1231ed88e61a0ecf94cef50041ca772f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475881"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a>Metodo Modify della \_ classe MINFOType di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse MINFO (mail Information).

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

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*ResponsibleMailbox* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica una cassetta postale responsabile della lista di distribuzione o della cassetta postale specificata nel nome del proprietario del record.

</dd> <dt>

*ErrorMailbox* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica una cassetta postale per ricevere i messaggi di errore correlati alla lista di distribuzione o alla cassetta postale specificata dal nome del proprietario del record MINFO.

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

[**\_MINFOType MicrosoftDNS**](microsoftdns-minfotype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





