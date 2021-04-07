---
title: Uso di Active Directory interfacce del servizio
description: Active Directory Service Interfaces (ADSI) fornisce i mezzi per le applicazioni client dei servizi directory per l'utilizzo di un set di interfacce per comunicare con qualsiasi spazio dei nomi che fornisce un'implementazione ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Uso di ADSI Active Directory interfacce di servizio
- ADSI ADSI, utilizzo
- Interfacce di servizio Active Directory ADSI, utilizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855234"
---
# <a name="using-active-directory-service-interfaces"></a>Uso di Active Directory interfacce del servizio

Active Directory Service Interfaces (ADSI) fornisce i mezzi per le applicazioni client dei servizi directory per l'utilizzo di un set di interfacce per comunicare con qualsiasi spazio dei nomi che fornisce un'implementazione ADSI. I client ADSI utilizzano le interfacce del servizio Active Directory ben definite al posto delle chiamate API specifiche della rete per ottenere un accesso più semplice ai servizi per uno spazio dei nomi.

Active Directory le interfacce del servizio sono conformi al Component Object Model (COM) e supportano le funzionalità COM standard.

ADSI fornisce le interfacce conformi all'automazione per i controller associati al nome, ad esempio Java, Microsoft Visual Basic Development System e Visual Basic Scripting Edition (VBScript). ADSI può inoltre fornire un'interfaccia in grado di ottimizzare le prestazioni per le interfacce non conformi all'automazione, da utilizzare con ambienti di linguaggio come C e C++.

ADSI fornisce anche le interfacce non di automazione, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), per supportare la gestione e le query degli oggetti directory.

Inoltre, ADSI fornisce il proprio provider di OLE DB, in modo che tutti i client che usano già OLE DB, inclusi quelli che usano ActiveX Data Objects, possano eseguire query direttamente nei servizi directory.

Anche le applicazioni Web che utilizzano Active Server pagine possono programmare l'accesso ai servizi directory tramite ADSI.

I client ADSI possono individuare a livello di programmazione tutti i provider ADSI in un sito e utilizzare le stesse interfacce per comunicare con ogni spazio dei nomi. Quando vengono installati provider aggiuntivi, i client ADSI possono comunicare, senza ricompilare, anche con i nuovi spazi dei nomi.

In questa guida di programmazione viene descritto il funzionamento di ADSI e vengono fornite informazioni per l'esecuzione di attività specifiche in ADSI. Vengono trattati i seguenti argomenti:

-   [Associazione a un oggetto ADSI](binding-to-an-adsi-object.md)
-   [Creazione ed eliminazione di oggetti](creating-and-deleting-objects.md)
-   [Accesso e manipolazione di dati con ADSI](accessing-and-manipulating-data-with-adsi.md)
-   [Utilizzo dello schema ADSI](using-the-adsi-schema.md)
-   [Raccolte e gruppi](collections-and-groups.md)
-   [Enumerazione di oggetti ADSI](enumerating-adsi-objects.md)
-   [Ricerca di Active Directory](searching-active-directory.md)
-   [Modello di sicurezza ADSI](adsi-security-model.md)
-   [Estensioni ADSI](adsi-extensions.md)
-   [Uso di ADSI con Exchange](using-adsi-with-exchange.md)
-   [Interfacce di utilità ADSI](adsi-utility-interfaces.md)
-   [Programmazione di ADSI con Java/COM](programming-adsi-with-javacom.md)

 

 




