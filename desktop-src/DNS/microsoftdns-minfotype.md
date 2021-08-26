---
title: MicrosoftDNS_MINFOType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record MINFO (Mail Information).
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- MicrosoftDNS_MINFOType DNS della classe
- MicrosoftDNS_MINFOType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_MINFOType.Modify
- MicrosoftDNS_MINFOType.ResponsibleMailbox
- MicrosoftDNS_MINFOType.ErrorMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6c04f6d87663534f9d1743ce09990de86fed9f7a16f78f26643f868554f58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967410"
---
# <a name="microsoftdns_minfotype-class"></a>Classe MicrosoftDNS \_ MINFOType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record MINFO (Mail Information).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_MINFOType : MicrosoftDNS_ResourceRecord
{
  string ResponsibleMailbox;
  string ErrorMailbox;
};
```

## <a name="members"></a>Members

La **classe MicrosoftDNS \_ MINFOType** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MicrosoftDNS \_ MINFOType** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo MINFO di RR in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome contenitore, nome proprietario dell'elenco di posta/casella, classe (impostazione predefinita = IN), valore time-to-live e cassette postali responsabili ed errori. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Questo metodo aggiorna il TTL, la cassetta postale responsabile e la cassetta postale di errore ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>    |



 

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ MINFOType** ha queste proprietà.

<dl> <dt>

**ErrorMailbox**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN che specifica una cassetta postale per ricevere messaggi di errore relativi alla lista di distribuzione o alla cassetta postale specificata dal nome del proprietario del record MINFO.

</dd> <dt>

**ResponsibleMailbox**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN che specifica una cassetta postale responsabile della mailing list o della cassetta postale specificata nel nome proprietario del record.

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

[**Metodo CreateInstanceFromPropertyData della classe \_ MicrosoftDNS MINFOType**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





