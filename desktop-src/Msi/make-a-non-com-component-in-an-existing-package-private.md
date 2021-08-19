---
description: Un amministratore può forzare un'applicazione client a utilizzare sempre la stessa copia di un server non COM in un pacchetto esistente&8212; senza influire sulle altre applicazioni \#&8212; specificando una relazione di componenti isolati tra il server e il \# client.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Rendere privato un componente non COM in un pacchetto esistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0082d89ca6e921213bb462d1b858154419bef416ffa263b8b63ca6d98660fe7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945615"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a>Rendere privato un componente non COM in un pacchetto esistente

Un amministratore può forzare un'applicazione client a usare sempre la stessa copia di un server non [](isolated-components.md) COM in un pacchetto esistente, senza influire sulle altre applicazioni, specificando una relazione di componenti isolati tra il server e il client. In questo modo viene installata una copia privata del componente server in un percorso utilizzato esclusivamente dall'applicazione client. L'amministratore deve usare le trasformazioni o uno strumento di creazione di pacchetti per eseguire le operazioni seguenti:

-   Inserire la DLL del server e il .exe client in componenti separati.
-   Immettere un record nella [tabella IsolatedComponent con](isolatedcomponent-table.md) il componente client nella colonna Componente condiviso e l'applicazione \_ client nella colonna Applicazione \_ componente. Includere [l'azione IsolateComponents](isolatecomponents-action.md) nelle tabelle di sequenza.
-   Impostare il bit **msidbComponentAttributesSharedDllRefCount** nel record [della tabella Component](component-table.md) per Component \_ Shared. Il programma di installazione richiede questo riferimento globale nel percorso condiviso per proteggere i file condivisi e la registrazione nei casi in cui è in corso la condivisione con altre tecnologie di installazione.

 

 



