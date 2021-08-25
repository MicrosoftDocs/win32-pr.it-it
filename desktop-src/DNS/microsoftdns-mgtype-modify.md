---
title: Metodo Modify della classe MicrosoftDNS_MGType
description: Il metodo Modify aggiorna un record di risorse del gruppo di posta (MG).
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_MGType classe
- MicrosoftDNS_MGType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db26f33e56ecc8553af1e34513a085b6eb6666ca99e2f91ec19383756094d6f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874911"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a>Metodo Modify della classe MICROSOFTDNS \_ MGType

Il **metodo Modify** aggiorna un record di risorse del gruppo di posta (MG).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*MGMailbox* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica una cassetta postale membro del gruppo di posta specificato dal nome del proprietario del record.

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

[**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MICROSOFTDNS \_ MGType**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





