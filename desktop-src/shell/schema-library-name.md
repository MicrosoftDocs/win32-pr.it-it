---
description: <name>L'elemento specifica il nome di questa libreria. Questo elemento è obbligatorio e non ha attributi o elementi figlio.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Elemento name (schema di libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 179d8b4a1f4358ccb441cc38c6c0765a6dc4d9ade8b3c32a1504be2151cfedaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883941"
---
# <a name="name-element-library-schema"></a>Elemento name (schema di libreria)

<name>L'elemento specifica il nome di questa libreria. Questo elemento è obbligatorio e non ha attributi o elementi figlio.

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

Il nome è il nome descrittivo della libreria visualizzato in Windows Explorer. Il nome può essere specificato in un formato <dllname> <index> , come nell'esempio seguente.


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

[Schema di descrizione del connettore di ricerca](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
