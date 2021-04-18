---
description: Specifica un alias di ordinamento o un elenco di alias di ordinamento specificando un elemento che contiene una proprietà di ordinamento o un elenco di proprietà di ordinamento.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310130"
---
# <a name="aliasinfo"></a>aliasInfo

Specifica un alias di ordinamento o un elenco di alias di ordinamento specificando un elemento che contiene una proprietà di ordinamento o un elenco di proprietà di ordinamento. Deve essere presente un solo elemento [aliasInfo]() per ogni elemento [PropertyDescription](./propdesc-schema-propertydescription.md) . Per le proprietà che impostano canGroupBy = true, a meno che non sia specificata una proprietà di ordinamento secondaria ( aliasInfo/@additionalSortByAliases = prop: example), l'utente può riscontrare un comportamento imprevisto quando si modifica il tipo di ordinamento in una vista raggruppata in base alla proprietà. In particolare, l'ordine dei gruppi cambierà, ma l'ordine degli elementi all'interno dei gruppi non lo è.

## <a name="syntax"></a>Sintassi


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                   | Elementi figlio |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | nessuno           |



 

## <a name="attributes"></a>Attributi



| Attributo               | Descrizione                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sortByAlias             | Pubblica. facoltativo. Nome canonico della proprietà da utilizzare per l'ordinamento. La stringa è di tipo canonico.                                            |
| additionalSortByAliases | Pubblica. facoltativo. Elenco delimitato da punti e virgola di proprietà aggiuntive da utilizzare durante l'ordinamento. Le proprietà vengono applicate all'ordinamento nella sequenza specificata. |



 

 

 
