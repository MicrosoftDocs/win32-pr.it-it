---
title: Metodo Modify della classe MicrosoftDNS_AFSDBType
description: Il metodo Modify aggiorna un record di risorse del server di database del file system andrew (AFSDB).
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_AFSDBType classe
- MicrosoftDNS_AFSDBType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385b80d853c3b610971803c0b1d80a81b7b7c2335186fe4585e63f60c3e3cca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104061"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a>Metodo Modify della classe \_ MicrosoftDNS AFSDBType

Il **metodo Modify** aggiorna un record di risorse del server di database del file system andrew (AFSDB).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*Sottotipo* \[ in, facoltativo\]
</dt> <dd>

Sottotipo del server AFS host. Per il sottotipo 1 (valore=1), l'host dispone di un server di posizione del volume AFS versione 3.0 per la cella AFS denominata. Nel caso del sottotipo 2 (value=2), l'host ha un server dei nomi autenticato che contiene il nodo della directory radice della cella per la cella DCE/NCA denominata.

</dd> <dt>

*NomeServer* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica un host con un server per la cella AFS specificata nel nome del proprietario.

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

[**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe \_ MicrosoftDNS AFSDBType**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





