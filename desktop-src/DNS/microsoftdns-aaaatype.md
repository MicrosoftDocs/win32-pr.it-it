---
title: Classe MicrosoftDNS_AAAAType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di indirizzo IPv6 (aaaa). Il record AAAA è comunemente pronunciato \ 0034; quad-a record \ 0034;.
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- DNS della classe MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0131177c342730c08868946c29356554cbfb9cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301646"
---
# <a name="microsoftdns_aaaatype-class"></a>\_Classe MicrosoftDNS AAAAType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di indirizzo IPv6 (aaaa). Il record AAAA viene comunemente pronunciato "record quad-a".

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a>Members

La **classe \_ AAAAType di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ AAAAType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo ' AAAA ' di RR in base ai dati nei parametri di input del metodo, ovvero il nome del server DNS del record, il nome del contenitore, il nome del proprietario o dell'host, la classe (impostazione predefinita = IN), il valore di durata (TTL) e l'indirizzo IPv6. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementata, statica<br/> |
| **Modifica**                         | Aggiorna l'indirizzo TTL e IPv6 ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementato<br/>      |



 

### <a name="properties"></a>Proprietà

La **classe \_ AAAAType di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**IPv6Address**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo IPv6 per l'host.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della \_ classe AAAAType di MicrosoftDNS**](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





