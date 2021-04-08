---
description: Per forzare un'applicazione client COM a utilizzare sempre la stessa copia di un server COM, creare il pacchetto di installazione dell'applicazione per specificare una relazione dei componenti isolati tra il server e il client COM.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Installazione di un componente COM in un percorso privato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879926"
---
# <a name="installing-a-com-component-to-a-private-location"></a>Installazione di un componente COM in un percorso privato

Per forzare un'applicazione client COM a utilizzare sempre la stessa copia di un server COM, creare il pacchetto di installazione dell'applicazione per specificare una relazione dei [componenti isolati](isolated-components.md) tra il server e il client com. Verrà installata una copia privata del componente server COM in un percorso utilizzato esclusivamente dall'applicazione client. Quando si crea il pacchetto, effettuare le operazioni seguenti:

-   Inserire la DLL del server COM e il client exe in componenti distinti.
-   Immettere un record nella [tabella IsolatedComponent](isolatedcomponent-table.md) con il componente COM-client nella \_ colonna Shared Component e l'applicazione client nella \_ colonna applicazione componente. Includere l' [azione IsolateComponents](isolatecomponents-action.md) nelle tabelle di sequenza.
-   Impostare il bit msidbComponentAttributesSharedDllRefCount nel record della [tabella dei componenti](component-table.md) per il componente \_ condiviso. Il programma di installazione richiede questo refcount globale sul percorso condiviso per proteggere i file condivisi e la registrazione nei casi in cui vi sia una condivisione con altre tecnologie di installazione.

 

 



