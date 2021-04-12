---
title: Revoca delle licenze (client Microsoft Windows Media DRM)
description: Revoca delle licenze (client Microsoft Windows Media DRM)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows Media Format SDK, licenze
- Windows Media Format SDK, revoca delle licenze
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), revoca delle licenze
- DRM (Digital Rights Management), revoca delle licenze
- API estese del client DRM, licenze
- API estese client, licenze
- API estese del client DRM, revoca delle licenze
- API estese client, revoca delle licenze
- licenze, revoca
- revoca delle licenze, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234432"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a>Revoca delle licenze (client Microsoft Windows Media DRM)

La revoca delle licenze si riferisce alla rimozione delle licenze da un archivio licenze locale. Uno scenario comune per la revoca delle licenze si verifica quando un provider di servizi, ad esempio un servizio di abbonamento musicale, deve disattivare il servizio nel computer di un utente.

Il processo di revoca della licenza viene avviato da un servizio fornito dall'autorità di certificazione. L'applicazione può ospitare questo servizio o può essere un'applicazione Web. In entrambi i casi, l'applicazione deve essere in grado di ricevere una richiesta di licenza creata dal servizio.

Per rimuovere le licenze dall'archivio licenze, eseguire le operazioni seguenti:

1.  Quando si riceve una richiesta di licenza dall'emittente della licenza, creare una richiesta di revoca usando il metodo [**IWMDRMLicenseManagement:: CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) . Questo metodo consente di allocare un buffer contenente i dati di una richiesta di revoca, che vengono passati all'applicazione tramite il parametro *ppbChallengeOutput* .
2.  Inviare la richiesta di revoca della licenza a un servizio di revoca delle licenze. Il server genererà un BLOB di revoca delle licenze (LRB) in risposta.
3.  Rimuovere la licenza dall'archivio locale usando il metodo [**IWMDRMLicenseManagement::P rocesslicenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) , passando il LRB restituito dal server licenze.
4.  Deallocare il buffer allocato da **CreateLicenseRevocationChallenge** tramite la funzione **CoTaskMemFree** .

Per ulteriori informazioni sul funzionamento della revoca delle licenze o su come scrivere un servizio di revoca, vedere Implementazione della revoca delle [licenze](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**Archivio licenze locale**](local-license-store.md)
</dt> <dt>

[**Guida per programmatori**](drm-programming-guide.md)
</dt> </dl>

 

 