---
description: "&lt;L'elemento name specifica il nome di questa &gt; libreria. Questo elemento è obbligatorio e non dispone di attributi o elementi figlio."
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Elemento name (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d32b6d929a58f19cc2b87a79af846d22fc0ebda
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880857"
---
# <a name="name-element-library-schema"></a>Elemento name (schema della libreria)

&lt;L'elemento name specifica il nome di questa &gt; libreria. Questo elemento è obbligatorio e non dispone di attributi o elementi figlio.

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

Il nome è il nome descrittivo della libreria visualizzato in Windows Explorer. Il nome può essere specificato in un &lt; formato di indice &gt; dllname, come &lt; &gt; nell'esempio seguente.


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

 

 
