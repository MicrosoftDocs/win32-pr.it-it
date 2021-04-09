---
description: Windows Installer installa e rimuove un'applicazione o un prodotto in parti denominate componenti di.
ms.assetid: 949d8b8c-8f1a-4fde-9a7d-824d33436e62
title: Organizzazione di applicazioni in componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3fc2db794bef2a29025bf7ebc54c65691145ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881041"
---
# <a name="organizing-applications-into-components"></a>Organizzazione di applicazioni in componenti

Windows Installer installa e rimuove un'applicazione o un prodotto in parti denominate [componenti](windows-installer-components.md)di. I componenti sono raccolte di risorse che vengono sempre installate o rimosse come unità dal sistema di un utente. Una risorsa può essere un file, una chiave del registro di sistema, un collegamento o qualsiasi altro elemento che può essere installato. A ogni componente viene assegnato un [GUID](guid.md)del codice componente univoco.

Gli autori dei pacchetti di installazione devono solo creare componenti e versioni di componenti che possono essere installati e rimossi senza danneggiare altri componenti. Inoltre, la rimozione di un componente non dovrebbe rimanere dietro a tutte le risorse orfane nel computer dell'utente, ad esempio file inutilizzati, chiavi del registro di sistema o scelte rapide. Per garantire questo problema, gli autori devono rispettare le regole generali seguenti quando si organizzano le risorse nei componenti:

-   Non creare mai due componenti che installano una risorsa con lo stesso nome e percorso di destinazione. Se una risorsa deve essere duplicata in più componenti, modificarne il nome o il percorso di destinazione in ogni componente. Questa regola deve essere applicata a tutte le applicazioni, i prodotti, le versioni dei prodotti e le società.
-   Si noti che la regola precedente indica che due componenti non devono avere lo stesso file di percorso della chiave. Il valore del percorso della chiave punta a un file o a una cartella particolare appartenente al componente utilizzato dal programma di installazione per rilevare il componente. Se due componenti hanno lo stesso file di percorso della chiave, il programma di installazione non sarà in grado di distinguere il componente installato. Tuttavia, due componenti possono condividere una cartella del percorso della chiave.
-   Non creare una versione di un componente incompatibile con tutte le versioni precedenti del componente. Il componente può essere condiviso da altre applicazioni, prodotti, versioni del prodotto e società. In alternativa, creare un nuovo componente.
-   Non creare componenti contenenti risorse che dovranno essere installate in più di una directory nel sistema dell'utente. Il programma di installazione installa tutte le risorse in un componente nella stessa directory. Non è possibile installare alcune risorse nelle sottodirectory.
-   Non includere più di un server COM per componente. Se un componente contiene un server COM, deve essere il percorso della chiave per il componente.
-   Non specificare più di un file per componente come destinazione per il menu **Start** o un collegamento sul desktop.

Quando si organizza un'applicazione in componenti, è possibile che gli autori di pacchetti debbano aggiungere, rimuovere o modificare le risorse in un'installazione esistente. In questo caso, l'autore deve decidere se fornire le risorse introducendo un nuovo componente o modificando i componenti esistenti e cambiandoli in una nuova versione del componente. Poiché un codice componente univoco deve essere assegnato quando viene introdotto un nuovo componente, gli autori devono determinare se le modifiche richiedono la modifica del codice componente. Per ulteriori informazioni, vedere [modifica del codice del componente](changing-the-component-code.md), [cosa accade se le regole del componente sono interrotte?](what-happens-if-the-component-rules-are-broken.md)e [definizione dei componenti del programma di installazione](defining-installer-components.md).

 

 



