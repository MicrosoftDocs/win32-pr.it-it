---
title: MicrosoftDNS_MDType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un agente di posta per il record di dominio (MD).
ms.assetid: 11242372-65fe-44ee-845b-2430aec59127
keywords:
- MicrosoftDNS_MDType DNS della classe
- MicrosoftDNS_MDType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
- MicrosoftDNS_MDType.Modify
- MicrosoftDNS_MDType.MDHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de51a9d60b110f8b8305655e8ef9be7c656a8314c41a7b96c59d2c300405495d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825091"
---
# <a name="microsoftdns_mdtype-class"></a>Classe \_ MDType MicrosoftDNS

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord che**](microsoftdns-resourcerecord.md) rappresenta un agente di posta per il record di dominio (MD).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_MDType : MicrosoftDNS_ResourceRecord
{
  string MDHost;
};
```

## <a name="members"></a>Members

La **classe \_ MDType MicrosoftDNS** include i tipi di membri seguenti:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ MDType MicrosoftDNS** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un record di risorse MD DNS in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome del contenitore, nome del proprietario del dominio, classe (impostazione predefinita = IN), valore di time-to-live e host dell'agente di posta elettronica. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Aggiorna l'host TTL e MD ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>                                 |



 

### <a name="properties"></a>Proprietà

La **classe \_ MDType MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**MDHost**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN che specifica un host con un agente di posta in grado di recapitare la posta per il dominio specificato.

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

[**Metodo CreateInstanceFromPropertyData della classe MDType MicrosoftDNS \_**](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe MDType MicrosoftDNS \_**](microsoftdns-mdtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





