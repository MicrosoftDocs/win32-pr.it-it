---
title: Metodo Modify della classe MicrosoftDNS_X25Type
description: Il metodo Modify aggiorna un record di risorse X.25 (X25).
ms.assetid: 2d82d67e-ae29-4ded-86fe-7db0ef5ed74f
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_X25Type classe
- MicrosoftDNS_X25Type classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94120c5ccf0f86cf2687941f3442b3e7f16db3c140af5c6234fe475445a3dd06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573611"
---
# <a name="modify-method-of-the-microsoftdns_x25type-class"></a>Metodo Modify della classe MicrosoftDNS \_ X25Type

Il **metodo Modify** aggiorna un record di risorse X.25 (X25).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*PSDNAddress* \[ in, facoltativo\]
</dt> <dd>

Indirizzo PSDN del proprietario del RR.

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

[**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ X25Type**](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





