---
title: Classe MicrosoftDNS_ATMAType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un indirizzo ATM per il nome (ATMA) record.
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- DNS della classe MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237dc4ecb657e79e835abcfdacf90844fb05c5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964226"
---
# <a name="microsoftdns_atmatype-class"></a>\_Classe MicrosoftDNS ATMAType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un indirizzo ATM per il nome (ATMA) record.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a>Members

La **classe \_ ATMAType di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ ATMAType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un record di risorse ATMA basato sui dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario/nodo, la classe (impostazione predefinita = IN), il valore di durata (TTL) e il formato e l'indirizzo ATM. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementata, statica<br/> |
| **Modifica**                         | Aggiorna l'indirizzo TTL, format e ATMA ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementato<br/>         |



 

### <a name="properties"></a>Proprietà

La **classe \_ ATMAType di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**ATMAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa di lunghezza variabile di ottetti che contiene l'indirizzo ATM del nodo/proprietario a cui si riferisce questo RR. I primi 4 byte della matrice vengono usati per archiviare le dimensioni della stringa di ottetto. Il byte più significativo viene archiviato nel byte 0.

</dd> <dt>

**Formato**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Formato dell'indirizzo ATM. I valori validi sono: 0 che indica il formato AESA (ATM End System Address) e 1 che indica il formato E. 164.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della \_ classe ATMAType di MicrosoftDNS**](microsoftdns-atmatype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





