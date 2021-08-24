---
title: Implementazione di Component Categories Manager
description: Con l'aumentare del numero di componenti disponibili, diventa sempre più difficile gestire questi componenti. In termini di interfacce che espongono e delle attività che eseguono, molti componenti offrono funzionalità simili.
ms.assetid: c2c67129-bf19-465b-8354-193922aeafaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941ba5f422a4305a3bb6056d1d02648dde3bffc9c9f872fe7f7804ebb90a19ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679212"
---
# <a name="component-categories-manager-implementation"></a>Implementazione di Component Categories Manager

Con l'aumentare del numero di componenti disponibili, diventa sempre più difficile gestire questi componenti. In termini di interfacce che espongono e delle attività che eseguono, molti componenti offrono funzionalità simili.

Spesso è necessario enumerare i componenti che possono essere usati in un determinato contesto. Ad esempio, la **finestra di dialogo** Inserisci oggetto  usata nei documenti composti OLE e la finestra di dialogo Inserisci controllo usata nei controlli OLE. Queste finestre di dialogo elencano tutti i componenti che soddisfano (o pretendono di soddisfare) i contratti di interfaccia per i documenti o i controlli composti. Queste categorie esistenti (documento OLE, controllo OLE) non implicano una firma dell'interfaccia esatta. I documenti OLE devono esporre un determinato set di interfacce di base , ad esempio [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) o [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), ma possono anche esporre interfacce aggiuntive, ad esempio [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink).

In passato, i componenti sono stati contrassegnati aggiungendo un nome leggibile dall'utente ("Inseriscibile", "Controllo" e così via) come sottochiave al **CLSID RADICE HKEY \_ CLASSES \_ \\ \\ {...}** chiave del Registro di sistema corrispondente al componente. Ciò funziona bene per una definizione centrale delle categorie, ma rischia conflitti di nomi quando molte parti indipendenti definiscono nuove categorie. Come in altre aree di COM, la soluzione per fornire uno spazio dei nomi estendibile consiste nell'uso di GUID (Globally Unique Identifier). Invece di usare un nome leggibile, a ogni categoria viene assegnato un numero univoco (CATID).

Un'altra limitazione della categorizzazione esistente è che si limita a esprimere le funzionalità del componente stesso. Molti componenti richiedono determinate funzionalità dai contenitori. Quando un componente di questo tipo viene inserito in un contenitore, l'inserimento può avere esito negativo o comportarsi in modo imprevisto, anche se il componente soddisfa i contratti impliciti da una delle relative categorie. Per enumerare i componenti che possono essere usati correttamente in determinate situazioni, è necessario considerare le funzionalità del componente e del contenitore.

Per queste considerazioni, sono state apportate le modifiche seguenti alla categorizzazione esistente:

-   Le categorie vengono indicate usando CATID che sono identificatori univoci a livello globale.
-   Nella **sottochiave Components** della chiave del Registro di sistema **\_ HKEY CLASSES \_ ROOT \\ CLSID** sono state sviluppate due sottochiavi separate, "Implemented Categories" e "Required Categories". Queste sottochiavi contengono gli elenchi di CATID forniti dal componente o che il contenitore del componente deve fornire.

Per semplificare la gestione delle categorie di componenti, le categorie sono elencate in una posizione centrale nel Registro di sistema: **HKEY \_ CLASSES ROOT \_ Component \\ Categories**. Questa chiave elenca le categorie installate sia con il CATID che con i nomi localizzati e leggibili dall'utente.

Per altre informazioni, vedere i seguenti argomenti:

-   [Categorizzazione in base alle funzionalità dei componenti](categorizing-by-component-capabilities.md)
-   [Categorizzazione in base alle funzionalità del contenitore](categorizing-by-container-capabilities.md)
-   [Gestione categorie componenti](the-component-categories-manager.md)
-   [Classi e associazioni predefinite](default-classes-and-associations.md)
-   [Definizione di categorie di componenti](defining-component-categories.md)
-   [Associazione di icone a una categoria](associating-icons-with-a-category.md)

 

 




