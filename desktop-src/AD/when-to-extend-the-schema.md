---
title: Quando estendere lo schema
description: Estendere lo schema solo se nessuna classe di oggetti esistente soddisfa i requisiti dell'applicazione. L'estensione dello schema è un'operazione complessa; le modifiche dello schema vengono replicate in ogni controller di dominio della foresta aziendale. Considerare attentamente questo problema.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Quando estendere l'annuncio dello schema
- ANNUNCIO dello schema, quando estenderlo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297713"
---
# <a name="when-to-extend-the-schema"></a>Quando estendere lo schema

Estendere lo schema solo se nessuna classe di oggetti esistente soddisfa i requisiti dell'applicazione. L'estensione dello schema è un'operazione complessa; le modifiche dello schema vengono replicate in ogni controller di dominio della foresta aziendale. Considerare attentamente questo problema.

Lo schema può essere esteso in tre modi:

-   Derivare una nuova sottoclasse da una classe esistente: la sottoclasse dispone di tutti gli attributi della superclasse e di tutti gli attributi specificati. Derivare da una classe esistente:
    -   Quando la classe esistente richiede attributi aggiuntivi, ma in caso contrario è accettabile.
    -   Quando la possibilità di trasformare gli oggetti esistenti della classe in una nuova classe non è obbligatoria. Non è possibile aggiungere una sottoclasse a un oggetto esistente.
    -   Per utilizzare lo snap-in di gestione directory esistente per gestire gli attributi estesi degli oggetti.
-   Aggiungere gli attributi a una classe esistente e/o aggiungere oggetti padre per la classe. Quando si aggiungono più attributi, eseguire questa operazione in modo strutturato definendo una classe ausiliaria e aggiungendo tale classe ausiliaria alla classe esistente.
-   La modifica di una classe esistente è obbligatoria quando un'applicazione richiede la possibilità di estendere gli oggetti esistenti della classe. Ad esempio, per aggiungere i dati specifici dell'applicazione all'oggetto utente, estendere normalmente l'utente della classe, perché è necessario gestire gli utenti esistenti e non solo gli utenti speciali creati dall'applicazione.
-   Creare una nuova classe con gli attributi obbligatori. Creare una nuova classe; ovvero una classe derivata da "Top" quando nessuna classe esistente soddisfa i requisiti operativi.

Quando si crea una sottoclasse di una classe esistente, qualsiasi elemento dell'interfaccia utente associato alla classe originale non verrà ereditato dalla sottoclasse. Se ad esempio si esegue la sottoclasse di un oggetto utente, le pagine delle proprietà e le voci di menu associate all'utente non vengono ereditate. Per questo motivo, è preferibile estendere un oggetto esistente o creare una classe ausiliaria anziché creare una sottoclasse.

Se si esegue la sottoclasse di una classe esistente o si modifica una classe esistente, sarà necessario estendere strumenti come lo snap-in Active Directory utenti e computer per gestire gli attributi estesi degli oggetti. Per ulteriori informazioni, vedere [estensione dell'interfaccia utente per gli oggetti directory](extending-the-user-interface-for-directory-objects.md).

 

 




