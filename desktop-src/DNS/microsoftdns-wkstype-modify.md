---
title: Metodo Modify della classe MicrosoftDNS_WKSType
description: Il metodo modify aggiorna un record di risorse di Well-Known Services (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Modificare il metodo DNS
- Modificare il metodo DNS, MicrosoftDNS_WKSType classe
- Classe MicrosoftDNS_WKSType DNS, metodo modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874089"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a>Metodo Modify della \_ classe WKSType di MicrosoftDNS

Il metodo **Modify** aggiorna un record di risorse di Well-Known Services (WKS).

## <a name="syntax"></a>Sintassi


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

Valore *TTL* \[ in, facoltativo\]
</dt> <dd>

Tempo, in secondi, che l'RR può memorizzare nella cache da un resolver DNS.

</dd> <dt>

*InternetAddress* \[ in, facoltativo\]
</dt> <dd>

Indirizzo IP Internet per il proprietario del record.

</dd> <dt>

*IPProtocol* \[ in, facoltativo\]
</dt> <dd>

Stringa che rappresenta il protocollo IP per questo record. I valori validi sono UDP o TCP.

</dd> <dt>

*Servizi* \[ di in, facoltativo\]
</dt> <dd>

Stringa contenente tutti i servizi utilizzati dal record del servizio noto (WKS).

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

[**\_WKSType MicrosoftDNS**](microsoftdns-wkstype.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WKSType**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





