---
title: Uso del protocollo Windows Media DRM 10 per i dispositivi di rete
description: Uso del protocollo Windows Media DRM 10 per i dispositivi di rete
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- Windows Media Format SDK, Windows Media DRM 10 per i dispositivi di rete
- Windows Media Format SDK, DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), Windows Media DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), Windows Media DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), DRM 10 per i dispositivi di rete
- ASF (Advanced Systems Format), DRM 10 per i dispositivi di rete
- Digital Rights Management (DRM), Windows Media DRM 10 per i dispositivi di rete
- DRM (Digital Rights Management), Windows Media DRM 10 per i dispositivi di rete
- Digital Rights Management (DRM), DRM 10 per i dispositivi di rete
- DRM (Digital Rights Management), DRM 10 per i dispositivi di rete
- Windows Media DRM 10 per dispositivi di rete, protocolli
- DRM 10 per dispositivi di rete, protocolli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329692"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a>Uso del protocollo Windows Media DRM 10 per i dispositivi di rete

Windows Media Format SDK fornisce alcune funzionalità per il supporto del protocollo Secure Network Device Protocol, Windows Media DRM 10 per i dispositivi di rete. Questo protocollo definisce i messaggi inviati tra un dispositivo di riproduzione multimediale digitale, ad esempio un lettore video set-top, e il computer che fornisce i dati al dispositivo. I dati multimediali inviati tra il server e il dispositivo vengono crittografati per proteggerli dall'intercettazione.

La comunicazione tra l'applicazione e i dispositivi che supportano Windows Media DRM 10 per i dispositivi di rete può usare tutti i protocolli di rete che preferisci. Windows Media Format SDK non fornisce alcun oggetto che esegua le comunicazioni di rete. Al contrario, gli oggetti di questo SDK elaborano i messaggi di Windows Media DRM 10 per i dispositivi di rete dopo che sono stati ricevuti dall'applicazione.

Le funzionalità che supportano Windows Media DRM 10 per i dispositivi di rete sono la registrazione del dispositivo, il rilevamento della prossimità e la conversione di file protetti da DRM. Queste funzionalità sono descritte nelle sezioni riportate di seguito.



| Sezione                                                                                                                                                                          | Descrizione                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Registrazione del dispositivo](device-registration.md)                                                                                                                                   | Viene descritto come elaborare i messaggi di richiesta di registrazione dai dispositivi.                                                                       |
| [Esecuzione del rilevamento della prossimità](performing-proximity-detection.md)                                                                                                             | Descrive il processo di rilevamento della prossimità.                                                                                                 |
| [Conversione di un file di DRM-Protected in un flusso Windows Media DRM 10 per dispositivi di rete](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | Viene descritto come convertire un file protetto da DRM in un flusso che può essere inviato a un dispositivo che usa Windows Media DRM 10 per i dispositivi di rete. |



 

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




