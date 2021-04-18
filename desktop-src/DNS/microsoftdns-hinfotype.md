---
title: Classe MicrosoftDNS_HINFOType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di informazioni sull'host (HINFO).
ms.assetid: c6591010-0fe6-45b2-9032-9f847237ecf6
keywords:
- DNS della classe MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_HINFOType.Modify
- MicrosoftDNS_HINFOType.CPU
- MicrosoftDNS_HINFOType.OS
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3298e5a7f90dbaee24e5014b1a3aab76ad6997
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302040"
---
# <a name="microsoftdns_hinfotype-class"></a>\_Classe MicrosoftDNS HINFOType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di informazioni sull'host (HINFO).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_HINFOType : MicrosoftDNS_ResourceRecord
{
  string CPU;
  string OS;
};
```

## <a name="members"></a>Members

La **classe \_ HINFOType di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ HINFOType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un HINFO di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore time-to-Live e i tipi di CPU e del sistema operativo dell'host. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementata, statica<br/> |
| **Modifica**                         | Aggiorna il TTL, la CPU e il sistema operativo ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementato<br/>          |



 

### <a name="properties"></a>Proprietà

La **classe \_ HINFOType di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**CPU**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di CPU del proprietario del record.

</dd> <dt>

**Sistema operativo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Sistema operativo del proprietario del record.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della \_ classe HINFOType di MicrosoftDNS**](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





