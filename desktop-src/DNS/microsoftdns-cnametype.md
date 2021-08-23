---
title: MicrosoftDNS_CNAMEType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record CNAME (Canonical Name).
ms.assetid: 93a972e3-abb1-425f-beb7-32abe7d0b485
keywords:
- MicrosoftDNS_CNAMEType DNS della classe
- MicrosoftDNS_CNAMEType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
- MicrosoftDNS_CNAMEType.Modify
- MicrosoftDNS_CNAMEType.PrimaryName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e819380726fb311d3e892ff3ae1610890f87330cc3d15ac7e9459985aa775354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076845"
---
# <a name="microsoftdns_cnametype-class"></a>Classe \_ CNAMEType MicrosoftDNS

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record CNAME (Canonical Name).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_CNAMEType : MicrosoftDNS_ResourceRecord
{
  string PrimaryName;
};
```

## <a name="members"></a>Members

La **classe \_ CNAMEType MicrosoftDNS** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ CNAMEType MicrosoftDNS** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un record di risorse CNAME in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome del contenitore, nome del proprietario, classe (impostazione predefinita = IN), valore di time-to-live e nome primario del record CNAME. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Aggiorna la durata (TTL) e il nome primario ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>                        |



 

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ CNAMEType** dispone di queste proprietà.

<dl> <dt>

**PrimaryName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome canonico o primario per il proprietario del record CNAME.

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

[**Metodo CreateInstanceFromPropertyData della classe CNAMEType MicrosoftDNS \_**](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe CNAMEType MicrosoftDNS \_**](microsoftdns-cnametype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





