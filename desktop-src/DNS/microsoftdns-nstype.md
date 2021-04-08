---
title: Classe MicrosoftDNS_NSType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record del server dei nomi (NS).
ms.assetid: 8d229acd-bc47-4a32-b6f1-b784a48dc91a
keywords:
- DNS della classe MicrosoftDNS_NSType
- MicrosoftDNS_NSType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType
- MicrosoftDNS_NSType.CreateInstanceFromPropertyData
- MicrosoftDNS_NSType.Modify
- MicrosoftDNS_NSType.NSHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07155c36089e60b12aeea214b19cb8aca146005a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964993"
---
# <a name="microsoftdns_nstype-class"></a>\_Classe MicrosoftDNS NSType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record del server dei nomi (NS).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_NSType : MicrosoftDNS_ResourceRecord
{
  string NSHost;
};
```

## <a name="members"></a>Members

La **classe \_ NSType di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ NSType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un record di risorse NS DNS basato sui dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore di durata e l'host con autorità per il dominio. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementata, statica<br/> |
| **Modifica**                         | Aggiorna l'host TTL e NS ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementato<br/>                               |



 

### <a name="properties"></a>Proprietà

La **classe \_ NSType di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**NSHost**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Host autorevole per il dominio.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ NSType**](microsoftdns-nstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della \_ classe NSType di MicrosoftDNS**](microsoftdns-nstype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





