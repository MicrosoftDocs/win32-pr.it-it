---
title: Restrizioni sull'estensione dello schema
description: Per ridurre la possibilità di modifiche dello schema da parte di un'applicazione che suddivide altre applicazioni e per mantenere la coerenza dello schema, Active Directory Domain Services applicare restrizioni sul tipo di modifiche dello schema che possono essere apportate da un'applicazione o da un utente.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707567"
---
# <a name="restrictions-on-schema-extension"></a>Restrizioni sull'estensione dello schema

Per ridurre la possibilità di modifiche dello schema da parte di un'applicazione che suddivide altre applicazioni e per mantenere la coerenza dello schema, Active Directory Domain Services applicare restrizioni sul tipo di modifiche dello schema che possono essere apportate da un'applicazione o da un utente.

Le restrizioni vengono imposte solo sulla modifica degli oggetti dello schema esistenti. Lo schema è suddiviso in due categorie. Gli oggetti dello schema forniti con Windows 2000 nello schema di base appartengono alla categoria 1. Tutti gli oggetti dello schema aggiunti in seguito da altre applicazioni o utenti tramite estensione dello schema dinamico appartengono alla categoria 2. La categoria di un oggetto dello schema può essere determinata dal bit 0x10 impostato nell'attributo **systemFlags** dell'oggetto **classSchema** . Questo bit viene impostato solo sugli oggetti di categoria 1 e non può essere modificato, né può essere impostato su qualsiasi oggetto di categoria 2.

L'attributo **systemFlags** viene utilizzato internamente da Active Directory Domain Services per identificare le caratteristiche speciali degli oggetti "Infrastructure" nello schema di base. Oltre a identificare gli oggetti di categoria 1, **systemFlags** controlla se un oggetto può essere spostato, eliminato o rinominato. Queste operazioni sono evitate per gli oggetti da cui dipende Windows 2000 per l'esecuzione.

Per tutti gli oggetti dello schema, categoria 1 o 2, Active Directory Domain Services impone le restrizioni seguenti:

-   Non è possibile aggiungere un nuovo **mustContain** a una classe (direttamente o tramite ereditarietà mediante l'aggiunta di una classe ausiliaria).
-   Non è possibile eliminare **mustContain** della classe (direttamente o tramite ereditarietà).

Per gli oggetti dello schema di categoria 1 vengono inoltre applicate le restrizioni aggiuntive seguenti:

-   Non è possibile modificare gli attributi seguenti di un attributo di categoria 1:

    -   **RangeLower** e **rangeUpper** (intervallo di valori).
    -   **attributeSecurityGuid** (determina il set di proprietà a cui appartiene l'attributo, se presente).

-   Non è possibile modificare il **defaultObjectCategory** di una classe di categoria 1.
-   Non è possibile modificare il **objectCategory** di un'istanza di una classe di categoria 1.
-   Non è possibile rendere inattivo una classe o un attributo di categoria 1.
-   Non è possibile modificare il **ldapDisplayName** di una classe o di un attributo di categoria 1.
-   Non è possibile rinominare una classe o un attributo di categoria 1.

 

 




