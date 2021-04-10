---
title: Metodo Modify della classe MicrosoftDNS_SRVType
description: Il metodo modify aggiorna un record di risorse del servizio (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_SRVType classe
- Classe MicrosoftDNS_SRVType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048695"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a>Metodo Modify della \_ classe SRVType di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse del servizio (SRV).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*Priorità* \[ di in, facoltativo\]
</dt> <dd>

Priorità dell'host di destinazione specificato nel nome del proprietario. I numeri più bassi implicano priorità più elevate.

</dd> <dt>

*Peso* \[ in, facoltativo\]
</dt> <dd>

Peso dell'host di destinazione. Questa operazione è utile quando si seleziona tra gli host con la stessa priorità. La possibilità di utilizzare questo host deve essere proporzionale al suo peso.

</dd> <dt>

*Porta* \[ in, facoltativo\]
</dt> <dd>

Porta utilizzata nell'host di destinazione di un servizio del protocollo.

</dd> <dt>

*SRVDomainName* \[ in, facoltativo\]
</dt> <dd>

FQDN dell'host di destinazione. Destinazione di \\ . \\ indica che il servizio non è disponibile in questo dominio.

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

[**\_SRVType MicrosoftDNS**](microsoftdns-srvtype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SRVType**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





