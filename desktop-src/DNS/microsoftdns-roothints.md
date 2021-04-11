---
title: Classe MicrosoftDNS_RootHints
description: La \_ classe MicrosoftDNS RootHints descrive il RootHints archiviato in un file di cache in un server DNS. Questa classe semplifica la visualizzazione dell'indipendenza degli oggetti DNS anziché la rappresentazione di un oggetto reale.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- DNS della classe MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints della classe DNS, descritta
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
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120090"
---
# <a name="microsoftdns_roothints-class"></a>\_Classe MicrosoftDNS RootHints

La classe **MicrosoftDNS \_ RootHints** descrive il RootHints archiviato in un file di cache in un server DNS. Questa classe semplifica la visualizzazione dell'indipendenza degli oggetti DNS anziché la rappresentazione di un oggetto reale.

**MicrosoftDNS \_ RootHints** è un contenitore per i record di risorse archiviati dal server DNS in un file di cache. Ogni istanza della classe **\_ RootHints di MicrosoftDNS** deve essere assegnata esattamente a un server DNS. Può essere associato a più istanze della classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Members

La **classe \_ RootHints di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe \_ RootHints di MicrosoftDNS** dispone di questi metodi.



| Metodo                        | Descrizione                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| **Getdistinguishname**      | Recupera il nome distinto per la zona. <br/> Qualificatori: implementato<br/>   |
| **WriteBackRootHintDatafile** | Scrive RootHints di nuovo nel file di cache DNS. <br/> Qualificatori: implementato<br/> |



 

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

[**Metodo WriteBackRootHintDatafile della classe MicrosoftDNS \_ RootHints**](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[**Metodo getdistinguishname della \_ classe RootHints di MicrosoftDNS**](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





