---
title: Metodo Modify della classe MicrosoftDNS_SOAType
description: Il metodo Modify aggiorna un record di risorse SOA (Start Of Authority).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_SOAType classe
- MicrosoftDNS_SOAType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74785804ebed8266443f0dd708a5d122e350a6cf88b91f228d2ce266481dffaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825081"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a>Metodo Modify della classe \_ SOAType MicrosoftDNS

Il **metodo Modify** aggiorna un record di risorse SOA (Start Of Authority).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*SerialNumber* \[ in, facoltativo\]
</dt> <dd>

Numero di serie SOA che rappresenta il numero di [](s-gly.md) volte in cui la zona è stata aggiornata, usata dai server secondari per determinare se è necessario il trasferimento della zona.

</dd> <dt>

*PrimaryServer* \[ in, facoltativo\]
</dt> <dd>

Nome del server primario.

</dd> <dt>

*ResponsibleParty* \[ in, facoltativo\]
</dt> <dd>

Indirizzo della cassetta postale della parte responsabile, sotto forma di alias.domain, ad esempio xyz.microsoft.com. Si noti l'uso di un punto anziché di un simbolo at (@).

</dd> <dt>

*RefreshInterval* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, prima dell'aggiornamento della zona contenente questo record.

</dd> <dt>

*RetryDelay* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il server DNS deve ritardare tra i tentativi di risoluzione dei nomi.

</dd> <dt>

*ExpireLimit* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui i server secondari devono attendere una risposta dal server primario prima di eliminare le copie del file di zona come non valide.

</dd> <dt>

*MinimumTTL* \[ in, facoltativo\]
</dt> <dd>

Tempo TTL, in secondi, applicato ai record di risorse nella zona che non specificano il proprio TTL.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Riferimento all'oggetto modificato

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

[**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





