---
description: L' <version> elemento specifica la versione del contenuto della libreria. Questo elemento non ha attributi e nessun elemento figlio.
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: Elemento Version (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7b16a6078a16f4ebbe5e995503114996572f1b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977847"
---
# <a name="version-element-library-schema"></a>Elemento Version (schema della libreria)

L' <version> elemento specifica la versione del contenuto della libreria. Questo elemento non ha attributi e nessun elemento figlio.

## <a name="syntax"></a>Sintassi

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                               | Elementi figlio |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (schema della libreria)](schema-librarydescription.md) | nessuno           |



 

## <a name="remarks"></a>Osservazioni

La versione del contenuto della libreria è diversa dalla versione del formato di file della libreria ( \* libreria-MS). La versione del formato di file della libreria è specificata nello [spazio dei nomi](library-schema-entry.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Schema Descrizione libreria](library-schema-entry.md)
</dt> <dt>

[Cerca nello schema di descrizione del connettore](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
