---
title: Uso di canali con autenticazione sicura
description: Uso di canali con autenticazione sicura
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Media Gestione dispositivi, autenticazione
- Gestione dispositivi, autenticazione
- applicazioni desktop, autenticazione
- provider di servizi, autenticazione
- Guida per programmatori, autenticazione
- autenticazione
- Windows Media Gestione dispositivi, comunicazione protetta
- Gestione dispositivi, comunicazione protetta
- applicazioni desktop, comunicazione protetta
- provider di servizi, comunicazione protetta
- Guida per programmatori, comunicazione sicura
- comunicazione protetta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044343"
---
# <a name="using-secure-authenticated-channels"></a>Uso di canali con autenticazione sicura

Windows Media Gestione dispositivi consente l'autenticazione e la comunicazione sicura tra i componenti fornendo due classi helper, [CSecureChannelClient](csecurechannelclient-class.md) (per le applicazioni) e [CSecureChannelServer](csecurechannelserver-class.md) (per i provider di servizi) e un'interfaccia, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (per entrambi). Insieme costituiscono un'API per l'uso di canali con autenticazione sicura (SAC). SAC gestisce le tre attività seguenti per i provider di servizi o le applicazioni che usano Windows Media Gestione dispositivi:

-   [Autenticazione componenti](component-authentication.md)
-   [Crittografia e decrittografia](encryption-and-decryption.md)
-   [Autenticazione del messaggio](message-authentication.md)

Un'applicazione o un provider di servizi deve gestire l'autenticazione, la crittografia e la decrittografia di componenti. l'autenticazione del messaggio è facoltativa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività comuni per le applicazioni e i provider di servizi**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




