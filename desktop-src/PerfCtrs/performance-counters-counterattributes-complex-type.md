---
description: Definisce un elenco contenente fino a cinque attributi del contatore.
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: Tipo complesso counterAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfcb94b131e1343565d5763ae2ea4d95e53f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967508"
---
# <a name="counterattributes-complex-type"></a>Tipo complesso counterAttributes

Definisce un elenco contenente fino a cinque attributi del contatore.

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento              | Tipo                                                                               | Descrizione                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| **counterAttribute** | [**uomo: counterAttribute**](performance-counters-counterattribute-complex-type.md) | Un attributo del contatore che specifica la modalità di visualizzazione dei dati del contatore in un'applicazione consumer.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




