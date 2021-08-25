---
title: MicrosoftDNS_WKSType classe
description: Sottoclasse di MicrosoftDNS ResourceRecord che rappresenta \_ un record Well-Known Services (WKS).
ms.assetid: 7bbfd518-d473-4127-949b-9133a43ac7a7
keywords:
- MicrosoftDNS_WKSType DNS della classe
- MicrosoftDNS_WKSType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WKSType.Modify
- MicrosoftDNS_WKSType.InternetAddress
- MicrosoftDNS_WKSType.IPProtocol
- MicrosoftDNS_WKSType.Services
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82a6621e3dedacd5520c00b71c66bf0091c31135b70f27486ba43da63f393da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874761"
---
# <a name="microsoftdns_wkstype-class"></a>Classe WKSType MicrosoftDNS \_

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record Well-Known Services (WKS).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_WKSType : MicrosoftDNS_ResourceRecord
{
  string InternetAddress;
  string IPProtocol;
  string Services;
};
```

## <a name="members"></a>Members

La **classe \_ WKSType MicrosoftDNS** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ WKSType MicrosoftDNS** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo WKS di RR in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome del contenitore, nome del proprietario, classe (impostazione predefinita = IN), valore di time-to-live e indirizzo Internet, protocollo IP e maschera di bit della porta del proprietario. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/>  |
| **Modifica**                         | Questo metodo aggiorna la durata (TTL), l'indirizzo Internet, il protocollo IP e i servizi ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ WKSType MicrosoftDNS** ha queste proprietà.

<dl> <dt>

**InternetAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo IP Internet per il proprietario del record.

</dd> <dt>

**IPProtocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che rappresenta il protocollo IP per questo record. I valori validi sono UDP o TCP.

</dd> <dt>

**Services**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa contenente tutti i servizi usati dal record well known service (WKS).

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

[**Metodo CreateInstanceFromPropertyData della classe WKSType MicrosoftDNS \_**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe \_ WKSType MicrosoftDNS**](microsoftdns-wkstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





