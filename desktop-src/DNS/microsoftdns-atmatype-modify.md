---
title: Metodo Modify della classe MicrosoftDNS_ATMAType
description: Il metodo Modify aggiorna un record di risorse atm address to name (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Modificare il DNS del metodo
- Modificare il DNS del metodo , MicrosoftDNS_ATMAType classe
- MicrosoftDNS_ATMAType classe DNS , metodo Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c8f98288c519340e6a95959964a4c42799201c7e1701bb748f634746a94226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163759"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a>Metodo Modify della classe ATMAType MicrosoftDNS \_

Il **metodo Modify** aggiorna un record di risorse atm address to name (ATMA).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, in cui RR può essere memorizzato nella cache da un resolver DNS.

</dd> <dt>

*Formato* \[ in, facoltativo\]
</dt> <dd>

Formato dell'indirizzo del bancomat. Due valori possibili per FORMAT sono: 0 che indica il formato AESA (ATM End System Address) e 1 che indica il formato E.164.

</dd> <dt>

*ATMAddress* \[ in, facoltativo\]
</dt> <dd>

Stringa di ottetti a lunghezza variabile contenente l'indirizzo del bancomat del nodo o del proprietario a cui si riferiscono questi RR. I primi quattro byte della matrice vengono usati per archiviare le dimensioni della stringa dell'ottetto. Il byte più significativo viene archiviato in byte 0.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Riferimento al nuovo oggetto .

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

[**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





