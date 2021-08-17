---
title: MicrosoftDNS_MFType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record MF (Mail Forwarding Agent for Domain).
ms.assetid: 0ba0fddd-c316-4a5b-ad65-6344dbe949c1
keywords:
- MicrosoftDNS_MFType DNS della classe
- MicrosoftDNS_MFType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
- MicrosoftDNS_MFType.Modify
- MicrosoftDNS_MFType.MFHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e0b2f2e08a7e9144f2fe2a6ac3e94578428109d7f3e712ac8c54752721f7592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163212"
---
# <a name="microsoftdns_mftype-class"></a>Classe MicrosoftDNS \_ MFType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record MF (Mail Forwarding Agent for Domain).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_MFType : MicrosoftDNS_ResourceRecord
{
  string MFHost;
};
```

## <a name="members"></a>Members

La **classe MicrosoftDNS \_ MFType** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MicrosoftDNS \_ MFType** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                            |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Questo metodo crea un'istanza di un tipo MF di RR in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome del contenitore, nome del proprietario del dominio, classe (impostazione predefinita = IN), valore di time-to-live e host dell'agente di posta elettronica. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Questo metodo aggiorna la durata (TTL) e l'host MF (MF Host) ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>                         |



 

### <a name="properties"></a>Proprietà

La **classe MicrosoftDNS \_ MFType** ha queste proprietà.

<dl> <dt>

**MFHost**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN che specifica un host con un agente di posta che accetterà la posta per l'inoltro al dominio specificato.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MFType**](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe MicrosoftDNS \_ MFType**](microsoftdns-mftype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





