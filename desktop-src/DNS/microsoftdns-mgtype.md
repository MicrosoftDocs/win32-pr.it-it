---
title: MicrosoftDNS_MGType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record del gruppo di posta (MG).
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- MicrosoftDNS_MGType DNS della classe
- MicrosoftDNS_MGType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af4a9b1f88a3d7e2752d2e4c199c261b49364ab7bdcbf4543e852f5218111491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692601"
---
# <a name="microsoftdns_mgtype-class"></a>Classe MGType MicrosoftDNS \_

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record del gruppo di posta (MG).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a>Members

La **classe MICROSOFTDNS \_ MGType** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MICROSOFTDNS \_ MGType** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Questo metodo crea un'istanza di un tipo MG di RR in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome contenitore, nome proprietario del gruppo di posta elettronica, classe (impostazione predefinita = IN), valore time-to-live e nome della cassetta postale. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Questo metodo aggiorna il TTL e la cassetta postale MG ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>                |



 

### <a name="properties"></a>Proprietà

La **classe MICROSOFTDNS \_ MGType** ha queste proprietà.

<dl> <dt>

**MGMailbox**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN che specifica una cassetta postale membro del gruppo di posta specificato dal nome del proprietario del record.

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

[**Metodo CreateInstanceFromPropertyData della classe MICROSOFTDNS \_ MGType**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe MICROSOFTDNS \_ MGType**](microsoftdns-mgtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





