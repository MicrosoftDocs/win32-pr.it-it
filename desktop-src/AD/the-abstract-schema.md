---
title: Schema astratto
description: Il contenitore dello schema contiene tutti gli oggetti classSchema e attributeSchema che definiscono le classi e gli attributi che possono esistere in una foresta di directory.
ms.assetid: 688fccf7-37ce-4eea-b4ff-b0b3223a964e
ms.tgt_platform: multiple
keywords:
- AD abstract schema AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9123c72cc4cc38eafa77e0ad0c6384940667e54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044088"
---
# <a name="the-abstract-schema"></a>Schema astratto

Il contenitore dello schema contiene tutti gli oggetti **classSchema** e **attributeSchema** che definiscono le classi e gli attributi che possono esistere in una foresta di directory. Il contenitore dello schema contiene anche un oggetto denominato aggregate della classe **subschema**. Questo oggetto **sottoschema** è noto come schema astratto.

Lo schema astratto contiene un subset dei dati archiviati negli oggetti **classSchema** e **attributeSchema** . Lo scopo è quello di fornire un meccanismo semplice ed efficiente per recuperare gli elementi utilizzati di frequente della classe e delle definizioni di attributo. Ad esempio, per recuperare gli attributi facoltativi e obbligatori di una classe di oggetti, eseguire l'associazione a più oggetti per raccogliere i valori **mayContain**, **mustContain**, **systemMayContain** e **systemMustContain** dalla classe e tutte le relative superclassi, nonché da qualsiasi classe ausiliaria della classe e delle relative superclassi. Lo schema astratto raccoglie comodamente tutti questi dati in un singolo oggetto.

Come per qualsiasi oggetto in Active Directory Domain Services, è possibile eseguire l'associazione all'oggetto di **sottoschema** e leggere i relativi attributi, analizzando i valori di stringa per recuperare i dati desiderati. Tuttavia, ADSI fornisce un set di interfacce che rendono molto più semplice la lettura dello schema astratto. Per altre informazioni, vedere [Reading the abstract schema](reading-the-abstract-schema.md).

Nella tabella seguente sono elencati gli attributi chiave di un oggetto **sottoschema** .



| Attributo                 | Descrizione                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **attributeTypes**        | Un attributo multivalore contenente stringhe che rappresentano ogni attributo nello schema. Ogni valore contiene **attributeId**, **ldapDisplayName**, **attributeSyntax**, **RangeLower**, **rangeUpper** e un elemento che indica se l'attributo può avere più valori. |
| **extendedAttributeInfo** | Un attributo multivalore contenente stringhe che rappresentano dati aggiuntivi per ogni attributo. Ogni valore contiene **attributeId**, **ldapDisplayName**, **schemaIDGUID** e **attributeSecurityGUID**.                                                                          |
| **extendedClassInfo**     | Un attributo multivalore contenente stringhe che rappresentano dati aggiuntivi per ogni classe. Ogni valore contiene **governsID**, **ldapDisplayName** e **schemaIDGUID** della classe.                                                                                              |
| **objectClasses**         | Un attributo multivalore contenente stringhe che rappresentano ogni classe nello schema. Ogni valore contiene **governsID**, **ldapDisplayName**, **mustContain**, **mayContain** e così via.                                                                                           |



 

 

 




