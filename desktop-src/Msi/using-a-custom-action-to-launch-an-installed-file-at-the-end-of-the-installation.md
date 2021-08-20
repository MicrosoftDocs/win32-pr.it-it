---
description: L'esempio seguente illustra come avviare un file HTML al termine di un'installazione.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Uso di un'azione personalizzata per avviare un file installato al termine dell'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108ae06dae331660fe5c4f1ff8740a5fdb7e76f5eab27794fafcd7a4495296ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141480"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a>Uso di un'azione personalizzata per avviare un file installato al termine dell'installazione

L'esempio seguente illustra come avviare un file HTML al termine di un'installazione. Il programma di installazione installa il componente che contiene il file e quindi pubblica un evento di controllo al termine dell'installazione per eseguire un'azione personalizzata che apre il file. Questo approccio può essere usato per avviare un'esercitazione della Guida alla fine della prima installazione di un'applicazione.

L'esempio deve soddisfare le specifiche seguenti.

-   Il programma di installazione esegue l'azione personalizzata solo se [*per*](f-gly.md) installare un'applicazione viene usato il livello completo dell'interfaccia utente.
-   Il programma di installazione esegue l'azione personalizzata solo se il componente che contiene il file HTML è installato per l'esecuzione in locale nel computer.
-   L'azione personalizzata viene eseguita solo alla prima installazione dell'applicazione.
-   L'installazione non ha esito negativo se l'azione personalizzata non riesce.

L'esempio include un componente ipotetico denominato Tutorial che controlla almeno una risorsa, un file denominato tutorial.htm. L'identificatore per questo file nella colonna File della tabella File è Tutorial. Nella discussione seguente si presuppone che siano già state create le risorse richieste da Tutorial e che siano state create tutte le voci necessarie nelle tabelle [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md)e [FeatureComponents](featurecomponents-table.md) per installare questo componente. Per altre informazioni, vedere [An Installation Example](an-installation-example.md).

Negli argomenti seguenti sono contenute informazioni su come creare le azioni personalizzate necessarie e aggiungerle a un pacchetto di installazione di .

-   [Creazione dell'azione personalizzata Di avvio](authoring-the-launch-custom-action.md)
-   [Aggiunta di Launch alle tabelle CustomAction e Binary](adding-launch-to-the-customaction-and-binary-tables.md)
-   [Aggiunta di un evento di controllo alla fine dell'installazione per l'esecuzione dell'avvio](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



