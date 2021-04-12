---
title: Introduzione agli utenti di Windows Media Format SDK
description: Introduzione agli utenti di Windows Media Format SDK
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows Media Format SDK, API client DRM estese
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, API estese
- Windows Media Format SDK, API
- Windows Media Format SDK, Digital Rights Management (DRM)
- Digital Rights Management (DRM), API estese del client
- DRM (Digital Rights Management), API estese client
- Digital Rights Management (DRM), API estese
- DRM (Digital Rights Management), API estese
- Digital Rights Management (DRM), API
- DRM (Digital Rights Management), API
- API estese del client DRM, informazioni
- API estese client, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396074"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a>Introduzione agli utenti di Windows Media Format SDK

Gran parte delle funzionalità fornite dalle API estese del client Windows Media DRM è la stessa della funzionalità fornita dagli oggetti di Windows Media Format SDK. Windows Media Format SDK fornisce agli sviluppatori gli oggetti necessari per creare, accedere e modificare i file multimediali che usano la struttura di file ASF (Advanced Systems Format). Poiché Windows Media DRM è progettato per proteggere i file ASF, la funzionalità DRM sul lato client è stata inclusa in Windows Media Format SDK.

Le API estese del client Windows Media DRM sono state rilasciate insieme alla piattaforma multimediale digitale di prossima generazione Microsoft, il Microsoft Media Foundation SDK. Media Foundation includerà la funzionalità ASF che si sovrappone ad alcune delle funzionalità di Windows Media Format SDK. Poiché ora esistono due SDK Microsoft che modificano i file ASF, la funzionalità DRM sul lato client viene separata da Windows Media Format SDK nelle API estese del client Windows Media DRM. È possibile accedere a queste API dagli utenti di Windows Media Format SDK e di Media Foundation SDK. Al momento, queste API sono incluse come parte del pacchetto di installazione di Windows Media Format SDK e sono documentate come parte di Windows Media Format SDK. Tuttavia, le API estese del client Windows Media DRM sono implementate nella propria libreria e hanno un proprio file di intestazione. Dopo l'installazione di Windows Media Format SDK, queste API possono essere utilizzate una propria, senza includere intestazioni o librerie di Windows Media Format SDK nell'applicazione.

Se si sviluppano applicazioni che utilizzano Windows Media Format SDK, è necessario decidere se utilizzare la funzionalità DRM fornita dall'SDK oppure utilizzare le API estese del client Windows Media DRM. Sebbene molte delle funzionalità di questi due SDK siano molto simili, le API estese del client Windows Media DRM offrono le seguenti funzionalità non disponibili per gli utenti delle routine DRM precedenti:

-   Possibilità di importare contenuti protetti da un sistema di Rights Management di terze parti.
-   Possibilità di esportare contenuti protetti da DRM di Windows Media in un sistema di Rights Management di terze parti.
-   Enumerazione diretta delle licenze nell'archivio licenze.
-   Semplice esecuzione di query sui diritti aggregati in base all'ID chiave (non è necessario caricare il file multimediale).
-   Possibilità di rinnovare i componenti revocati usando l'interfaccia Media Foundation standard, **IMFContentEnabler**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulle API estese del client Windows Media DRM**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




