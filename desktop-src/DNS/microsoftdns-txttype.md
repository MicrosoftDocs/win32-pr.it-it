---
title: MicrosoftDNS_TXTType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record text (TXT).
ms.assetid: e4bd445f-71c4-48dc-b210-e3ad4452d2e5
keywords:
- MicrosoftDNS_TXTType DNS della classe
- MicrosoftDNS_TXTType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_TXTType.Modify
- MicrosoftDNS_TXTType.DescriptiveText
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6f288978d5dff0d184dc0e026350e3ada1c16d3fd21c9aec26deea0272e338a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109081"
---
# <a name="microsoftdns_txttype-class"></a>Classe TXTType di MicrosoftDNS \_

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record text (TXT).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_TXTType : MicrosoftDNS_ResourceRecord
{
  string DescriptiveText;
};
```

## <a name="members"></a>Members

La **classe \_ TXTType di MicrosoftDNS** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ TXTType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo TXT di RR in base ai dati nei parametri di input del metodo: nome server DNS del record, nome contenitore, nome proprietario, classe (impostazione predefinita = IN), valore time-to-live e testo del record. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/>        |
| **Modifica**                         | Aggiorna il TTL e il testo descrittivo ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ TXTType di MicrosoftDNS** ha queste proprietà.

<dl> <dt>

**Testo descrittivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Testo descrittivo, la cui semantica dipende dal dominio del proprietario.

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

[**Metodo CreateInstanceFromPropertyData della classe TXTType MicrosoftDNS \_**](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe TXTType MicrosoftDNS \_**](microsoftdns-txttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





