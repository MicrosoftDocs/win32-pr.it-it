---
title: MicrosoftDNS_WINSRType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record WINS Reverse Look-up (WINSR).
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- MicrosoftDNS_WINSRType DNS della classe
- MicrosoftDNS_WINSRType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSRType.Modify
- MicrosoftDNS_WINSRType.MappingFlag
- MicrosoftDNS_WINSRType.LookupTimeout
- MicrosoftDNS_WINSRType.CacheTimeout
- MicrosoftDNS_WINSRType.ResultDomain
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89c9545c73a4dbd5a01ff401c7b5587cf448553fcafcf4d698e3aeb17ed8722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912821"
---
# <a name="microsoftdns_winsrtype-class"></a>Classe MICROSOFTDNS \_ WINSRType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record WINS Reverse Look-up (WINSR).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_WINSRType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string ResultDomain;
};
```

## <a name="members"></a>Members

La **classe MICROSOFTDNS \_ WINSRType** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MICROSOFTDNS \_ WINSRType** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo WINSR di RR in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome del contenitore, nome del proprietario, classe (impostazione predefinita = IN), valore di time-to-live e flag di mapping WINS, timeout di ricerca inversa, timeout della cache WINS e nome di dominio da aggiungere. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Aggiorna la durata (TTL), il flag di mapping, il timeout di ricerca, il timeout della cache e il dominio dei risultati ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>                        |



 

### <a name="properties"></a>Proprietà

La **classe \_ WINSRType MicrosoftDNS** ha queste proprietà.

<dl> <dt>

**CacheTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo, in secondi, in cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.

</dd> <dt>

**LookupTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Timeout, in secondi, per un server DNS che usa la ricerca inversa WINS.

</dd> <dt>

**MappingFlag**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Flag di mapping WINSR che specifica se il record deve essere incluso nella replica di zona. Può avere solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale).

</dd> <dt>

**ResultDomain**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome di dominio da aggiungere ai nomi NetBIOS restituiti.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MICROSOFTDNS \_ WINSRType**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe MICROSOFTDNS \_ WINSRType**](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





