---
title: Classe MicrosoftDNS_Statistic
description: La \_ classe statistica MicrosoftDNS rappresenta una singola statistica del server DNS.
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- DNS della classe MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e26f1738c046e446fa898c4fdff2f6e8855730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048640"
---
# <a name="microsoftdns_statistic-class"></a>\_Classe statistica MicrosoftDNS

La **classe \_ statistica MicrosoftDNS** rappresenta una singola statistica del server DNS.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a>Members

La **classe \_ statistica MicrosoftDNS** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ statistica MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Rappresentazione numerica di **CollectionName**.

</dd> <dt>

**CollectionName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della raccolta a cui appartiene la statistica.

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il nome di dominio completo o l'indirizzo IP del server DNS che contiene la statistica.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della statistica.

</dd> <dt>

**StringValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore stringa della statistica, utilizzato solo quando il valore statistico non è rappresentato come DWORD.

</dd> <dt>

**Valore**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore numerico della statistica, rappresentato come DWORD.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MicrosoftDNS \_ StatisticCollection](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





