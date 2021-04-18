---
title: Classe MicrosoftDNS_AType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di indirizzo host (a).
ms.assetid: c7bd8a26-b0ac-49ef-9068-a0ecddeb6ef4
keywords:
- DNS della classe MicrosoftDNS_AType
- MicrosoftDNS_AType della classe DNS, descritta
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
ms.openlocfilehash: 25e856968e2c3d4e581d69e0ac7bcbddc256424c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301642"
---
# <a name="microsoftdns_atype-class"></a>\_Classe MicrosoftDNS aType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di indirizzo host (a).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_AType : MicrosoftDNS_ResourceRecord
{
  string IPAddress;
};
```

## <a name="members"></a>Members

La **classe \_ aType di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ aType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un indirizzo host (A) RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore time-to-Live e l'indirizzo IP dell'host. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementata, statica<br/> |
| **Modifica**                         | Aggiorna il valore TTL e l'indirizzo IP ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementato<br/>             |



 

### <a name="properties"></a>Proprietà

La **classe \_ aType di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
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
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ aType**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della \_ classe aType di MicrosoftDNS**](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





