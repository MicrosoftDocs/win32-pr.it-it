---
title: Classe MicrosoftDNS_WINSType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record WINS (Windows Internet Name Service).
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- DNS della classe MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSType.Modify
- MicrosoftDNS_WINSType.MappingFlag
- MicrosoftDNS_WINSType.LookupTimeout
- MicrosoftDNS_WINSType.CacheTimeout
- MicrosoftDNS_WINSType.WinsServers
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce23132073305142948518327ea5b6c7e46f1289
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874093"
---
# <a name="microsoftdns_winstype-class"></a>\_Classe MicrosoftDNS WINSType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record WINS (Windows Internet Name Service).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_WINSType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string WinsServers;
};
```

## <a name="members"></a>Members

La **classe \_ WINSType di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ WINSType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo WINS di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata (TTL) e il flag di mapping WINS, il timeout di ricerca, il timeout della cache e l'elenco degli indirizzi IP per la ricerca Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementata, statica<br/> |
| **Modifica**                         | Aggiorna il valore TTL, il flag di mapping, il timeout di ricerca, il timeout della cache e i server WINS ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementato<br/>                      |



 

### <a name="properties"></a>Proprietà

La **classe \_ WINSType di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**CacheTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo, in secondi, per cui un server DNS che usa la ricerca WINS può memorizzare nella cache la risposta del server WINS.

</dd> <dt>

**LookupTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo, in secondi, durante il quale un server DNS tenta la risoluzione usando la ricerca di WINS.

</dd> <dt>

**MappingFlag**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Flag di mapping WINS che specifica se il record deve essere incluso nella replica della zona. Potrebbero essere presenti solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale). I valori seguenti sono validi.



| Valore                                                                                                                                               | Significato                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Flag di replica<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Flag senza replica (record locale)<br/> |



 

</dd> <dt>

**WinsServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di indirizzi IP delimitati da virgole dei server WINS utilizzati nelle ricerche WINS.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ WINSType**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della \_ classe WINSType di MicrosoftDNS**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





