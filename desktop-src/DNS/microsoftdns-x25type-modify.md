---
title: Metodo Modify della classe MicrosoftDNS_X25Type
description: Il metodo modify aggiorna un record di risorse X. 25 (x25).
ms.assetid: 2d82d67e-ae29-4ded-86fe-7db0ef5ed74f
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_X25Type classe
- Classe MicrosoftDNS_X25Type DNS, metodo modify
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
ms.openlocfilehash: 10db2fa770d3da8487a712e631c41fdd4256bf7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120258"
---
# <a name="modify-method-of-the-microsoftdns_x25type-class"></a>Metodo Modify della \_ classe X25Type di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse X. 25 (x25).

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

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*PSDNAddress* \[ in, facoltativo\]
</dt> <dd>

Indirizzo PSDN del proprietario dell'RR.

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

[**\_X25Type MicrosoftDNS**](microsoftdns-x25type.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ X25Type**](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





