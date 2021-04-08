---
title: Metodo Modify della classe MicrosoftDNS_SOAType
description: Il metodo modify aggiorna un record di risorse di inizio di autorità (SOA).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_SOAType classe
- Classe MicrosoftDNS_SOAType DNS, metodo modify
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
ms.openlocfilehash: 1ff40abc7f4e93b7122a1c48889c17f9efc4f625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047983"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a>Metodo Modify della \_ classe SOAType di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse di inizio di autorità (SOA).

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

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*SerialNumber* \[ in, facoltativo\]
</dt> <dd>

Numero di serie SOA che rappresenta il numero di volte in cui la zona è stata aggiornata, usata dai [*server secondari*](s-gly.md) per determinare se è necessario il trasferimento di zona.

</dd> <dt>

*PrimaryServer* \[ in, facoltativo\]
</dt> <dd>

Nome del server primario.

</dd> <dt>

*Qualcunoresponsabile* \[ in, facoltativo\]
</dt> <dd>

Indirizzo della cassetta postale della parte responsabile, nel formato alias. dominio, ad esempio xyz.microsoft.com. Si noti l'uso di un punto anziché un simbolo di chiocciola (@).

</dd> <dt>

*RefreshInterval* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, prima che sia necessario aggiornare la zona contenente questo record.

</dd> <dt>

*RetryDelay* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, per cui il server DNS deve ritardare tra i tentativi di risoluzione dei nomi.

</dd> <dt>

*ExpireLimit* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, durante il quale i server secondari devono attendere una risposta dal server primario prima di rimuovere le copie del file di zona come non valide.

</dd> <dt>

*MinimumTTL* \[ in, facoltativo\]
</dt> <dd>

Tempo TTL, in secondi, applicato ai record di risorse nella zona che non specificano un valore TTL specifico.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Riferimento all'oggetto modificato

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

[**\_SOAType MicrosoftDNS**](microsoftdns-soatype.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





