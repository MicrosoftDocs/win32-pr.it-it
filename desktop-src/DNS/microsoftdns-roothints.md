---
title: MicrosoftDNS_RootHints classe
description: La classe MicrosoftDNS \_ RootHints descrive i RootHints archiviati in un file di cache in un server DNS. Questa classe semplifica la visualizzazione del contenimento degli oggetti DNS, anziché rappresentare un oggetto reale.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- MicrosoftDNS_RootHints DNS della classe
- MicrosoftDNS_RootHints classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050da9acb1d3865fb490035b6de57fcc1279a45b6f9d78c57df305993d590c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913001"
---
# <a name="microsoftdns_roothints-class"></a>Classe MicrosoftDNS \_ RootHints

La **classe MicrosoftDNS \_ RootHints** descrive i RootHints archiviati in un file di cache in un server DNS. Questa classe semplifica la visualizzazione del contenimento degli oggetti DNS, anziché rappresentare un oggetto reale.

**MicrosoftDNS \_ RootHints è** un contenitore per i record di risorse archiviati dal server DNS in un file di cache. Ogni istanza della **classe MicrosoftDNS \_ RootHints** deve essere assegnata esattamente a un server DNS. Può essere associato a più istanze della [**classe \_ ResourceRecord MicrosoftDNS.**](microsoftdns-resourcerecord.md)

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Members

La **classe MicrosoftDNS \_ RootHints** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe MicrosoftDNS \_ RootHints** include questi metodi.



| Metodo                        | Descrizione                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| **GetDistinguishedName**      | Recupera il nome distinto per la zona. <br/> Qualificatori: implementati<br/>   |
| **WriteBackRootHintDatafile** | Scrive di nuovo RootHints nel file di cache DNS. <br/> Qualificatori: implementati<br/> |



 

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

[**Metodo WriteBackRootHintDatafile della classe \_ MicrosoftDNS RootHints**](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[**Metodo GetDistinguishedName della classe \_ MicrosoftDNS RootHints**](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





