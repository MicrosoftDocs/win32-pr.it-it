---
title: Metodo Modify della classe MicrosoftDNS_RTType
description: Il metodo Modify aggiorna un record di risorse Route Through (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_RTType classe
- MicrosoftDNS_RTType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2003f8e2840a2684f91a7a01b0341e2e8dcdf0ca88b6bf31fcf58b3a3c6f79bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692401"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a>Metodo Modify della classe MICROSOFTDNS \_ RTType

Il **metodo Modify** aggiorna un record di risorse Route Through (RT).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
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

*IntermediateHost* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica un host da utilizzare come intermedio per raggiungere l'host specificato dal proprietario.

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

[**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe \_ MICROSOFTDNS RTType**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





