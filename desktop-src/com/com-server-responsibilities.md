---
title: Responsabilità server COM
description: Responsabilità server COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399772"
---
# <a name="com-server-responsibilities"></a>Responsabilità server COM

Uno dei modi più importanti per ottenere un puntatore a un oggetto da parte del client è che il client chieda che un server venga avviato e che sia stata creata e attivata un'istanza dell'oggetto fornito dal server. Il server è responsabile della verifica del corretto funzionamento. A questo punto sono disponibili diverse parti importanti.

Il server deve implementare il codice per un oggetto classe tramite un'implementazione dell'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) o [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) .

Il server deve registrare il proprio CLSID nel registro di sistema nel computer in cui si trova e ulteriormente, può scegliere di pubblicare il percorso del computer su altri sistemi in una rete per consentire ai client di chiamarlo senza richiedere al client di conoscerne la posizione.

Il server è principalmente responsabile della sicurezza. ovvero, nella maggior parte dei casi, il server determina se fornirà un puntatore a uno dei relativi oggetti a un client.

I server in-process devono implementare ed esportare determinate funzioni che consentono al processo client di crearne un'istanza.

Gli argomenti seguenti illustrano in dettaglio le responsabilità del server COM:

-   [Implementazione di IClassFactory](implementing-iclassfactory.md)
-   [Licenze e IClassFactory2](licensing-and-iclassfactory2.md)
-   [Registrazione di server COM](registering-com-servers.md)
-   [Helper di implementazione del server out-of-process](out-of-process-server-implementation-helpers.md)
-   [Creazione e ottimizzazioni di GUID](guid-creation-and-optimizations.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> </dl>

 

 