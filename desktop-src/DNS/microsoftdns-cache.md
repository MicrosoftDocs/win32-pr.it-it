---
title: Classe MicrosoftDNS_Cache
description: La \_ classe cache MicrosoftDNS descrive una cache esistente in un server DNS.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- DNS della classe MicrosoftDNS_Cache
- MicrosoftDNS_Cache della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048374"
---
# <a name="microsoftdns_cache-class"></a>\_Classe della cache MicrosoftDNS

La **classe \_ cache MicrosoftDNS** descrive una cache esistente in un server DNS. Questa classe semplifica la visualizzazione dell'indipendenza degli oggetti DNS anziché la rappresentazione di un oggetto reale. La classe della **\_ cache MicrosoftDNS** è un contenitore per i record di risorse memorizzati nella cache dal server DNS. Non confondere questo oggetto con un file di cache che contiene parametri radice.

Ogni istanza della **\_ cache MicrosoftDNS** della classe deve essere assegnata esattamente a un server DNS. Può essere associato a più istanze del [**\_ dominio MicrosoftDNS**](microsoftdns-domain.md) o alle classi [**\_ ResourceRecord di MicrosoftDNS**](microsoftdns-resourcerecord.md) .

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Members

La classe della **\_ cache MicrosoftDNS** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La classe della **\_ cache MicrosoftDNS** presenta questi metodi.



| Metodo                   | Descrizione                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| **ClearCache**           | Cancella la cache del server DNS dei record di risorse. <br/> Qualificatori: implementato<br/> |
| **Getdistinguishname** | Recupera il nome distinto per la zona. <br/> Qualificatori: implementato<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dominio MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Metodo ClearCache della \_ classe cache MicrosoftDNS**](microsoftdns-cache-clearcache.md)
</dt> <dt>

[**Metodo getdistinguishname della \_ classe cache MicrosoftDNS**](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





