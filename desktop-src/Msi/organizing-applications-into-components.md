---
description: Windows Il programma di installazione installa e rimuove un'applicazione o un prodotto in parti denominate componenti.
ms.assetid: 949d8b8c-8f1a-4fde-9a7d-824d33436e62
title: Organizzazione delle applicazioni in componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1398bbbacbdb15df148576ebf0904f7aec98354a4d417681a81f2195535f08d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129191"
---
# <a name="organizing-applications-into-components"></a>Organizzazione delle applicazioni in componenti

Windows Il programma di installazione installa e rimuove un'applicazione o un prodotto in parti denominate [componenti](windows-installer-components.md)di . I componenti sono raccolte di risorse che vengono sempre installate o rimosse come unità dal sistema di un utente. Una risorsa può essere un file, una chiave del Registro di sistema, un collegamento o qualsiasi altro elemento che può essere installato. A ogni componente viene assegnato un GUID di codice componente [univoco.](guid.md)

Gli autori dei pacchetti di installazione devono creare solo componenti, e versioni dei componenti, che possono essere installati e rimossi senza danneggiare altri componenti. Inoltre, la rimozione di un componente non deve lasciare alcuna risorsa orfana nel computer dell'utente, ad esempio file inutilizzati, chiavi del Registro di sistema o collegamenti. A tale scopo, gli autori devono rispettare le regole generali seguenti quando si organizzano le risorse in componenti:

-   Non creare mai due componenti che installano una risorsa con lo stesso nome e lo stesso percorso di destinazione. Se una risorsa deve essere duplicata in più componenti, modificarne il nome o il percorso di destinazione in ogni componente. Questa regola deve essere applicata ad applicazioni, prodotti, versioni dei prodotti e aziende.
-   Si noti che la regola precedente indica che due componenti non devono avere lo stesso file di percorso della chiave. Il valore del percorso della chiave punta a un particolare file o cartella appartenente al componente utilizzato dal programma di installazione per rilevare il componente. Se due componenti hanno lo stesso file di percorso della chiave, il programma di installazione non sarà in grado di distinguere quale componente è installato. Due componenti possono tuttavia condividere una cartella del percorso della chiave.
-   Non creare una versione di un componente incompatibile con tutte le versioni precedenti del componente. Il componente può essere condiviso da altre applicazioni, prodotti, versioni dei prodotti e società. Creare invece un nuovo componente.
-   Non creare componenti contenenti risorse che dovranno essere installate in più directory nel sistema dell'utente. Il programma di installazione installa tutte le risorse di un componente nella stessa directory. Non è possibile installare alcune risorse nelle sottodirectory.
-   Non includere più di un server COM per componente. Se un componente contiene un server COM, questo deve essere il percorso della chiave per il componente.
-   Non specificare più di un file per componente come destinazione per il menu **Start** o un collegamento sul desktop.

Quando si organizza un'applicazione in componenti, gli autori di pacchetti potrebbero dover aggiungere, rimuovere o modificare le risorse in un'installazione esistente. In questo caso, l'autore deve decidere se fornire le risorse introducendo un nuovo componente o modificando i componenti esistenti e modificandoli in una nuova versione del componente. Poiché è necessario assegnare un codice componente univoco quando viene introdotto un nuovo componente, gli autori devono determinare se le modifiche richiedono la modifica del codice del componente. Per altre informazioni, vedere [Modifica del codice del componente,](changing-the-component-code.md)Cosa accade se le regole del componente vengono interrotte? e Definizione dei componenti del programma di [installazione.](defining-installer-components.md) [](what-happens-if-the-component-rules-are-broken.md)

 

 



