---
title: MicrosoftDNS_SRVType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record del servizio (SRV).
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- MicrosoftDNS_SRVType DNS della classe
- MicrosoftDNS_SRVType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaff2c570647386ecd8d53592b940cbd54477764b323b5457dbec3357cf3b98c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104011"
---
# <a name="microsoftdns_srvtype-class"></a>Classe MicrosoftDNS \_ SRVType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record del servizio (SRV).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a>Members

La **classe MicrosoftDNS \_ SRVType** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MicrosoftDNS \_ SRVType** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo SRV di RR in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome del contenitore, nome proprietario/destinazione, classe (impostazione predefinita = IN), valore di time-to-live e priorità, peso, porta e nome di dominio dell'host di destinazione. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Aggiorna TTL, Priority, Weight, Port e Domain Name ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>                  |



 

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ SRVType** ha queste proprietà.

<dl> <dt>

**Porta**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Porta utilizzata nell'host di destinazione di un servizio di protocollo.

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Priorità dell'host di destinazione specificato nel nome del proprietario. I numeri più bassi implicano priorità più elevate.

</dd> <dt>

**SRVDomainName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN dell'host di destinazione. Una destinazione \\ di significa che il servizio non è decisamente disponibile in questo \\ dominio.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Peso dell'host di destinazione. Ciò è utile quando si selezionano tra host con la stessa priorità. Le probabilità di usare questo host devono essere proporzionali al peso.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SRVType**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe MicrosoftDNS \_ SRVType**](microsoftdns-srvtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





