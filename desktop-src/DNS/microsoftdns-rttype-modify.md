---
title: Metodo Modify della classe MicrosoftDNS_RTType
description: Il metodo modify aggiorna una route tramite un record di risorse (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_RTType classe
- Classe MicrosoftDNS_RTType DNS, metodo modify
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
ms.openlocfilehash: 8267bf1dc256ec95a456978643226ab5c01af93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517938"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a>Metodo Modify della \_ classe RTType di MicrosoftDNS

Il metodo **Modify** aggiorna una route tramite un record di risorse (RT).

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

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*Preferenza* \[ in, facoltativo\]
</dt> <dd>

Preferenza assegnata a questo RR tra gli altri nello stesso proprietario. Sono preferibili valori inferiori.

</dd> <dt>

*IntermediateHost* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica un host che funge da intermediario per raggiungere l'host specificato dal proprietario.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Riferimento al nuovo oggetto.

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

[**\_RTType MicrosoftDNS**](microsoftdns-rttype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ RTType**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





