---
title: Metodo Modify della classe MicrosoftDNS_MXType
description: Il metodo modify aggiorna un record di risorse di Mail Exchanger (Sig.).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_MXType classe
- Classe MicrosoftDNS_MXType DNS, metodo modify
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
ms.openlocfilehash: 8a665d0673e048eff684b4c985b54a1c57e030a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964895"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a>Metodo Modify della \_ classe MXType di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse di Mail Exchanger (Sig.).

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

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*Preferenza* \[ in, facoltativo\]
</dt> <dd>

Preferenza assegnata a questo RR tra gli altri nello stesso proprietario. Sono preferibili valori inferiori.

</dd> <dt>

*MailExchange* \[ in, facoltativo\]
</dt> <dd>

FQDN che specifica un host disposto a fungere da scambio di posta elettronica per il nome del proprietario.

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

[**\_MXType MicrosoftDNS**](microsoftdns-mxtype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MXType**](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





