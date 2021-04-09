---
description: Definisce il tipo che definisce i valori validi per l'attributo Type dell'elemento Content \[ Journal Reader \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Tipo semplice ContentTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050170"
---
# <a name="contenttypetype-simple-type"></a>Tipo semplice ContentTypeType

Definisce il tipo che definisce i valori validi per l'attributo *Type* dell' [elemento Content \[ Journal Reader \]](content-element--journal-reader.md).

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il tipo semplice **ContentTypeType** è una stringa limitata dal modello seguente:

-   `Normal|Inert`

## <a name="remarks"></a>Commenti

I valori validi sono "Normal" e "inerti".

Se il tipo è "inerte", il contenuto contenuto è una pagina journal che rappresenta lo "sfondo" di sola lettura o non modificabile per il documento. Questo errore si verifica quando viene creato un documento utilizzando il driver della stampante Journal note writer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



 

 




