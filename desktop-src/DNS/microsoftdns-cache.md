---
title: MicrosoftDNS_Cache classe
description: La classe Cache MicrosoftDNS \_ descrive una cache esistente in un server DNS.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- MicrosoftDNS_Cache DNS della classe
- MicrosoftDNS_Cache classe DNS , descritto
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
ms.openlocfilehash: 03728a82f7668e38e43c92e3edacff1717333c6b073ee3491389723fb63b5f7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077071"
---
# <a name="microsoftdns_cache-class"></a>Classe Cache MicrosoftDNS \_

La **classe \_ Cache MicrosoftDNS** descrive una cache esistente in un server DNS. Questa classe semplifica la visualizzazione del contenimento degli oggetti DNS, anziché rappresentare un oggetto reale. La **classe \_ Cache MicrosoftDNS** è un contenitore per i record di risorse memorizzati nella cache dal server DNS. Non confondere questo problema con un file di cache che contiene hint radice.

Ogni istanza della classe **MicrosoftDNS \_ Cache** deve essere assegnata esattamente a un server DNS. Può essere associato a più istanze delle [**classi MicrosoftDNS \_ Domain o**](microsoftdns-domain.md) [**MicrosoftDNS \_ ResourceRecord.**](microsoftdns-resourcerecord.md)

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Members

La **classe \_ Cache MicrosoftDNS** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe \_ Cache MicrosoftDNS** include questi metodi.



| Metodo                   | Descrizione                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| **Clearcache**           | Cancella la cache del server DNS dei record di risorse. <br/> Qualificatori: implementati<br/> |
| **GetDistinguishedName** | Recupera il nome distinto per la zona. <br/> Qualificatori: implementati<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dominio \_ MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Metodo ClearCache della classe Cache MicrosoftDNS \_**](microsoftdns-cache-clearcache.md)
</dt> <dt>

[**Metodo GetDistinguishedName della classe Cache MicrosoftDNS \_**](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





