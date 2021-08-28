---
title: MicrosoftDNS_RPType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record responsabile.
ms.assetid: 2b1c1bbc-a69f-4480-a7f2-6420240d4ad8
keywords:
- MicrosoftDNS_RPType dns di classe
- MicrosoftDNS_RPType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
- MicrosoftDNS_RPType.Modify
- MicrosoftDNS_RPType.RPMailbox
- MicrosoftDNS_RPType.TXTDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2088420acc7a8d0e58cfa23ed95458c797dbe9f930651bc02f083fcc81f5342d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655371"
---
# <a name="microsoftdns_rptype-class"></a>Classe \_ MicrosoftDNS RPType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record responsabile.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_RPType : MicrosoftDNS_ResourceRecord
{
  string RPMailbox;
  string TXTDomainName;
};
```

## <a name="members"></a>Members

La **classe MicrosoftDNS \_ RPType** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MicrosoftDNS \_ RPType** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo RP di RR in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome contenitore, nome proprietario/persona responsabile, classe (impostazione predefinita = IN), valore time-to-live e nomi di dominio per la cassetta postale della persona e le posizioni txt RR. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Questo metodo aggiorna TTL, RP Mailbox e TXT Domain Name ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>                                  |



 

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ RPType** ha queste proprietà.

<dl> <dt>

**RPMailbox**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN che specifica la cassetta postale per la persona responsabile.

</dd> <dt>

**TXTDomainName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN per cui sono presenti record di risorse TXT.

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

[**Metodo CreateInstanceFromPropertyData della classe \_ MicrosoftDNS RPType**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe \_ MicrosoftDNS RPType**](microsoftdns-rptype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





