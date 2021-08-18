---
description: Specifica un alias di ordinamento o un elenco di alias di ordinamento specificando un elemento che contiene una proprietà di ordinamento o un elenco di proprietà di ordinamento.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 087323df682a2f74164c530f18a9c4da8405930304186288a3d84635bb06ab55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970970"
---
# <a name="aliasinfo"></a>aliasInfo

Specifica un alias di ordinamento o un elenco di alias di ordinamento specificando un elemento che contiene una proprietà di ordinamento o un elenco di proprietà di ordinamento. Deve essere presente un solo [elemento aliasInfo]() per ogni [elemento propertyDescription.](./propdesc-schema-propertydescription.md) Per le proprietà che impostano canGroupBy=true, a meno che non venga specificata una proprietà di ordinamento secondaria ( =prop:example), è possibile che si verifichi un comportamento imprevisto quando si modifica l'ordinamento in una vista raggruppata in base alla aliasInfo/@additionalSortByAliases proprietà . In particolare, l'ordine dei gruppi cambierà, mentre l'ordine degli elementi all'interno dei gruppi non cambierà.

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
| [proprietàDescrizione](./propdesc-schema-propertydescription.md) | Nessuno           |



 

## <a name="attributes"></a>Attributi



| Attributo               | Descrizione                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sortByAlias             | Pubblica. facoltativo. Nome canonico della proprietà da utilizzare per l'ordinamento. Questa stringa è di tipo canonical-type.                                            |
| additionalSortByAliases | Pubblica. facoltativo. Elenco delimitato da punto e virgola delle proprietà aggiuntive da utilizzare durante l'ordinamento. Le proprietà vengono applicate all'ordinamento nella sequenza specificata. |



 

 

 
