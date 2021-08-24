---
description: 'Tipo semplice CSymbolType (contatori delle prestazioni): definisce un nome di simbolo C/C++ valido.'
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Tipo semplice CSymbolType (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4ebba4d72b7bc79f2aaefccfa2d71e57abd82aa06efb09abc2e83cebdb513f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033531"
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

Il **tipo semplice CSymbolType** è **un tipo xs:string** limitato dal modello seguente:

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    Il nome del simbolo può essere vuoto o contenere caratteri alfanumerici e caratteri di sottolineatura. Se si specifica un nome, il nome deve iniziare con un carattere di sottolineatura ( \_ ) o un carattere alfabetico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




