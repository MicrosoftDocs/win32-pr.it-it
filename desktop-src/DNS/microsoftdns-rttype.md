---
title: MicrosoftDNS_RTType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record Route Through (RT).
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- MicrosoftDNS_RTType DNS della classe
- MicrosoftDNS_RTType classe DNS , descritto
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
ms.openlocfilehash: 287dc3d80370f812b6ee721b9556f906df289c67a17048aa326efc3b80de5954
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077061"
---
# <a name="microsoftdns_rttype-class"></a>Classe MicrosoftDNS \_ RTType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record Route Through (RT).

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

La **classe MicrosoftDNS \_ RTType** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MicrosoftDNS \_ RTType** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo RT di RR in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome del contenitore, nome proprietario/host, classe (impostazione predefinita = IN), valore di time-to-live, preferenza del record e nome host intermedio. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Aggiorna la durata (TTL), la preferenza e l'host intermedio ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>        |



 

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ RTType** dispone di queste proprietà.

<dl> <dt>

**IntermediateHost**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN che specifica un host da utilizzare come intermedio per raggiungere l'host specificato dal proprietario.

</dd> <dt>

**Preferenza**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Preferenza data a questo RR tra le altre presso lo stesso proprietario. Sono preferibili valori inferiori.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ RTType**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe MicrosoftDNS \_ RTType**](microsoftdns-rttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





