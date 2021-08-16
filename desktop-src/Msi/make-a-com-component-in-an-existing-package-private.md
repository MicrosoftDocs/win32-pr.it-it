---
description: Un amministratore può forzare un'applicazione client COM a usare sempre la stessa copia di un server COM in un pacchetto esistente&8212; senza influire sulle altre applicazioni \#&8212; specificando una relazione di componenti isolati tra il server COM e \# il client.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Rendere privato un componente COM in un pacchetto esistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5119e2d9417f51bb815fe9c76cd47be496e4c03cab81e4e0ccd2b7c49c7b8b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629032"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a>Rendere privato un componente COM in un pacchetto esistente

Un amministratore può forzare un'applicazione client COM a usare sempre la stessa copia di un server [](isolated-components.md) COM in un pacchetto esistente, senza influire sulle altre applicazioni, specificando una relazione di componenti isolati tra il server COM e il client. Verrà installata una copia privata del componente server COM in un percorso utilizzato esclusivamente dall'applicazione client. L'amministratore deve usare le trasformazioni o uno strumento di creazione di pacchetti per eseguire le operazioni seguenti:

-   Inserire la DLL del server COM e .exe client in componenti separati.
-   Immettere un record nella [tabella IsolatedComponent](isolatedcomponent-table.md) con il componente com-client nella colonna Component Shared e l'applicazione \_ client nella colonna Applicazione \_ componente. Includere [l'azione IsolateComponents](isolatecomponents-action.md) nelle tabelle di sequenza.
-   Impostare il bit **msidbComponentAttributesSharedDllRefCount** nel record [della tabella Component](component-table.md) per Component \_ Shared. Il programma di installazione richiede questo riferimento globale nel percorso condiviso per proteggere i file condivisi e la registrazione nei casi in cui è in corso la condivisione con altre tecnologie di installazione.

 

 



