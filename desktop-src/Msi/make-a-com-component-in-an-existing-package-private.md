---
description: Un amministratore può forzare un'applicazione client COM a utilizzare sempre la stessa copia di un server COM in un pacchetto esistente&\# 8212; senza influire sulle altre applicazioni&\# 8212; specificando una relazione dei componenti isolati tra il server e il client com.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Rendere privato un componente COM in un pacchetto esistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4935d20c5034af81a52c18d35454553b04cfb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316268"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a>Rendere privato un componente COM in un pacchetto esistente

Un amministratore può forzare un'applicazione client COM a utilizzare sempre la stessa copia di un server COM in un pacchetto esistente, senza influire sulle altre applicazioni, specificando una relazione dei [componenti isolati](isolated-components.md) tra il server e il client com. Verrà installata una copia privata del componente server COM in un percorso utilizzato esclusivamente dall'applicazione client. L'amministratore deve utilizzare le trasformazioni o uno strumento di creazione di pacchetti per eseguire le operazioni seguenti:

-   Inserire la DLL del server COM e il client exe in componenti distinti.
-   Immettere un record nella [tabella IsolatedComponent](isolatedcomponent-table.md) con il componente COM-client nella \_ colonna Shared Component e l'applicazione client nella \_ colonna applicazione componente. Includere l' [azione IsolateComponents](isolatecomponents-action.md) nelle tabelle di sequenza.
-   Impostare il bit **msidbComponentAttributesSharedDllRefCount** nel record della [tabella dei componenti](component-table.md) per il componente \_ condiviso. Il programma di installazione richiede questo refcount globale sul percorso condiviso per proteggere i file condivisi e la registrazione nei casi in cui vi sia una condivisione con altre tecnologie di installazione.

 

 



