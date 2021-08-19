---
description: Il sistema operativo Microsoft Windows fornisce il supporto per un'ampia gamma di dispositivi hardware e protocolli di ora di rete che usano l'architettura del provider di tempo.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Provider di tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f2073e94bdf893793b4ae1df2974226aa197de4ff429be9ce8f2a2e4b5f597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957905"
---
# <a name="time-provider"></a>Provider di tempo

Il sistema operativo Microsoft Windows fornisce il supporto per un'ampia gamma di dispositivi hardware e protocolli di ora di rete che usano *l'architettura del provider di* tempo. I provider di ora di input recuperano timestamp accurati dall'hardware o dalla rete e i provider di ora di output forniscono timestamp ad altri client nella rete.

I provider di tempo sono gestiti dal *gestore del provider di tempo*. È responsabile del caricamento, dell'avvio e dell'arresto dei provider di tempo come indicato dal gestore di controllo del servizio. Questa interfaccia semplifica la scrittura di un provider di tempo rispetto alla scrittura di un servizio completo.

-   [Creazione di un provider di tempo](creating-a-time-provider.md)
-   [Registrazione di un provider di tempo](registering-a-time-provider.md)
-   [Provider di tempo di esempio](sample-time-provider.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio Ora di Windows](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



