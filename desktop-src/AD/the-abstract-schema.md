---
title: Schema astratto
description: Il contenitore dello schema contiene tutti gli oggetti classSchema e attributeSchema che definiscono le classi e gli attributi che possono esistere in una foresta di directory.
ms.assetid: 688fccf7-37ce-4eea-b4ff-b0b3223a964e
ms.tgt_platform: multiple
keywords:
- Schema astratto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b46e4fefd52e786829e051a14714d2fec118b2ad42cdd95afcaa78b098b0f04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182782"
---
# <a name="the-abstract-schema"></a>Schema astratto

Il contenitore dello schema contiene tutti gli **oggetti classSchema** e **attributeSchema** che definiscono le classi e gli attributi che possono esistere in una foresta di directory. Il contenitore dello schema contiene anche un oggetto denominato Aggregate della **classe subSchema**. Questo **oggetto subSchema** è noto come schema astratto.

Lo schema astratto contiene un subset dei dati archiviati negli **oggetti classSchema** **e attributeSchema.** Il suo scopo è fornire un meccanismo semplice ed efficiente per il recupero degli elementi usati di frequente delle definizioni di classe e attributo. Ad esempio, per recuperare gli attributi facoltativi e obbligatori di una classe di oggetti, eseguire l'associazione a più oggetti per raccogliere i valori **mayContain**, **mustContain**, **systemMayContain** e **systemMustContain** dalla classe e da tutte le relative superclassi, nonché da qualsiasi classe ausiliaria della classe e delle relative superclassi. Lo schema astratto raccoglie facilmente tutti questi dati in un singolo oggetto.

Come con qualsiasi oggetto in Active Directory Domain Services, è possibile eseguire l'associazione all'oggetto **subSchema** e leggerne gli attributi, analizzando i valori stringa per recuperare i dati desiderati. Tuttavia, ADSI fornisce un set di interfacce che semplificano gran parte della lettura dello schema astratto. Per altre informazioni, vedere [Lettura dello schema astratto.](reading-the-abstract-schema.md)

Nella tabella seguente sono elencati gli attributi chiave di **un oggetto subSchema.**



| Attributo                 | Descrizione                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **attributeTypes**        | Attributo multivalore che contiene stringhe che rappresentano ogni attributo nello schema. Ogni valore contiene **attributeID**, **lDAPDisplayName**, **attributeSyntax**, **rangeLower**, **rangeUpper** e un elemento che indica se l'attributo può avere più valori. |
| **extendedAttributeInfo** | Attributo multivalore che contiene stringhe che rappresentano dati aggiuntivi per ogni attributo. Ogni valore contiene **gli attributi attributeID**, **lDAPDisplayName**, **schemaIDGUID** e **attributeSecurityGUID**.                                                                          |
| **extendedClassInfo**     | Attributo multivalore che contiene stringhe che rappresentano dati aggiuntivi per ogni classe. Ogni valore contiene **i valori governsID**, **lDAPDisplayName** e **schemaIDGUID** della classe .                                                                                              |
| **objectClasses**         | Attributo multivalore che contiene stringhe che rappresentano ogni classe nello schema. Ogni valore contiene **governsID**, **lDAPDisplayName**, **mustContain**, **mayContain** e così via.                                                                                           |



 

 

 




