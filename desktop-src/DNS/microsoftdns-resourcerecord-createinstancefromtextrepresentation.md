---
title: Metodo CreateInstanceFromTextRepresentation della classe MicrosoftDNS_ResourceRecord
description: Il metodo CreateInstanceFromTextRepresentation crea un'istanza di un oggetto \_ ResourceRecord MicrosoftDNS.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- DNS del metodo CreateInstanceFromTextRepresentation
- Metodo CreateInstanceFromTextRepresentation DNS, MicrosoftDNS_ResourceRecord classe
- MicrosoftDNS_ResourceRecord classe DNS, metodo CreateInstanceFromTextRepresentation
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
ms.openlocfilehash: 4a8ee7f92db1185fe2762b0b308b4fbafdbdd80e7417c7b615939c72333f15e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104021"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Metodo CreateInstanceFromTextRepresentation della classe ResourceRecord MicrosoftDNS \_

Il **metodo CreateInstanceFromTextRepresentation** crea un'istanza di un [**oggetto \_ ResourceRecord MicrosoftDNS.**](microsoftdns-resourcerecord.md)

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

*DnsServerName* \[ Pollici\]
</dt> <dd>

Nome del server DNS in cui deve essere creato il RR.

</dd> <dt>

*ContainerName* \[ Pollici\]
</dt> <dd>

Nome del contenitore in cui inserire il nuovo RR.

</dd> <dt>

*TextRepresentation* \[ Pollici\]
</dt> <dd>

Rappresentazione testuale dell'istanza di RR da creare.

</dd> <dt>

*RR* \[ out, ref\]
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

[**Metodo GetObjectByTextRepresentation della classe ResourceRecord MicrosoftDNS \_**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





