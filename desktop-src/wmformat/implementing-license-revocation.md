---
title: Implementazione della revoca delle licenze
description: Implementazione della revoca delle licenze
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- Windows Media Format SDK, implementazione della revoca delle licenze
- Windows MEDIA Format SDK, revoca delle licenze
- Windows MEDIA Format SDK, revoca delle licenze
- Advanced Systems Format (ASF), implementazione della revoca delle licenze
- ASF (Advanced Systems Format), implementazione della revoca delle licenze
- Advanced Systems Format (ASF), revoca delle licenze
- ASF (Advanced Systems Format),revoca delle licenze
- Advanced Systems Format (ASF), revoca delle licenze
- ASF (Advanced Systems Format),revoca delle licenze
- DRM (Digital Rights Management), implementazione della revoca delle licenze
- DRM (Digital Rights Management), implementazione della revoca delle licenze
- digital rights management (DRM), revoca delle licenze
- DRM (Digital Rights Management),revoca delle licenze
- digital rights management (DRM), revoca delle licenze
- DRM (Digital Rights Management),revoca delle licenze
- revoca di licenze, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c73d0204e83c941600eefb53579b19ef72217055080c6ef4603d8eac28e08caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809131"
---
# <a name="implementing-license-revocation"></a>Implementazione della revoca delle licenze

Il Windows Media Rights Manager 10 SDK include una funzionalità denominata revoca delle licenze. Questa funzionalità consente ai server licenze di richiedere la rimozione delle licenze dal computer client. Il Windows Media Format SDK fornisce metodi che elaborano i messaggi di revoca e rimuovono le licenze dall'archivio licenze locale.

Il processo di revoca delle licenze viene avviato da un servizio fornito dall'emittente della licenza. L'applicazione può ospitare questo servizio o può essere un'applicazione Web. In entrambi i casi, l'applicazione deve essere in grado di ricevere una richiesta di licenza creata dal servizio.

Per rimuovere le licenze dall'archivio licenze, seguire questa procedura:

1.  Quando si riceve una richiesta di licenza dall'emittente della licenza, chiamare la funzione [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) per creare un oggetto agente di revoca delle licenze e ottenere un [**puntatore all'interfaccia IWMLicenseRevocationAgent.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
2.  Chiamare il [**metodo IWMLicenseRevocationAgent::GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) per generare la risposta alla richiesta.
3.  Inviare di nuovo la risposta alla richiesta al componente del servizio licenze da cui è stata ricevuta la richiesta.
4.  Il componente del servizio licenze invia un BLOB di revoca delle licenze firmato all'applicazione. Quando viene ricevuto, chiamare il [**metodo IWMLicenseRevocationAgent::P rocessLRB.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) **ProcessLRB** crea un messaggio di acknowledgement che è necessario inviare al servizio licenze per verificare che le licenze siano state rimosse.

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interfaccia IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




