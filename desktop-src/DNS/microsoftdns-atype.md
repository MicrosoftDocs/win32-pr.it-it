---
title: MicrosoftDNS_AType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di indirizzo host (A).
ms.assetid: c7bd8a26-b0ac-49ef-9068-a0ecddeb6ef4
keywords:
- MicrosoftDNS_AType dns di classe
- MicrosoftDNS_AType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
- MicrosoftDNS_AType.Modify
- MicrosoftDNS_AType.IPAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb5cd5735d30d4b512c2dd382f6ef59b182da51c99df26ccebddbdc0e2a1837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574091"
---
# <a name="microsoftdns_atype-class"></a>Classe \_ MicrosoftDNS AType

Sottoclasse [**di MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di indirizzo host (A).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_AType : MicrosoftDNS_ResourceRecord
{
  string IPAddress;
};
```

## <a name="members"></a>Members

La **classe \_ MicrosoftDNS AType** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ MicrosoftDNS AType** ha questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un RR dell'indirizzo host (A) in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome contenitore, nome proprietario, classe (impostazione predefinita = IN), valore time-to-live e indirizzo IP dell'host. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Aggiorna il TTL e l'indirizzo IP ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>             |



 

### <a name="properties"></a>Proprietà

La **classe \_ MicrosoftDNS AType** ha queste proprietà.

<dl> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che rappresenta l'indirizzo IPv4 dell'host.

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe AType MicrosoftDNS \_**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe AType MicrosoftDNS \_**](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





