---
title: Classe MicrosoftDNS_SRVType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di servizio (SRV).
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- DNS della classe MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType della classe DNS, descritta
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
ms.openlocfilehash: aea955cad281e9361b4fa1ca5b033a4ca0d39719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477266"
---
# <a name="microsoftdns_srvtype-class"></a>\_Classe MicrosoftDNS SRVType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di servizio (SRV).

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

La **classe \_ SRVType di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ SRVType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo SRV di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario/destinazione, la classe (impostazione predefinita = IN), il valore di durata (TTL) e la priorità, il peso, la porta e il nome di dominio dell'host di destinazione. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementata, statica<br/> |
| **Modifica**                         | Aggiorna i valori TTL, Priority, Weight, Port e Domain Name con i valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementato<br/>                  |



 

### <a name="properties"></a>Proprietà

La **classe \_ SRVType di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**Porta**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Porta utilizzata nell'host di destinazione di un servizio del protocollo.

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Priorità dell'host di destinazione specificato nel nome del proprietario. I numeri più bassi implicano priorità più elevate.

</dd> <dt>

**SRVDomainName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN dell'host di destinazione. Destinazione di \\ . \\ indica che il servizio non è disponibile in questo dominio.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Peso dell'host di destinazione. Questa operazione è utile quando si seleziona tra gli host con la stessa priorità. La possibilità di utilizzare questo host deve essere proporzionale al suo peso.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SRVType**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della \_ classe SRVType di MicrosoftDNS**](microsoftdns-srvtype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





