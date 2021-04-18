---
title: Abilitazione del supporto DRM
description: Abilitazione del supporto DRM
ms.assetid: 90e92373-7fc2-4478-a179-22f22dbc3a3d
keywords:
- Windows Media Format SDK, abilitazione del supporto DRM
- ASF (Advanced Systems Format), abilitazione del supporto DRM
- ASF (Advanced Systems Format), abilitazione del supporto DRM
- Digital Rights Management (DRM), abilitazione del supporto
- DRM (Digital Rights Management), abilitazione del supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936210eb9d560bffe12acf5cc33fb9f864f8404c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300616"
---
# <a name="enabling-drm-support"></a>Abilitazione del supporto DRM

È possibile utilizzare Microsoft Windows Media Format Software Development Kit (SDK) per creare applicazioni che possano applicare la protezione Digital Rights Management (DRM) e riprodurre flussi Live-DRM o file protetti da DRM. Viene anche fornito supporto per il backup e il ripristino delle licenze DRM di un giocatore e per i giocatori [*individualizzazione*](wmformat-glossary.md) .

In questa documentazione si presuppone che l'utente disponga di una conoscenza di base della tecnologia Digital Rights Management Microsoft. Una panoramica di base di Windows Media DRM è disponibile nella sezione [Digital Rights Management Features](digital-rights-management-features.md) di questa documentazione. Per ulteriori informazioni su DRM, vedere la pagina relativa alla Rights Management digitale sul [sito Web Microsoft](https://windows.microsoft.com/windows/products/windows-media).

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

Nelle sezioni seguenti viene descritto come abilitare il supporto DRM.



| Sezione                                                                                                                        | Descrizione                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ottenere la libreria DRM necessaria](obtaining-the-required-drm-library.md)                                                   | Vengono descritti i passaggi necessari per ottenere la libreria statica necessaria per creare applicazioni abilitate per DRM.                                                                               |
| [Protezione DRM e distribuzione delle licenze di contenuti](drm-protection-and-content-license-distribution.md)                         | Confronta le funzionalità DRM di Windows Media Format SDK con Windows Media Rights Manager SDK.                                                                                        |
| [Operazioni di rete DRM](drm-network-operations.md)                                                                           | Viene descritto il modo in cui l'applicazione deve gestire le operazioni DRM che comunicano tramite Internet o altre reti.                                                                          |
| [Creazione di file protetti](creating-protected-files.md)                                                                       | Viene descritto come creare file protetti da DRM.                                                                                                                                                    |
| [Lettura di file protetti](reading-protected-files.md)                                                                         | Descrive come acquisire licenze per il contenuto e i vantaggi derivanti dall'implementazione dell'acquisizione di una licenza invisibile all'utente.                                                                                     |
| [Visualizzazione degli attributi dei file protetti](viewing-attributes-of-protected-files.md)                                             | Viene descritto come utilizzare l'interfaccia [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) nell'oggetto editor dei metadati per visualizzare gli attributi dei file protetti senza disporre della libreria statica necessaria per DRM. |
| [Utilizzo degli elenchi di revoche](working-with-revocation-lists.md)                                                             | Vengono descritti gli elenchi di revoche e il modo in cui vengono implementati.                                                                                                                                        |
| [Backup e ripristino di licenze](backing-up-and-restoring-licenses.md)                                                     | Descrive in che modo gli utenti possono gestire le proprie licenze di contenuto eseguendo il backup e il ripristino nel computer corrente o in altri computer.                                                         |
| [Applicazioni DRM individualizzazione](individualizing-drm-applications.md)                                                       | Viene descritto il modo in cui la funzionalità di [*individualizzazione*](wmformat-glossary.md) migliora la sicurezza in un sistema DRM.                                                           |
| [Utilizzo dei livelli di protezione dell'output](working-with-output-protection-levels.md)                                             | Viene descritto come supportare i livelli di protezione dell'output, usati per registrare le azioni consentite nelle licenze DRM versione 10.                                                                         |
| [Uso del protocollo Windows Media DRM 10 per i dispositivi di rete](using-the-windows-media-drm-10-for-network-devices-protocol.md) | Viene descritto come supportare lo streaming di dispositivi protetti usando il protocollo Windows Media DRM 10 per i dispositivi di rete.                                                                                |
| [Implementazione della revoca delle licenze](implementing-license-revocation.md)                                                         | Descrive il processo di revoca delle licenze e le azioni che l'applicazione deve eseguire per implementarla.                                                                                        |
| [Masterizzazione di playlist contenenti file protetti](burning-playlists-that-contain-secure-files.md)                                 | Viene descritto come implementare la masterizzazione di playlist nell'applicazione.                                                                                                                                |



 

L'SDK include diverse applicazioni di esempio che illustrano come leggere i file protetti. L'esempio più completo è DRMShow. Per altre informazioni, vedere [applicazioni di esempio](sample-applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità**](features.md)
</dt> </dl>

 

 




