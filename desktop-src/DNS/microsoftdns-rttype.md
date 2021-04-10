---
title: Classe MicrosoftDNS_RTType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record route through (RT).
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- DNS della classe MicrosoftDNS_RTType
- MicrosoftDNS_RTType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d867185d8ce07a54a47eb5ea7591ec8d68a11059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964371"
---
# <a name="microsoftdns_rttype-class"></a>\_Classe MicrosoftDNS RTType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record route through (RT).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a>Members

La **classe \_ RTType di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ RTType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo RT di RR in base ai dati nei parametri di input del metodo, ovvero il nome del server DNS del record, il nome del contenitore, il nome del proprietario o dell'host, la classe (impostazione predefinita = IN), il valore time-to-Live, la preferenza di record e il nome host intermedio. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementata, statica<br/> |
| **Modifica**                         | Aggiorna la durata (TTL), la preferenza e l'host intermedio ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementato<br/>        |



 

### <a name="properties"></a>Proprietà

La **classe \_ RTType di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**IntermediateHost**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN che specifica un host che funge da intermediario per raggiungere l'host specificato dal proprietario.

</dd> <dt>

**Preferenza**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Preferenza assegnata a questo RR tra gli altri nello stesso proprietario. Sono preferibili valori inferiori.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ RTType**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della \_ classe RTType di MicrosoftDNS**](microsoftdns-rttype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





