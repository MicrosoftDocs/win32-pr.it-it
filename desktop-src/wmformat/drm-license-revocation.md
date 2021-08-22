---
title: Revoca delle licenze (client Microsoft Windows Media DRM)
description: Revoca delle licenze (client Microsoft Windows Media DRM)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows Media Format SDK, licenze
- Windows MEDIA Format SDK, revoca delle licenze
- digital rights management (DRM), licenze
- DRM (Digital Rights Management),licenze
- DRM (Digital Rights Management), revoca delle licenze
- DRM (Digital Rights Management),revoca delle licenze
- API estese del client DRM, licenze
- API client estese, licenze
- API estese del client DRM, revoca delle licenze
- API client estese, revoca delle licenze
- licenze, revoca
- revoca di licenza, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3cd295ddc1aec40c04f5284d791d7482854208a17875bdd3ed60d998f4ccf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027839"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a>Revoca delle licenze (client Microsoft Windows Media DRM)

La revoca delle licenze si riferisce alla rimozione delle licenze da un archivio licenze locale. Uno scenario comune per la revoca delle licenze si verifica quando un provider di servizi, ad esempio un servizio di sottoscrizione musicale, deve disattivare il servizio nel computer di un utente.

Il processo di revoca delle licenze viene avviato da un servizio fornito dall'emittente della licenza. L'applicazione può ospitare questo servizio o può essere un'applicazione Web. In entrambi i casi, l'applicazione deve essere in grado di ricevere una richiesta di licenza creata dal servizio.

Per rimuovere le licenze dall'archivio licenze, eseguire le operazioni seguenti:

1.  Quando si riceve una richiesta di licenza dall'emittente della licenza, creare una richiesta di revoca usando il metodo [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge.**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) Questo metodo alloca un buffer contenente i dati della richiesta di revoca, che vengono passati all'applicazione tramite il *parametro ppbChallengeOutput.*
2.  Inviare la richiesta di revoca delle licenze a un servizio di revoca delle licenze. Il server genererà un BLOB di revoca delle licenze (LRB) in risposta.
3.  Rimuovere la licenza dall'archivio locale usando il metodo [**IWMDRMLicenseManagement::P rocessLicenseRevocationResponse,**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) passando l'LRB restituito dal server licenze.
4.  Deallocare il buffer allocato **da CreateLicenseRevocationChallenge** usando la **funzione CoTaskMemFree.**

Per altre informazioni sul funzionamento della revoca delle licenze o su come scrivere un servizio di revoca, vedere Implementazione della revoca [delle licenze.](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**Archivio licenze locale**](local-license-store.md)
</dt> <dt>

[**Guida per programmatori**](drm-programming-guide.md)
</dt> </dl>

 

 