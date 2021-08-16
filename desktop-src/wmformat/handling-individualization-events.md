---
title: Gestione degli eventi di individualizzazione
description: Gestione degli eventi di individualizzazione
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows Media Format SDK, gestione degli eventi di individualizzazione
- Windows Media Format SDK, eventi di individualizzazione
- Advanced Systems Format (ASF), gestione degli eventi di individualizzazione
- ASF (Advanced Systems Format), gestione degli eventi di individualizzazione
- Advanced Systems Format (ASF), eventi di individualizzazione
- ASF (Advanced Systems Format), eventi di individualizzazione
- DRM (Digital Rights Management), gestione degli eventi di individualizzazione
- DRM (Digital Rights Management), gestione degli eventi di individualizzazione
- digital rights management (DRM), eventi di individualizzazione
- DRM (Digital Rights Management),eventi di individualizzazione
- eventi di individualizzazione
- eventi, eventi di individualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895710558c58fca108915ad1a73a0354c1fb39feb662fa3e2c698dadbe4cbe76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433618"
---
# <a name="handling-individualization-events"></a>Gestione degli eventi di individualizzazione

Quando un'applicazione abilitata per DRM tenta di aprire un file protetto, il componente DRM esamina l'attributo [**\_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) nel file, che specifica il livello di versione minimo necessario per accedere al contenuto. Tutti i livelli del componente DRM funzionano con tutte le versioni 7.0 e successive di Windows Media Player e Windows Media Format SDK. Se il livello di versione individualizzato del componente DRM è inferiore alla versione richiesta, il componente DRM invierà un evento **WMT \_ NEEDS \_ INDIVIDUALIZATION** al metodo [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) dell'applicazione. L'applicazione deve quindi visualizzare un messaggio o una finestra di dialogo che richiede agli utenti di avviare o annullare l'aggiornamento della sicurezza. Questa richiesta è necessaria perché, per motivi di privacy, gli utenti devono concedere l'autorizzazione prima di installare un aggiornamento della sicurezza nel computer.

> [!Note]  
> L'intestazione del contenuto specifica solo le prime due cifre per DRM \_ DRMVersion \_ IndividualizedVersion. In altre parole, per richiedere un componente DRM di livello 2.2.0.1, l'intestazione conterrà "2.2".

 

Per avviare l'aggiornamento della sicurezza e/o attivare la individualizzazione, chiamare il metodo [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) con il parametro *dwFlags* impostato su 1.

È necessario gestire **l'evento \_ WMT INDIVIDUALIZE** nell'applicazione. Questo evento verrà generato più volte dal componente DRM con lo stato del processo di individualizzazione indicato nel *parametro pValue,* di cui viene eseguito il cast a un puntatore a una struttura [**WM \_ INDIVIDUALIZE \_ STATUS.**](wm-individualize-status.md)

Dopo che il componente DRM è stato individualizzato correttamente, l'applicazione riceverà un evento **WMT \_ NO RIGHTS \_ \_ EX,** che indica che l'applicazione può ora procedere all'acquisizione di una licenza per il contenuto.

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione degli eventi di acquisizione delle licenze**](handling-license-acquisition-events.md)
</dt> <dt>

[**Individualizzazione di applicazioni DRM**](individualizing-drm-applications.md)
</dt> <dt>

[**Interfaccia IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




