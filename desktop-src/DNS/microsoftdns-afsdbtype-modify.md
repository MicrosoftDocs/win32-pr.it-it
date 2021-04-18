---
title: Metodo Modify della classe MicrosoftDNS_AFSDBType
description: Il metodo modify aggiorna un record di risorse del server di database del file System Andrew (AFSDB).
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_AFSDBType classe
- Classe MicrosoftDNS_AFSDBType DNS, metodo modify
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
ms.openlocfilehash: 4752910ab9e8117bfdaf27f93d32be3377158ba5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301645"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a>Metodo Modify della \_ classe AFSDBType di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse del server di database del file System Andrew (AFSDB).

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

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*Sottotipo* \[ in, facoltativo\]
</dt> <dd>

Sottotipo del server AFS host. Per il sottotipo 1 (valore = 1), l'host dispone di un server del percorso del volume AFS versione 3,0 per la cella AFS denominata. Nel caso del sottotipo 2 (valore = 2), l'host dispone di un server dei nomi autenticato che contiene il nodo della directory radice della cella per la cella DCE/autorità di certificazione denominata.

</dd> <dt>

*Nomeserver* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica un host con un server per la cella AFS specificata nel nome del proprietario.

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

[**\_AFSDBType MicrosoftDNS**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





