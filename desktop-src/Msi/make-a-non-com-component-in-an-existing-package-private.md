---
description: Un amministratore può forzare un'applicazione client a utilizzare sempre la stessa copia di un server non COM in un pacchetto esistente&\# 8212; senza influire sulle altre applicazioni&\# 8212; specificando una relazione dei componenti isolati tra il server e il client.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Creare un componente non COM in un pacchetto esistente privato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87a74a4f9fe7c3770100f78dd0fcd154772943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308183"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a>Creare un componente non COM in un pacchetto esistente privato

Un amministratore può forzare un'applicazione client a utilizzare sempre la stessa copia di un server non COM in un pacchetto esistente, senza influire sulle altre applicazioni, specificando una relazione dei [componenti isolati](isolated-components.md) tra il server e il client. Verrà installata una copia privata del componente server in una posizione utilizzata esclusivamente dall'applicazione client. L'amministratore deve utilizzare le trasformazioni o uno strumento di creazione di pacchetti per eseguire le operazioni seguenti:

-   Inserire la DLL del server e il client exe in componenti distinti.
-   Immettere un record nella [tabella IsolatedComponent](isolatedcomponent-table.md) con il componente client nella \_ colonna Shared Component e l'applicazione client nella \_ colonna applicazione componente. Includere l' [azione IsolateComponents](isolatecomponents-action.md) nelle tabelle di sequenza.
-   Impostare il bit **msidbComponentAttributesSharedDllRefCount** nel record della [tabella dei componenti](component-table.md) per il componente \_ condiviso. Il programma di installazione richiede questo refcount globale sul percorso condiviso per proteggere i file condivisi e la registrazione nei casi in cui vi sia una condivisione con altre tecnologie di installazione.

 

 



