---
description: Definisce un nome di simbolo C/C++ valido.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Tipo semplice CSymbolType (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 418b5119046a89d93814ed8ac8bd427dc554bf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967506"
---
# <a name="csymboltype-simple-type-performance-counters"></a>Tipo semplice CSymbolType (contatori delle prestazioni)

Definisce un nome di simbolo C/C++ valido.

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il tipo semplice **CSymbolType** è **xs: String** limitato dal modello seguente:

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    Il nome del simbolo può essere vuoto o contenere caratteri alfanumerici e caratteri di sottolineatura. Se si specifica un nome, il nome deve iniziare con un carattere di sottolineatura ( \_ ) o un carattere alfabetico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




