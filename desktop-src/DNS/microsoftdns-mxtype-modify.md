---
title: Metodo Modify della classe MicrosoftDNS_MXType
description: Il metodo Modify aggiorna un record di risorse di Mail Exchanger (MR).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_MXType classe
- MicrosoftDNS_MXType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fb31da6bf0861c94c54163fa9c771ac592fca105a5459214e17031c3b8e6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076785"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a>Metodo Modify della classe \_ MXType MicrosoftDNS

Il **metodo Modify** aggiorna un record di risorse di Mail Exchanger (MR).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*Preferenza* \[ in, facoltativo\]
</dt> <dd>

Preferenza data a questo RR tra gli altri allo stesso proprietario. Sono preferibili valori inferiori.

</dd> <dt>

*MailExchange* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica un host che vuole fungere da scambio di posta elettronica per il nome del proprietario.

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

[**MicrosoftDNS \_ MXType**](microsoftdns-mxtype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe \_ MXType MicrosoftDNS**](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





