---
title: MicrosoftDNS_ISDNType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record ISDN.
ms.assetid: 8925042c-65d3-465f-aedd-9f7c862620b5
keywords:
- MicrosoftDNS_ISDNType DNS della classe
- MicrosoftDNS_ISDNType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
- MicrosoftDNS_ISDNType.Modify
- MicrosoftDNS_ISDNType.ISDNNumber
- MicrosoftDNS_ISDNType.SubAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af06ad782b6d36213e9a1df210916f9346e1e4f8bd0a98dd619651a579dc5c4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131721"
---
# <a name="microsoftdns_isdntype-class"></a>Classe \_ ISDNType di MicrosoftDNS

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record ISDN.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_ISDNType : MicrosoftDNS_ResourceRecord
{
  string ISDNNumber;
  string SubAddress;
};
```

## <a name="members"></a>Members

La **classe \_ MICROSOFTDNS ISDNType** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ MICROSOFTDNS ISDNType** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un record di risorse ISDN in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome contenitore, nome proprietario, classe (impostazione predefinita = IN), valore time-to-live e numero ISDN e sottoindirizzo del proprietario. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Aggiorna il TTL, il numero ISDN e il sottoindirizzo ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>                   |



 

### <a name="properties"></a>Proprietà

La **classe MICROSOFTDNS \_ ISDNType** ha queste proprietà.

<dl> <dt>

**ISDNNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero ISDN e DDI del proprietario del record.

</dd> <dt>

**Sottoindirizzo**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Sottoindirizzo del proprietario, se definito.

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

[**Metodo CreateInstanceFromPropertyData della classe \_ MICROSOFTDNS ISDNType**](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe \_ MICROSOFTDNS ISDNType**](microsoftdns-isdntype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





