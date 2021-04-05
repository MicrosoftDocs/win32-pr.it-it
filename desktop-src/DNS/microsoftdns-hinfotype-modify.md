---
title: Metodo Modify della classe MicrosoftDNS_HINFOType
description: Il metodo modify aggiorna un record di risorse host Information (HINFO).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_HINFOType classe
- Classe MicrosoftDNS_HINFOType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29a01eb94d82d080142d3496bab5f7f0b9acac8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741546"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a>Metodo Modify della \_ classe HINFOType di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse host Information (HINFO).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*CPU* \[ in, facoltativo\]
</dt> <dd>

Tipo di CPU del proprietario del record.

</dd> <dt>

*Sistema operativo* \[ in, facoltativo\]
</dt> <dd>

Sistema operativo del proprietario del record.

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

[**\_HINFOType MicrosoftDNS**](microsoftdns-hinfotype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





