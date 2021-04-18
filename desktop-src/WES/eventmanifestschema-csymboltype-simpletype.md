---
title: Tipo semplice CSymbolType (registro eventi di Windows)
description: Definisce un nome di simbolo C/C++ valido.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Log eventi di tipo semplice CSymbolType
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67b0ccb7c573aa4d71c038f9133cea7c95cdfbd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301557"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>Tipo semplice CSymbolType (registro eventi di Windows)

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

    Il nome del simbolo può essere vuoto o contenere caratteri alfanumerici e caratteri di sottolineatura. Se il nome è vuoto, il compilatore del messaggio genererà il nome del simbolo. Se si specifica un nome, il nome deve iniziare con un carattere di sottolineatura ( \_ ) o un carattere alfabetico.

## <a name="remarks"></a>Commenti

Se il nome del simbolo è vuoto, il compilatore di messaggi utilizzerà l'attributo **Name** dell'elemento che si sta definendo per generare il nome del simbolo. Il compilatore sostituisce tutti i caratteri non alfanumerici e le cifre iniziali con caratteri di sottolineatura. Se, ad esempio, l'attributo **Name** del canale è Microsoft-Windows-SampleProvider/Operational, il compilatore utilizzerà Microsoft \_ Windows \_ SampleProvider \_ Operational come nome del simbolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 





