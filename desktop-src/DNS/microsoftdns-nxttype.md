---
title: MicrosoftDNS_NXTType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un RR Next (NXT).
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- MicrosoftDNS_NXTType DNS della classe
- MicrosoftDNS_NXTType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36fa67d3d1ab60aa4af6c0be7269f068edaf42a64fa9cf1cfea68ca23d82ef7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913101"
---
# <a name="microsoftdns_nxttype-class"></a>Classe \_ NXTType di MicrosoftDNS

Sottoclasse [**di MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un RR Next (NXT).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a>Members

La **classe \_ MicrosoftDNS NXTType** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MicrosoftDNS \_ NXTType** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un record di risorse NXT in base ai dati nei parametri di input del metodo: nome server DNS del record, nome contenitore, nome proprietario, classe (impostazione predefinita = IN), valore time-to-live e flag di mapping WINS, timeout di ricerca inversa, timeout della cache WINS e nome di dominio da aggiungere. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/>                                                                                                                                           |
| **Modifica**                         | Aggiorna il TTL, il flag di mapping, il timeout di ricerca, il timeout della cache e il dominio dei risultati ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/> **Windows Server 2003:** Questo metodo aggiorna anche NextDomainName e Types ai valori specificati come parametri di input di questo metodo.<br/> <br/> |



 

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ NXTType** ha queste proprietà.

<dl> <dt>

**NextDomainName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome di dominio successivo.

</dd> <dt>

**Tipi**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco delimitato da spazi dei nomi mnemoici di tipo RR per il nome del proprietario del record di risorse NXT.

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

[**Metodo CreateInstanceFromPropertyData della classe \_ NXTType MicrosoftDNS**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe \_ NXTType MicrosoftDNS**](microsoftdns-nxttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





