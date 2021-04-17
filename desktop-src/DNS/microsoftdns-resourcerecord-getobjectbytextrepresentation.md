---
title: Metodo GetObjectByTextRepresentation della classe MicrosoftDNS_ResourceRecord
description: Il metodo GetObjectByTextRepresentation recupera un'istanza esistente della \_ classe ResourceRecord di MicrosoftDNS.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- DNS del metodo GetObjectByTextRepresentation
- DNS del metodo GetObjectByTextRepresentation, classe MicrosoftDNS_ResourceRecord
- Classe MicrosoftDNS_ResourceRecord DNS, metodo GetObjectByTextRepresentation
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
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477278"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Metodo GetObjectByTextRepresentation della classe MicrosoftDNS \_ ResourceRecord

Il metodo **GetObjectByTextRepresentation** recupera un'istanza esistente della classe [**\_ ResourceRecord di MicrosoftDNS**](microsoftdns-resourcerecord.md) .

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

*DnsServerName* \[ in\]
</dt> <dd>

Nome del server DNS da cui recuperare l'RR.

</dd> <dt>

*ContainerName* \[ in\]
</dt> <dd>

Nome del contenitore da cui ottenere l'RR.

</dd> <dt>

*TextRepresentation* \[ in\]
</dt> <dd>

Rappresentazione testuale dell'RR da recuperare.

</dd> <dt>

*RR* \[ out\]
</dt> <dd>

Riferimento all'RR di cui è stata creata un'istanza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Metodo CreateInstanceFromTextRepresentation della classe MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





