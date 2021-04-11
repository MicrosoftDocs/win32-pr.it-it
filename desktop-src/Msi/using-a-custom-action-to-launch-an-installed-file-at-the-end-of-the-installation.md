---
description: Nell'esempio seguente viene illustrato come avviare un file HTML al termine di un'installazione.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Uso di un'azione personalizzata per avviare un file installato al termine dell'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232435"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a>Uso di un'azione personalizzata per avviare un file installato al termine dell'installazione

Nell'esempio seguente viene illustrato come avviare un file HTML al termine di un'installazione. Il programma di installazione installa il componente che contiene il file e quindi pubblica un evento di controllo alla fine dell'installazione per eseguire un'azione personalizzata che apre il file. Questo approccio può essere usato per avviare un'esercitazione della Guida alla fine della prima installazione di un'applicazione.

L'esempio deve soddisfare le specifiche seguenti.

-   Il programma di installazione esegue l'azione personalizzata solo se viene usato il livello di [*interfaccia utente completo*](f-gly.md) per installare un'applicazione.
-   Il programma di installazione esegue l'azione personalizzata solo se il componente che contiene il file HTML è installato per l'esecuzione locale nel computer.
-   L'azione personalizzata viene eseguita solo alla prima installazione dell'applicazione.
-   Se l'azione personalizzata ha esito negativo, l'installazione non riesce.

Nell'esempio è incluso un ipotetico componente denominato tutorial che controlla almeno una risorsa, un file denominato tutorial.htm. L'identificatore per questo file nella colonna file della tabella file è tutorial. Nella discussione seguente si presuppone che siano già state create le risorse necessarie per l'esercitazione e che siano state apportate tutte le voci necessarie nelle tabelle [feature](feature-table.md), [Component](component-table.md), [file](file-table.md), [directory](directory-table.md)e [FeatureComponents](featurecomponents-table.md) per installare questo componente. Per ulteriori informazioni, vedere [un esempio di installazione](an-installation-example.md).

Negli argomenti seguenti sono contenute informazioni su come creare azioni personalizzate obbligatorie e aggiungerle a un pacchetto di installazione.

-   [Creazione dell'azione personalizzata di avvio](authoring-the-launch-custom-action.md)
-   [Aggiunta dell'avvio alle tabelle CustomAction e binarie](adding-launch-to-the-customaction-and-binary-tables.md)
-   [Aggiunta di un evento di controllo alla fine dell'installazione per l'esecuzione dell'avvio](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



