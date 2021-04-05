---
title: Linee guida per l'associazione allo schema
description: Esistono due modi per eseguire l'associazione allo schema Active Directory associare direttamente al contenitore dello schema o a un oggetto classSchema o attributeSchema nel contenitore dello schema.
ms.assetid: 8c10415e-136c-476c-993c-b6dc459b5bf4
ms.tgt_platform: multiple
keywords:
- Linee guida per l'associazione allo schema AD
- AD dello schema, associazione a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf246a4ea1ded5c7d80c52abb8ac9192182b3b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872302"
---
# <a name="guidelines-for-binding-to-the-schema"></a>Linee guida per l'associazione allo schema

Esistono due modi per eseguire l'associazione allo schema Active Directory:

-   Associare direttamente al contenitore dello schema o a un oggetto **classSchema** o **attributeSchema** nel contenitore dello schema. Gli oggetti **classSchema** o **attributeSchema** contengono definizioni formali complete di ogni classe e attributo che possono esistere in una foresta dominio di Active Directory. Per altre informazioni, vedere [lettura degli oggetti attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).
-   Eseguire l'associazione allo schema astratto o a una voce di classe o attributo nello schema astratto. Lo schema astratto contiene solo un subset dei dati relativi a ogni classe e attributo, ma i dati sono in un formato semplice da recuperare e utilizzare. Per ulteriori informazioni, vedere [lo schema astratto](the-abstract-schema.md) e [leggere lo schema astratto](reading-the-abstract-schema.md).

Per modificare o estendere lo schema, effettuare l'associazione direttamente al contenitore dello schema. Per leggere le definizioni delle classi e degli attributi, è in genere più facile leggere dallo schema astratto.

È più facile leggere dallo schema astratto per i motivi seguenti:

-   ADSI fornisce tecniche di associazione speciali e un set di interfacce per la lettura dello schema astratto.
-   Le interfacce ADSI che funzionano con lo schema astratto restituiscono i dati in un formato appropriato per l'utilizzo in altre interfacce ADSI. Ad esempio, [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) e [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) in genere usano stringhe **ldapDisplayName** per segnalare i nomi di attributi e classi, anche se questi dati vengono archiviati nella directory sotto forma di identificatori di oggetto (OID). Il formato **ldapDisplayName** è utile perché altre interfacce ADSI lo usano per fare riferimento alle classi e agli attributi nei filtri di ricerca e altrove.
-   La voce dello schema astratto per una classe di oggetti contiene i dati raccolti da più oggetti **classSchema** . Ad esempio, gli elementi padre, gli attributi obbligatori e gli attributi facoltativi possibili per una classe di oggetti sono l'Unione di questi attributi dalle superclassi della classe e dalle classi ausiliarie. Se si legge dal contenitore dello schema effettivo, è necessario raccogliere i dati dai vari oggetti **classSchema** da cui è stata derivata la classe. Se si legge dallo schema astratto, i dati sono in un'unica posizione.

È necessario eseguire l'associazione direttamente al contenitore dello schema anziché utilizzare lo schema astratto nei casi seguenti:

-   Per ottenere attributi specifici non esposti nello schema astratto. Ad esempio, **oMSyntax**, **attributeSchema**, **defaultSecurityDescriptor** e altri attributi non sono esposti nello schema astratto.
-   Per eseguire una query per gli oggetti **attributeSchema** e **classSchema** . Per cercare le classi o gli attributi che corrispondono a un filtro specificato, associare il contenitore dello schema ed eseguire una ricerca a un solo livello.
-   Per aggiungere o modificare attributi o classi. Lo schema astratto è di sola lettura. non è possibile usarlo per modificare o estendere lo schema. Tenere presente che le modifiche devono essere apportate al controller di dominio che è il master schema. Per ulteriori informazioni, vedere [prerequisiti per l'installazione di un'estensione dello schema](prerequisites-for-installing-a-schema-extension.md).

 

 