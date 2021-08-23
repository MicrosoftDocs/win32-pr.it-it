---
title: MicrosoftDNS_X25Type classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record X.25 (X25).
ms.assetid: 1213dfd7-30b3-413e-b723-f4284fa0b416
keywords:
- MicrosoftDNS_X25Type DNS della classe
- MicrosoftDNS_X25Type classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
- MicrosoftDNS_X25Type.Modify
- MicrosoftDNS_X25Type.PSDNAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46f57cdd5dce38c57214d91108a548a4f4890df6d44c0909a706c8e57c383a49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655281"
---
# <a name="microsoftdns_x25type-class"></a>Classe MicrosoftDNS \_ X25Type

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record X.25 (X25).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_X25Type : MicrosoftDNS_ResourceRecord
{
  string PSDNAddress;
};
```

## <a name="members"></a>Members

La **classe MicrosoftDNS \_ X25Type** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MicrosoftDNS \_ X25Type** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo "X25" di RR in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome del contenitore, nome del proprietario, classe (impostazione predefinita = IN), valore di time-to-live e indirizzo PSDN. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/>              |
| **Modifica**                         | Questo metodo aggiorna la durata (TTL) e l'indirizzo PSDN ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/> |



 

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ X25Type** ha queste proprietà.

<dl> <dt>

**PSDNAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo PSDN del proprietario di RR.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ X25Type**](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe MicrosoftDNS \_ X25Type**](microsoftdns-x25type-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





