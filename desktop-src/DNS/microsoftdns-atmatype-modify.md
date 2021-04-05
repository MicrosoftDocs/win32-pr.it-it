---
title: Metodo Modify della classe MicrosoftDNS_ATMAType
description: Il metodo modify aggiorna un indirizzo ATM al record di risorse Name (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_ATMAType classe
- Classe MicrosoftDNS_ATMAType DNS, metodo modify
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
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048376"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a>Metodo Modify della \_ classe ATMAType di MicrosoftDNS

Il metodo **Modify** aggiorna un indirizzo ATM al record di risorse Name (ATMA).

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

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*Formato* \[ in, facoltativo\]
</dt> <dd>

Formato dell'indirizzo ATM. Due valori possibili per FORMAT sono: 0 che indica il formato AESA (ATM End System Address) e 1 indica il formato E. 164.

</dd> <dt>

*ATMAddress* \[ in, facoltativo\]
</dt> <dd>

Stringa di lunghezza variabile di ottetti che contiene l'indirizzo ATM del nodo/proprietario a cui si riferisce questo RR. I primi quattro byte della matrice vengono usati per archiviare le dimensioni della stringa di ottetto. Il byte più significativo viene archiviato nel byte 0.

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

[**\_ATMAType MicrosoftDNS**](microsoftdns-atmatype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





