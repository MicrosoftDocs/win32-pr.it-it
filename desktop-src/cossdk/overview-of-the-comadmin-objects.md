---
description: Gli oggetti COMAdmin offrono un semplice modello a oggetti che consente di accedere al catalogo COM+.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Panoramica degli oggetti COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad382fcfab6e53a2eb8bfec9914a070d8a78e6ef2a29253005c324c8df8257e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070391"
---
# <a name="overview-of-the-comadmin-objects"></a>Panoramica degli oggetti COMAdmin

Gli oggetti COMAdmin offrono un semplice modello a oggetti che consente di accedere al catalogo COM+. In questo modo, vengono utilizzati per modellare tutte le funzionalità fornite dallo strumento di amministrazione Servizi componenti. Ogni volta che si eserviti qualsiasi tipo di amministrazione COM+, si interagisce con il catalogo COM+. Per una descrizione del catalogo, vedere [Accesso al catalogo COM+.](accessing-the-com--catalog.md)

Le informazioni che si ottengono dallo strumento amministrativo Servizi componenti o tramite gli oggetti COMAdmin sono strutturate in modo analogo e le azioni eseguite in entrambi i contesti sono analoghe. La correlazione di base tra l'utilizzo dello snap-in Servizi componenti e l'amministrazione a livello di codice è che le cartelle nell'albero della console dello snap-in corrispondono alle raccolte nel catalogo COM+. Ciò significa che, proprio come ogni cartella nello snap-in contiene tutti gli elementi di un tipo; Ad esempio, **le applicazioni COM+** contiene applicazioni COM+ installate. Ogni raccolta nel catalogo COM+ contiene elementi di un tipo uniforme. Inoltre, proprio come ogni elemento in una cartella ha proprietà che è possibile impostare in una finestra delle proprietà, ogni elemento di una raccolta espone le proprietà che è possibile impostare.

Per consentire la configurazione di oggetti all'interno di questa struttura, gli oggetti COMAdmin consentono di eseguire le operazioni seguenti:

-   Accedere al catalogo COM+
-   Accedere alle raccolte nel catalogo
-   Accedere agli elementi nelle raccolte
-   Accedere alle proprietà degli elementi nelle raccolte

Per supportare queste azioni, la libreria COMAdmin fornisce le tre classi seguenti:

-   [**COMAdminCatalog**](comadmincatalog.md), che rappresenta il catalogo stesso.
-   [**COMAdminCatalogCollection,**](comadmincatalogcollection.md)che rappresenta qualsiasi raccolta.
-   [**COMAdminCatalogObject**](comadmincatalogobject.md), che rappresenta qualsiasi elemento in una raccolta.

Per descrizioni più complete di queste classi, vedere [Descrizione di riepilogo delle classi COMAdmin](summary-description-of-the-comadmin-classes.md) in questa sezione.

Per avere un'idea rapida delle azioni tipiche eseguite nell'amministrazione a livello di codice, vedere Esempio introduttivo [dell'uso del catalogo di amministrazione COM+.](introductory-example-using-the-com--administration-catalog.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operazioni di amministrazione COM+ all'interno di transazioni](com--administration-operations-within-transactions.md)
</dt> <dt>

[Gestione degli errori di amministrazione COM+](handling-com--administration-errors.md)
</dt> <dt>

[Esempio introduttivo di utilizzo del catalogo di amministrazione COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



