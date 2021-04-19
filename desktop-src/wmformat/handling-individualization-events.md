---
title: Gestione degli eventi di individualizzazione
description: Gestione degli eventi di individualizzazione
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows Media Format SDK, gestione di eventi di individualizzazione
- Windows Media Format SDK, eventi di individualizzazione
- Formato di sistemi avanzati (ASF), gestione di eventi di individualizzazione
- ASF (formato avanzato dei sistemi), gestione di eventi di individualizzazione
- ASF (Advanced Systems Format), eventi di individualizzazione
- ASF (formato avanzato dei sistemi), eventi di individualizzazione
- Digital Rights Management (DRM), gestione di eventi di individualizzazione
- DRM (Digital Rights Management), gestione di eventi di individualizzazione
- Digital Rights Management (DRM), eventi di individualizzazione
- DRM (Digital Rights Management), eventi di individualizzazione
- eventi di individualizzazione
- eventi, eventi di individualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e74df94bf871ec62ec2acb94658785969812640
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299412"
---
# <a name="handling-individualization-events"></a>Gestione degli eventi di individualizzazione

Quando un'applicazione abilitata per il DRM tenta di aprire un file protetto, il componente DRM esamina l'attributo [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) nel file, che specifica il livello di versione minimo necessario per accedere al contenuto. Tutti i livelli del componente DRM funzionano con tutte le versioni 7,0 e successive di Windows Media Player e Windows Media Format SDK. Se il livello di versione individualizzato del componente DRM è inferiore alla versione richiesta, il componente DRM invierà un evento **WMT \_ needs \_ individualation** al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) dell'applicazione. Nell'applicazione deve quindi essere visualizzato un messaggio o una finestra di dialogo in cui viene richiesto agli utenti di avviare o annullare l'aggiornamento della sicurezza. Questa richiesta è necessaria perché, per motivi di privacy, gli utenti devono concedere l'autorizzazione prima che nel computer venga installato un aggiornamento della sicurezza.

> [!Note]  
> L'intestazione del contenuto specifica solo le prime due cifre per DRM \_ DRMVersion \_ IndividualizedVersion. In altre parole, per richiedere un componente 2.2.0.1 DRM di livello, l'intestazione conterrebbe "2,2".

 

Per avviare l'aggiornamento della sicurezza e/o attivare l'individualizzazione, chiamare il metodo [**IWMDRMReader:: individualizzato**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) con il parametro *dwFlags* impostato su 1.

È necessario gestire l'evento **WMT di \_ personalizzazione** dell'applicazione. Questo evento verrà generato più volte dal componente DRM con lo stato del processo di individualizzazione indicato nel parametro *pValue* , di cui viene eseguito il cast su un puntatore a una struttura di [**\_ \_ stato di personalizzazione WM**](wm-individualize-status.md) .

Una volta che il componente DRM è stato personalizzato correttamente, l'applicazione riceverà un evento **WMT \_ No \_ Rights \_** , che indica che l'applicazione può ora procedere con l'acquisizione di una licenza per il contenuto.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione degli eventi di acquisizione delle licenze**](handling-license-acquisition-events.md)
</dt> <dt>

[**Applicazioni DRM individualizzazione**](individualizing-drm-applications.md)
</dt> <dt>

[**Interfaccia IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




