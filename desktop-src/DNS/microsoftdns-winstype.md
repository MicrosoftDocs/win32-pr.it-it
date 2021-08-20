---
title: MicrosoftDNS_WINSType classe
description: Sottoclasse di MicrosoftDNS ResourceRecord che rappresenta \_ Windows record WINS (Internet Name Service).
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- MicrosoftDNS_WINSType DNS della classe
- MicrosoftDNS_WINSType classe DNS , descritto
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
ms.openlocfilehash: 089faa6fa3cda6780b600dbf6c296fd1ce71f902428e6c2abe16f92dada1e219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162841"
---
# <a name="microsoftdns_winstype-class"></a>Classe \_ WINSType MicrosoftDNS

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta Windows record WINS (Internet Name Service).

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

La **classe \_ WINSType MicrosoftDNS** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ WINSType MicrosoftDNS** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo WINS di RR in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome del contenitore, nome del proprietario, classe (impostazione predefinita = IN), valore di time-to-live e flag di mapping WINS, timeout della ricerca, timeout della cache ed elenco di indirizzi IP per la ricerca. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Aggiorna I valori TTL, Flag di mapping, Timeout ricerca, Timeout cache e Wins ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>                      |



 

### <a name="properties"></a>Proprietà

La **classe \_ WINSType MicrosoftDNS** dispone di queste proprietà.

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

Tempo, in secondi, in cui un server DNS tenta di eseguire la risoluzione usando WINS Cerca.

</dd> <dt>

**MappingFlag**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Flag di mapping WINS che specifica se il record deve essere incluso nella replica di zona. Può avere solo due valori: 0x80000000 e 0x00010000 corrispondenti rispettivamente ai flag di replica e senza replica (record locale). I valori seguenti sono validi.



| Valore                                                                                                                                               | Significato                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Flag di replica<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Flag di nessuna replica (record locale)<br/> |



 

</dd> <dt>

**WinsServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di indirizzi IP delimitati da virgole dei server WINS usati nelle ricerca WINS.

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

[**Metodo CreateInstanceFromPropertyData della classe MICROSOFTDNS \_ WINSType**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe \_ WINSType MicrosoftDNS**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





