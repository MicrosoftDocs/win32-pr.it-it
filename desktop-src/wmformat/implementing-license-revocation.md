---
title: Implementazione della revoca delle licenze
description: Implementazione della revoca delle licenze
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- Windows Media Format SDK, implementazione della revoca delle licenze
- Windows Media Format SDK, revoca delle licenze
- Windows Media Format SDK, revoca delle licenze
- ASF (Advanced Systems Format), implementazione della revoca delle licenze
- ASF (Advanced Systems Format), implementazione della revoca delle licenze
- ASF (Advanced Systems Format), revoca delle licenze
- ASF (formato avanzato dei sistemi), revoca delle licenze
- ASF (Advanced Systems Format), revoca delle licenze
- ASF (formato avanzato dei sistemi), revoca delle licenze
- Digital Rights Management (DRM), implementazione della revoca delle licenze
- DRM (Digital Rights Management), implementazione della revoca delle licenze
- Digital Rights Management (DRM), revoca delle licenze
- DRM (Digital Rights Management), revoca delle licenze
- Digital Rights Management (DRM), revoca delle licenze
- DRM (Digital Rights Management), revoca delle licenze
- revoca delle licenze, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83bfb1a512b031f5b7c297ecede4ed33fba8f2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723567"
---
# <a name="implementing-license-revocation"></a>Implementazione della revoca delle licenze

Windows Media Rights Manager 10 SDK include una funzionalità denominata revoca delle licenze. Questa funzionalità consente ai server licenze di richiedere la rimozione delle licenze dal computer client. Windows Media Format SDK fornisce metodi che elaborano i messaggi di revoca e rimuovono le licenze dall'archivio licenze locale.

Il processo di revoca della licenza viene avviato da un servizio fornito dall'autorità di certificazione. L'applicazione può ospitare questo servizio o può essere un'applicazione Web. In entrambi i casi, l'applicazione deve essere in grado di ricevere una richiesta di licenza creata dal servizio.

Per rimuovere le licenze dall'archivio licenze, seguire questa procedura:

1.  Quando si riceve una richiesta di licenza dall'autorità emittente della licenza, chiamare la funzione [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) per creare un oggetto agente di revoca delle licenze e ottenere un puntatore all'interfaccia [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .
2.  Chiamare il metodo [**IWMLicenseRevocationAgent:: GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) per generare la risposta alla richiesta di verifica.
3.  Inviare la risposta alla richiesta di verifica al componente del servizio licenze dal quale è stata ricevuta la richiesta di verifica.
4.  Il componente del servizio licenze invia un BLOB di revoche di licenze firmato (LRB) all'applicazione. Quando viene ricevuta, chiamare il metodo [**IWMLicenseRevocationAgent::P rocesslrb**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) . **ProcessLRB** crea un messaggio di riconoscimento che è necessario restituire al servizio licenze per verificare che le licenze siano state rimosse.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interfaccia IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




