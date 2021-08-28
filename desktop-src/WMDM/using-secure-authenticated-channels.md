---
title: Uso di canali autenticati sicuri
description: Uso di canali autenticati sicuri
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Gestione dispositivi multimediali, autenticazione
- Gestione dispositivi, autenticazione
- applicazioni desktop, autenticazione
- provider di servizi, autenticazione
- guida per programmatori,autenticazione
- autenticazione
- Windows Gestione dispositivi multimediali, comunicazione sicura
- Gestione dispositivi, comunicazione sicura
- applicazioni desktop, comunicazione sicura
- provider di servizi, comunicazione sicura
- guida alla programmazione, comunicazione sicura
- comunicazione sicura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a86eb364baca933eea1c81e587f99c9381786c5c3f62f2cefcfe3ceaed6e51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124111"
---
# <a name="using-secure-authenticated-channels"></a>Uso di canali autenticati sicuri

Windows Gestione dispositivi multimediali consente l'autenticazione e la comunicazione sicura tra i componenti fornendo due classi helper, [CSecureChannelClient](csecurechannelclient-class.md) (per le applicazioni) e [CSecureChannelServer](csecurechannelserver-class.md) (per i provider di servizi) e un'interfaccia, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (per entrambi). Insieme costituiscono un'API per l'uso di canali autenticati sicuri (SAC). SAC gestisce le tre attività seguenti per i provider di servizi o le applicazioni Windows Gestione dispositivi multimediali:

-   [Autenticazione dei componenti](component-authentication.md)
-   [Crittografia e decrittografia](encryption-and-decryption.md)
-   [Autenticazione dei messaggi](message-authentication.md)

Un provider di applicazioni o servizi deve gestire l'autenticazione, la crittografia e la decrittografia dei componenti; L'autenticazione dei messaggi è facoltativa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività comuni ad applicazioni e provider di servizi**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




