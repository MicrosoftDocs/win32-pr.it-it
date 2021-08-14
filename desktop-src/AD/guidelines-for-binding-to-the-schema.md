---
title: Linee guida per l'associazione allo schema
description: Esistono due modi per eseguire l'associazione allo schema di Active Directory Bind direttamente al contenitore dello schema o a un oggetto classSchema o attributeSchema nel contenitore dello schema.
ms.assetid: 8c10415e-136c-476c-993c-b6dc459b5bf4
ms.tgt_platform: multiple
keywords:
- Linee guida per l'associazione allo schema AD
- Schema AD , binding a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1492814bbce4b359a16c10f1d92340ae06d0f3c58177cd125a0b0c861f32f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188685"
---
# <a name="guidelines-for-binding-to-the-schema"></a>Linee guida per l'associazione allo schema

Esistono due modi per eseguire l'associazione allo schema di Active Directory:

-   Eseguire l'associazione direttamente al contenitore dello schema o a **un oggetto classSchema** o **attributeSchema** nel contenitore dello schema. Gli **oggetti classSchema** **o attributeSchema** contengono definizioni formali complete di ogni classe e attributo che può esistere in una Dominio di Active Directory foresta. Per altre informazioni, vedere [Lettura di oggetti attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).
-   Eseguire l'associazione allo schema astratto o a una voce di classe o attributo nello schema astratto. Lo schema astratto contiene solo un subset dei dati relativi a ogni classe e attributo, ma i dati sono in un formato facile da recuperare e usare. Per altre informazioni, vedere [Schema astratto e](the-abstract-schema.md) [Lettura dello schema astratto.](reading-the-abstract-schema.md)

Per modificare o estendere lo schema, eseguire l'associazione direttamente al contenitore dello schema. Per leggere le definizioni di classi e attributi, è in genere più semplice leggere dallo schema astratto.

È più facile leggere dallo schema astratto per i motivi seguenti:

-   ADSI fornisce tecniche di associazione speciali e un set di interfacce per leggere lo schema astratto.
-   Le interfacce ADSI che usano lo schema astratto restituiscono dati in un formato appropriato per l'uso in altre interfacce ADSI. Ad esempio, [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) e [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) usano in genere stringhe **lDAPDisplayName** per segnalare i nomi di attributi e classi, anche se questi dati vengono archiviati nella directory sotto forma di identificatori di oggetto (OID). Il **formato lDAPDisplayName** è utile perché viene utilizzato da altre interfacce ADSI per fare riferimento a classi e attributi nei filtri di ricerca e altrove.
-   La voce dello schema astratto per una classe di oggetti contiene i dati raccolti da **più oggetti classSchema.** Ad esempio, i possibili elementi padre, gli attributi obbligatori e gli attributi facoltativi per una classe oggetto sono l'unione di questi attributi dalle superclassi e dalle classi ausiliarie della classe. Se si legge dal contenitore dello schema effettivo, è necessario raccogliere dati dai vari oggetti **classSchema** da cui è stata derivata la classe. Se si legge dallo schema astratto, i dati si trova in un'unica posizione.

È consigliabile eseguire l'associazione direttamente al contenitore dello schema anziché usare lo schema astratto nei casi seguenti:

-   Per ottenere attributi specifici non esposti nello schema astratto. Ad esempio, **oMSyntax**, **attributeSchema**, **defaultSecurityDescriptor** e altri attributi non sono esposti nello schema astratto.
-   Per eseguire una query **per gli** oggetti **attributeSchema e classSchema.** Per cercare classi o attributi che corrispondono a un filtro specificato, eseguire l'associazione al contenitore dello schema ed eseguire una ricerca a un livello.
-   Per aggiungere o modificare attributi o classi. Lo schema astratto è di sola lettura. non è possibile usarlo per modificare o estendere lo schema. Tenere presente che è necessario apportare modifiche al controller di dominio che rappresenta il master schema. Per altre informazioni, vedere [Prerequisiti per l'installazione di un'estensione dello schema.](prerequisites-for-installing-a-schema-extension.md)

 

 