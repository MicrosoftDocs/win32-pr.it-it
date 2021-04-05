---
title: Metodo CreateInstanceFromTextRepresentation della classe MicrosoftDNS_ResourceRecord
description: Il metodo CreateInstanceFromTextRepresentation crea un'istanza di un \_ oggetto ResourceRecord MicrosoftDNS.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- DNS del metodo CreateInstanceFromTextRepresentation
- DNS del metodo CreateInstanceFromTextRepresentation, classe MicrosoftDNS_ResourceRecord
- Classe MicrosoftDNS_ResourceRecord DNS, metodo CreateInstanceFromTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a578d036180ecb1dc8a5e66bf853eec8845583f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048473"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Metodo CreateInstanceFromTextRepresentation della classe MicrosoftDNS \_ ResourceRecord

Il metodo **CreateInstanceFromTextRepresentation** crea un'istanza di un oggetto [**\_ ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md) .

## <a name="syntax"></a>Sintassi


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DnsServerName* \[ in\]
</dt> <dd>

Nome del server DNS in cui deve essere creato l'RR.

</dd> <dt>

*ContainerName* \[ in\]
</dt> <dd>

Nome del contenitore in cui deve essere inserito il nuovo RR.

</dd> <dt>

*TextRepresentation* \[ in\]
</dt> <dd>

Rappresentazione testo dell'istanza di RR da creare.

</dd> <dt>

*RR* \[ out, Ref\]
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

[**Metodo GetObjectByTextRepresentation della classe MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





