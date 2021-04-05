---
title: Implementazione di gestione categorie di componenti
description: Man mano che aumenta il numero di componenti disponibili, diventa sempre più difficile gestire questi componenti. Per quanto riguarda le interfacce che espongono e le attività che eseguono, molti componenti offrono funzionalità simili.
ms.assetid: c2c67129-bf19-465b-8354-193922aeafaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2414567beba159c05ea08b3561f0a97ddda1cb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955822"
---
# <a name="component-categories-manager-implementation"></a>Implementazione di gestione categorie di componenti

Man mano che aumenta il numero di componenti disponibili, diventa sempre più difficile gestire questi componenti. Per quanto riguarda le interfacce che espongono e le attività che eseguono, molti componenti offrono funzionalità simili.

Spesso è necessario enumerare i componenti che possono essere usati in un determinato contesto. Alcuni esempi sono la finestra di dialogo **Inserisci oggetto** utilizzata in documenti composti OLE e la finestra di dialogo **Inserisci controllo** utilizzata nei controlli OLE. In queste finestre di dialogo sono elencati tutti i componenti che soddisfano (o attestano per soddisfare) i contratti di interfaccia per i documenti o i controlli composti. Queste categorie esistenti (documento OLE, controllo OLE) non implicano una firma dell'interfaccia esatta. I documenti OLE devono esporre un determinato set di interfacce di base, ad esempio [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) o [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), ma possono anche esporre interfacce aggiuntive, ad esempio [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink).

In passato, i componenti sono stati contrassegnati con l'aggiunta di un nome leggibile ("Insertable", "Control" e così via) come sottochiave al **\_ CLSID radice delle classi HKEY \_ \\ \\ {...}** chiave del registro di sistema corrispondente al componente. Questa funzione è ottimale per una definizione centrale delle categorie ma rischia conflitti di nomi quando molte parti indipendenti definiscono nuove categorie. Come in altre aree di COM, la soluzione per fornire uno spazio dei nomi estendibile consiste nell'utilizzo di identificatori univoci globali (GUID). Invece di usare un nome leggibile, viene assegnato un numero univoco (CATId) a ogni categoria.

Un altro limite con la categorizzazione esistente è che è limitato a esprimere le funzionalità del componente stesso. Molti componenti richiedono determinate funzionalità dai contenitori. Quando un componente di questo tipo viene inserito in un contenitore, l'inserimento può avere esito negativo o comportarsi in modo imprevisto, anche se il componente soddisfa i contratti impliciti in una delle categorie. Per enumerare i componenti che possono essere utilizzati correttamente in determinate situazioni, è necessario considerare le funzionalità del componente e del contenitore.

A causa di queste considerazioni, sono state apportate le modifiche seguenti alla categorizzazione esistente:

-   Le categorie sono indicate usando CATID che sono identificatori univoci globali.
-   Sotto la sottochiave **Components** della chiave del registro di sistema **HKEY delle \_ classi \_ radice \\** , sono state sviluppate due sottochiavi separate, "Categorie implementate" e "categorie obbligatorie". Queste sottochiavi contengono gli elenchi di CATID forniti dal componente o che il contenitore del componente deve fornire.

Per semplificare la gestione delle categorie di componenti, le categorie sono elencate in una posizione centrale nel registro di sistema: **HKEY \_ classi \_ radice dei \\ componenti**. Questa chiave elenca le categorie installate sia con il CATId che con i nomi leggibili localizzati.

Per altre informazioni, vedere i seguenti argomenti:

-   [Categorizzazione in base alle funzionalità del componente](categorizing-by-component-capabilities.md)
-   [Categorizzazione in base alle funzionalità del contenitore](categorizing-by-container-capabilities.md)
-   [Gestione categorie di componenti](the-component-categories-manager.md)
-   [Classi e associazioni predefinite](default-classes-and-associations.md)
-   [Definizione delle categorie di componenti](defining-component-categories.md)
-   [Associazione di icone a una categoria](associating-icons-with-a-category.md)

 

 




