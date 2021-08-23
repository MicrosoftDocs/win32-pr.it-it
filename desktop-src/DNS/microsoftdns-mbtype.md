---
title: MicrosoftDNS_MBType classe
description: Sottoclasse di MicrosoftDNS ResourceRecord che rappresenta un record di risorse \_ cassetta postale (MB).
ms.assetid: b8f3b106-58f4-44b8-b2db-b00f1a495641
keywords:
- MicrosoftDNS_MBType DNS della classe
- MicrosoftDNS_MBType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
- MicrosoftDNS_MBType.Modify
- MicrosoftDNS_MBType.MBHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccea0cc9c30fb8a46debedaa2aeb0811ed63b08005919c7f189d771fd7daed2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163265"
---
# <a name="microsoftdns_mbtype-class"></a>Classe \_ MBType MicrosoftDNS

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord che**](microsoftdns-resourcerecord.md) rappresenta un record di risorse cassetta postale (MB).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_MBType : MicrosoftDNS_ResourceRecord
{
  string MBHost;
};
```

## <a name="members"></a>Members

La **classe \_ MBType MicrosoftDNS** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ MBType MicrosoftDNS** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di MB RR in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome del contenitore, nome del proprietario della cassetta postale, classe (impostazione predefinita = IN), valore di time-to-live e host della cassetta postale. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Aggiorna l'host TTL e MB ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>        |



 

### <a name="properties"></a>Proprietà

La **classe \_ MBType MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**MBHost**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN che specifica un host della cassetta postale specificato nel nome del proprietario del record.

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

[**Metodo CreateInstanceFromPropertyData della classe \_ MBType MicrosoftDNS**](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe \_ MBType MicrosoftDNS**](microsoftdns-mbtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





