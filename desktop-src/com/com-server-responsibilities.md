---
title: Responsabilità del server COM
description: Responsabilità del server COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c6604a8f42804867e797087ffb346fe69152cb84440d052560c3f40a42140c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854771"
---
# <a name="com-server-responsibilities"></a>Responsabilità del server COM

Uno dei modi più importanti per ottenere un puntatore a un oggetto da parte di un client è chiedere che un server sia avviato e che un'istanza dell'oggetto fornito dal server sia creata e attivata. È responsabilità del server assicurarsi che ciò avvenga correttamente. Esistono diverse parti importanti a questo scopo.

Il server deve implementare il codice per un oggetto classe tramite un'implementazione [**dell'interfaccia IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) o [**IClassFactory2.**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)

Il server deve registrare il proprio CLSID nel Registro di sistema nel computer in cui risiede e ha la possibilità di pubblicare il percorso del computer in altri sistemi in una rete per consentire ai client di chiamarlo senza richiedere al client di conoscere la posizione del server.

Il server è principalmente responsabile della sicurezza. in altri casi, il server determina se fornirà un puntatore a uno dei relativi oggetti a un client.

I server in-process devono implementare ed esportare determinate funzioni che consentono al processo client di crearne un'istanza.

Gli argomenti seguenti descrivono in dettaglio le responsabilità del server COM:

-   [Implementazione di IClassFactory](implementing-iclassfactory.md)
-   [Licenze e IClassFactory2](licensing-and-iclassfactory2.md)
-   [Registrazione di server COM](registering-com-servers.md)
-   [Helper di implementazione del server out-of-process](out-of-process-server-implementation-helpers.md)
-   [Creazione e ottimizzazioni di GUID](guid-creation-and-optimizations.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> </dl>

 

 