---
title: Metodo Modify della classe MicrosoftDNS_NXTType
description: Il metodo Modify aggiorna un record di risorse Next (NXT).
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- Modificare il DNS del metodo
- Modificare il metodo DNS , MicrosoftDNS_NXTType classe
- MicrosoftDNS_NXTType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e43082ff829a7b8701701e9b099aa0f36d274879bfb6f281272096558f1c8bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163202"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a>Metodo Modify della classe \_ NXTType MicrosoftDNS

Il **metodo Modify** aggiorna un record di risorse Next (NXT).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui il RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*NextDomainName* \[ Pollici\]
</dt> <dd>

Nome di dominio successivo.

</dd> <dt>

*Tipi* \[ Pollici\]
</dt> <dd>

Elenco delimitato da spazi dei nomi mnemoici di tipo RR per il nome del proprietario del record di risorse NXT.

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

[**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe \_ NXTType MicrosoftDNS**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





