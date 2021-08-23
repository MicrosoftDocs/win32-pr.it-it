---
title: Metodo GetObjectByTextRepresentation della MicrosoftDNS_ResourceRecord classe
description: Il metodo GetObjectByTextRepresentation recupera un'istanza esistente della classe \_ ResourceRecord MicrosoftDNS.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- DNS del metodo GetObjectByTextRepresentation
- Metodo GetObjectByTextRepresentation DNS, MicrosoftDNS_ResourceRecord classe
- MicrosoftDNS_ResourceRecord classe DNS, metodo GetObjectByTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e3b824ccabe86e842d4ef6f61799b33110b5d28a58658a6d4cbedc824c134b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692421"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Metodo GetObjectByTextRepresentation della classe ResourceRecord MicrosoftDNS \_

Il **metodo GetObjectByTextRepresentation** recupera un'istanza esistente della [**classe \_ ResourceRecord MicrosoftDNS.**](microsoftdns-resourcerecord.md)

## <a name="syntax"></a>Sintassi


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DnsServerName* \[ Pollici\]
</dt> <dd>

Nome del server DNS da cui recuperare RR.

</dd> <dt>

*ContainerName* \[ Pollici\]
</dt> <dd>

Nome del contenitore da cui deve essere ottenuto RR.

</dd> <dt>

*Rappresentazione di testo* \[ Pollici\]
</dt> <dd>

Rappresentazione testuale dell'RR da recuperare.

</dd> <dt>

*RR* \[ Cambio\]
</dt> <dd>

Riferimento al RR di cui è stata creata un'istanza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Metodo CreateInstanceFromTextRepresentation della classe \_ ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





