---
title: Metodo Modify della classe MicrosoftDNS_MBType
description: Il metodo Modify aggiorna un record di risorse cassetta postale (MB).
ms.assetid: ee76031c-ac1b-4ebb-9fb2-3b64553867cc
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_MBType classe
- MicrosoftDNS_MBType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b0e4183a2b736d0ed896fee4bf2cc57e35f0e6b628a9aee4345f4c33b33ed6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918341"
---
# <a name="modify-method-of-the-microsoftdns_mbtype-class"></a>Metodo Modify della classe \_ MBType MicrosoftDNS

Il **metodo Modify** aggiorna un record di risorse cassetta postale (MB).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MBHost,
  [out, ref]     MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*MBHost* \[ Pollici\]
</dt> <dd>

Stringa che rappresenta il nome host della cassetta postale per il record MB.

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

[**MicrosoftDNS \_ MBType**](microsoftdns-mbtype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe \_ MBType MicrosoftDNS**](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





