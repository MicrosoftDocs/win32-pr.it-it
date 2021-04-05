---
title: Definizione di una nuova classe
description: Quando si definisce una nuova classe, specificare le classi padre legali della nuova classe, ovvero le classi che possono contenere istanze della nuova classe.
ms.assetid: 24e346b3-2de2-41f9-a0a2-7b7d8ab5668b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d6c0ede945c39a00111cd43ece8257031b3aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955156"
---
# <a name="defining-a-new-class"></a>Definizione di una nuova classe

Quando si definisce una nuova classe, specificare le classi padre legali della nuova classe, ovvero le classi che possono contenere istanze della nuova classe. Le classi padre legali sono specificate negli attributi **possSuperiors** e **systemPossSuperiors** della nuova classe, oltre che nei possibili elementi superiori ereditati dalle sue superclassi, ma non da classi ausiliarie.

Essere specifici quando si definiscono le classi padre valide per la nuova classe. Decidere dove si vuole che gli utenti creino istanze della classe. Se ad esempio si specifica "container" come elemento padre valido, l'utente creerà le istanze in uno qualsiasi dei contenitori standard (**container**, **OrganizationalUnit** e così via), mentre se si specifica "computer" si Abilita la creazione di istanze solo in istanze dell'oggetto **computer** .

**Per creare una classe**

1.  Scegliere un nome per la classe. Per ulteriori informazioni sulla composizione di un nome comune e di un nome visualizzato LDAP per una nuova classe, vedere [Naming Attributes and](naming-attributes-and-classes.md)Classes.
2.  Ottenere un identificatore di oggetto (OID) per la classe. Per ulteriori informazioni, vedere [ottenere un identificatore di oggetto](obtaining-an-object-identifier.md).
3.  Scegliere una "categoria di oggetti predefinita" per la classe. Per altre informazioni, vedere [classe di oggetti e categoria di oggetti](object-class-and-object-category.md).
4.  Scegliere una "categoria classe oggetti" per la classe. Indica se la classe è astratta, strutturale o ausiliaria. Per altre informazioni, vedere [classi strutturali, astratte e ausiliarie](structural-abstract-and-auxiliary-classes.md).
5.  Creare un nuovo oggetto **classSchema** . Molti attributi possono essere impostati per un oggetto **classSchema** . Gli attributi seguenti sono fondamentali per la definizione di una nuova classe:

    -   Classi da cui eredita la nuova classe: **subclassOf**, **auxiliaryClass** e **systemAuxiliaryClass**
    -   Nomi e identificatori per la nuova classe: **CN**, **ldapDisplayName**, **AdminDisplayName**, **schemaIDGUID**, **governsID**
    -   Attributi possibili della nuova classe: **mustContain**, **systemMustContain**, **mayContain**, **systemMayContain**
    -   Possibili elementi padre della nuova classe: **possSuperiors**, **systemPossSuperiors**
    -   **objectClassCategory**
    -   **defaultObjectCategory**
    -   **defaultHidingValue**
    -   **rDnAttId**
    -   **defaultSecurityDescriptor**
    -   **Descrizione** (facoltativa)

    Per ulteriori informazioni e descrizioni di questi attributi, vedere [caratteristiche delle classi di oggetti](characteristics-of-object-classes.md).

    Tenere presente che le classi specificate in **subclassOf**, **possSuperiors**, **systemPossSuperiors**, **auxiliaryClass** e **systemAuxiliaryClass** devono esistere quando la nuova classe viene scritta nella directory; in caso contrario, l'oggetto **classSchema** non verrà aggiunto alla directory. Analogamente, gli attributi specificati in **mustContain**, **systemMustContain**, **mayContain** e **systemMayContain** devono esistere oppure l'operazione di creazione della classe avrà esito negativo.

6.  Scrivere il nuovo oggetto **classSchema** nella directory.

**Per aggiungere un attributo alla proprietà mayContain**

1.  Ottenere l'oggetto **classSchema** per la classe da modificare.
2.  Aggiungere il nuovo attributo alla proprietà multivalore **mayContain** .
3.  Scrivere nuovamente l'oggetto **classSchema** modificato nella directory.

È possibile creare nuovi attributi contemporaneamente alle nuove classi; l'ordine di creazione dei nuovi attributi e classi è importante. Per ulteriori informazioni, vedere [operazioni che devono essere eseguite dall'installazione](what-the-installation-must-do.md).

**Per aggiungere nuovi attributi e nuove classi allo stesso tempo**

1.  Definire prima tutti i nuovi attributi. Per ulteriori informazioni, vedere [definizione di un nuovo attributo](defining-a-new-attribute.md).
2.  Aggiornare la cache dello schema prima di definire le nuove classi. Per ulteriori informazioni, vedere [aggiornamento della cache dello schema](updating-the-schema-cache.md).
3.  Creare le nuove classi.
4.  Aggiungere gli attributi desiderati alle nuove classi.
5.  Aggiornare nuovamente la cache dello schema.

 

 




