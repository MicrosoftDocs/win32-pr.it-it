---
title: Metodo Modify della classe MicrosoftDNS_WINSType
description: Il metodo modify aggiorna un record di risorse WINS (Windows Internet Name Service).
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_WINSType classe
- Classe MicrosoftDNS_WINSType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874094"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a>Metodo Modify della \_ classe WINSType di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse WINS (Windows Internet Name Service).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*MappingFlag* \[ in, facoltativo\]
</dt> <dd>

Flag di mapping WINS che specifica se il record deve essere incluso nella replica della zona. Potrebbero essere presenti solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale). I valori seguenti sono validi.



| Valore                                                                                                                                               | Significato                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Flag di replica<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Flag senza replica (record locale)<br/> |



 

</dd> <dt>

*LookupTimeout* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, durante il quale un server DNS tenta la risoluzione usando la ricerca di WINS.

</dd> <dt>

*CacheTimeout* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, per cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.

</dd> <dt>

*WinsServers* \[ in, facoltativo\]
</dt> <dd>

Elenco di indirizzi IP delimitati da virgole dei server WINS utilizzati nelle ricerche WINS.

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

[**\_WINSType MicrosoftDNS**](microsoftdns-winstype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WINSType**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





