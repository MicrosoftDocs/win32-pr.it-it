---
description: Per forzare l'utilizzo sempre della stessa copia di un server non COM da parte di un'applicazione client, creare il pacchetto di installazione dell'applicazione in modo da specificare una relazione dei componenti isolati tra il server e il client.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Installazione di un componente non COM in una posizione privata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885522"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a>Installazione di un componente non COM in una posizione privata

Per forzare l'utilizzo sempre della stessa copia di un server non COM da parte di un'applicazione client, creare il pacchetto di installazione dell'applicazione in modo da specificare una relazione dei [componenti isolati](isolated-components.md) tra il server e il client. Verrà installata una copia privata del componente server in una posizione utilizzata esclusivamente dall'applicazione client. Quando si crea il pacchetto, effettuare le operazioni seguenti:

-   Inserire la DLL del server e il client exe in componenti distinti.
-   Immettere un record nella [tabella IsolatedComponent](isolatedcomponent-table.md) con il componente client nella \_ colonna Shared Component e l'applicazione client nella \_ colonna applicazione componente. Includere l' [azione IsolateComponents](isolatecomponents-action.md) nelle tabelle di sequenza.
-   Impostare il bit msidbComponentAttributesSharedDllRefCount nel record della [tabella dei componenti](component-table.md) per il componente \_ condiviso. Il programma di installazione richiede questo refcount globale sul percorso condiviso per proteggere i file condivisi e la registrazione nei casi in cui vi sia una condivisione con altre tecnologie di installazione.
-   Evitare di creare un percorso registrato condiviso tra i componenti.

 

 



