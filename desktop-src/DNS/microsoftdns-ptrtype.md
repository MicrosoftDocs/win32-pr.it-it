---
title: Classe MicrosoftDNS_PTRType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record puntatore (PTR).
ms.assetid: 2cb0f13b-e683-473b-9cdd-bc5d805b919d
keywords:
- DNS della classe MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
- MicrosoftDNS_PTRType.Modify
- MicrosoftDNS_PTRType.PTRDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65dc434eb751ed925ab9efcdaf29f04741b749ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517950"
---
# <a name="microsoftdns_ptrtype-class"></a>\_Classe MicrosoftDNS PTRType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record puntatore (PTR).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_PTRType : MicrosoftDNS_ResourceRecord
{
  string PTRDomainName;
};
```

## <a name="members"></a>Members

La **classe \_ PTRType di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ PTRType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un record di risorsa PTR DNS basato sui dati nei parametri di input del metodo, ovvero il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata (TTL) e il nome di dominio completo (FQDN) del record PTR. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementata, statica<br/> |
| **Modifica**                         | Aggiorna il nome di dominio TTL e PTR ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementato<br/>                 |



 

### <a name="properties"></a>Proprietà

La **classe \_ PTRType di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**PTRDomainName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN dei dati del record PTR.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della \_ classe PTRType di MicrosoftDNS**](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





