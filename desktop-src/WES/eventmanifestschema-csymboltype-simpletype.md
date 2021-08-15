---
title: Tipo semplice CSymbolType (Windows eventi)
description: 'Tipo semplice CSymbolType (Windows eventi): definisce un nome di simbolo C/C++ valido.'
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- EventLog di tipo semplice CSymbolType
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e51438a49a45c167b247882f0976b27a4ad8d4da048437f385ccff545663b4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589894"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>Tipo semplice CSymbolType (Windows eventi)

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

    Il nome del simbolo può essere vuoto o contenere caratteri alfanumerici e caratteri di sottolineatura. Se il nome è vuoto, il compilatore di messaggi genererà il nome del simbolo. Se si specifica un nome, il nome deve iniziare con un carattere di sottolineatura ( \_ ) o un carattere alfabetico.

## <a name="remarks"></a>Commenti

Se il nome del simbolo è vuoto, il compilatore di messaggi usa l'attributo **name** dell'elemento che si sta definendo per generare il nome del simbolo. Il compilatore sostituisce tutti i caratteri non alfanumerici e le cifre iniziali con caratteri di sottolineatura. Ad esempio, se l'attributo **name** del canale è Microsoft-Windows-SampleProvider/Operational, il compilatore userà Microsoft Windows SampleProvider Operational come nome \_ del \_ \_ simbolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

 





