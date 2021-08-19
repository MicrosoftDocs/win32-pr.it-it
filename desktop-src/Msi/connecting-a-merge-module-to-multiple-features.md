---
description: Il Connessione dell'oggetto merge può essere usato per connettere un modulo a una funzionalità aggiuntiva che è stata unita nel database o che verrà unita nel database. La funzionalità deve esistere prima di chiamare questo metodo.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Connessione di un modulo unione a più funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12044ff293d825c160533907d625a2d12bb9ea217233c54dd9d5a0099990ee3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948422"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a>Connessione di un modulo unione a più funzionalità

Il [**Connessione**](merge-connect.md) dell'oggetto [](merge-object.md) merge può essere usato per connettere un modulo a una funzionalità aggiuntiva che è stata unita nel database o che verrà unita nel database. La funzionalità deve esistere prima di chiamare questo metodo.

Un modulo unione non deve mai recapitare un componente contenente file di sistema alla funzionalità principale di un'applicazione, perché ciò potrebbe causare la convalida e il ripristino dell'applicazione da parte del programma di installazione ogni volta che viene usato il file di sistema. È necessario creare un file di .msi destinato ad accettare componenti di un modulo unione in modo che tutti i componenti che contengono file di sistema appartengano solo a funzionalità separate dalla funzionalità principale dell'applicazione.

Se il pacchetto usa un modulo unione contenente file di sistema che collegano tutti i componenti del modulo di merge alla funzionalità principale dell'applicazione, un tentativo di usare il file di sistema può attivare il programma di installazione per provare a ripristinare la funzionalità principale dell'applicazione. Se non è possibile ripristinare la funzionalità principale, l'installazione potrebbe non riuscire.

 

 



