---
title: MicrosoftDNS_AFSDBType classe
description: Sottoclasse di MicrosoftDNS ResourceRecord che rappresenta un record del \_ server di database del file system andrew (AFSDB).
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- MicrosoftDNS_AFSDBType DNS della classe
- MicrosoftDNS_AFSDBType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c7887d51e58b8c34374ed5ca96d0206472155872ba573b7b9f8879329910f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815701"
---
# <a name="microsoftdns_afsdbtype-class"></a>Classe \_ MicrosoftDNS AFSDBType

Sottoclasse [**di MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di Andrew File System Database Server (AFSDB).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a>Members

La **classe \_ MicrosoftDNS AFSDBType** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MicrosoftDNS \_ AFSDBType** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un record di risorse AFSDB in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome contenitore, nome proprietario/cella, classe (impostazione predefinita = IN), valore time-to-live e sottotipo e nome del server AFS host. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Questo metodo aggiorna il TTL, il sottotipo e il nome del server ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>   |



 

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ AFSDBType** ha queste proprietà.

<dl> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN che specifica un host con un server per la cella AFS specificata nel nome del proprietario.

</dd> <dt>

**Sottotipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Sottotipo del server AFS host. Per il sottotipo 1 (valore=1), l'host dispone di un server di posizione del volume AFS versione 3.0 per la cella AFS denominata. Nel caso del sottotipo 2 (value=2), l'host ha un server dei nomi autenticato che contiene il nodo della directory radice della cella per la cella DCE/NCA denominata.

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

[**Metodo CreateInstanceFromPropertyData della classe \_ MicrosoftDNS AFSDBType**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe \_ MicrosoftDNS AFSDBType**](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





