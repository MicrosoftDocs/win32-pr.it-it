---
description: L' <name> elemento specifica il nome della libreria. Questo elemento è obbligatorio e non dispone di attributi o elementi figlio.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Elemento Name (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995176"
---
# <a name="name-element-library-schema"></a>Elemento Name (schema della libreria)

L' <name> elemento specifica il nome della libreria. Questo elemento è obbligatorio e non dispone di attributi o elementi figlio.

## <a name="syntax"></a>Sintassi

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                               | Elementi figlio |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (schema della libreria)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Commenti

Il nome è il nome descrittivo della libreria visualizzato in Esplora risorse. Il nome può essere specificato in un <dllname> <index> formato, come nell'esempio seguente.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elemento libraryDescription (schema della libreria)](schema-librarydescription.md)
</dt> <dt>

[Cerca nello schema di descrizione del connettore](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
