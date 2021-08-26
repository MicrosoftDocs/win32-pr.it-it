---
title: Abilitazione del supporto DRM
description: Abilitazione del supporto DRM
ms.assetid: 90e92373-7fc2-4478-a179-22f22dbc3a3d
keywords:
- Windows Media Format SDK, abilitazione del supporto DRM
- Advanced Systems Format (ASF), abilitazione del supporto DRM
- ASF (Advanced Systems Format), abilitazione del supporto DRM
- digital rights management (DRM), abilitazione del supporto
- DRM (digital rights management), abilitazione del supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dca900089e93b9f2c149f1e349bdf5b91f88a7c3d549b5f54147839a8ed9296
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089751"
---
# <a name="enabling-drm-support"></a>Abilitazione del supporto DRM

È possibile usare Microsoft Windows Media Format Software Development Kit (SDK) per creare applicazioni in grado di applicare la protezione DRM (Digital Rights Management) e riprodurre flussi DRM live o file protetti da DRM. Viene fornito anche il supporto per il backup e il ripristino delle licenze DRM di un giocatore e per [*l'individualizzazione dei*](wmformat-glossary.md) giocatori.

Questa documentazione presuppone che l'utente abbia una familiarità di base con la tecnologia di gestione dei diritti digitali di Microsoft. Una panoramica di base di Windows Media DRM è disponibile nella sezione [Digital Rights Management Features](digital-rights-management-features.md) di questa documentazione. Per altre informazioni su DRM, vedere la pagina digital Rights Management nel [sito Web Microsoft](https://windows.microsoft.com/windows/products/windows-media).

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

Le sezioni seguenti descrivono come abilitare il supporto DRM.



| Sezione                                                                                                                        | Descrizione                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Recupero della libreria DRM richiesta](obtaining-the-required-drm-library.md)                                                   | Descrive i passaggi necessari per ottenere la libreria statica necessaria per creare applicazioni abilitate per DRM.                                                                               |
| [Protezione DRM e distribuzione delle licenze dei contenuti](drm-protection-and-content-license-distribution.md)                         | Confronta le funzionalità DRM di Windows Media Format SDK con Windows Media Rights Manager SDK.                                                                                        |
| [Operazioni di rete DRM](drm-network-operations.md)                                                                           | Descrive come l'applicazione deve gestire le operazioni DRM che comunicano tramite Internet o altre reti.                                                                          |
| [Creazione di file protetti](creating-protected-files.md)                                                                       | Viene descritto come creare file protetti da DRM.                                                                                                                                                    |
| [Lettura di file protetti](reading-protected-files.md)                                                                         | Vengono descritti i modi per acquisire licenze per il contenuto e i vantaggi dell'implementazione dell'acquisizione di licenze invisibile all'utente.                                                                                     |
| [Visualizzazione degli attributi dei file protetti](viewing-attributes-of-protected-files.md)                                             | Viene descritto come usare [**l'interfaccia IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) nell'oggetto editor di metadati per visualizzare gli attributi dei file protetti senza avere la libreria statica necessaria per DRM. |
| [Uso degli elenchi di revoche](working-with-revocation-lists.md)                                                             | Vengono descritti gli elenchi di revoche e il modo in cui vengono implementati.                                                                                                                                        |
| [Backup e ripristino delle licenze](backing-up-and-restoring-licenses.md)                                                     | Descrive come gli utenti possono gestire le licenze per il contenuto tramite il backup e il ripristino nel computer corrente o in altri computer.                                                         |
| [Individualizzazione delle applicazioni DRM](individualizing-drm-applications.md)                                                       | Descrive come la funzionalità [*di individualizzazione*](wmformat-glossary.md) aumenta la sicurezza in un sistema DRM.                                                           |
| [Uso dei livelli di protezione dell'output](working-with-output-protection-levels.md)                                             | Descrive come supportare i livelli di protezione dell'output, usati per registrare le azioni consentite nelle licenze DRM versione 10.                                                                         |
| [Uso del Windows DRM 10 per dispositivi di rete](using-the-windows-media-drm-10-for-network-devices-protocol.md) | Descrive come supportare lo streaming sicuro dei dispositivi usando il Windows Media DRM 10 per dispositivi di rete.                                                                                |
| [Implementazione della revoca delle licenze](implementing-license-revocation.md)                                                         | Descrive il processo di revoca della licenza e le azioni che l'applicazione deve intraprendere per implementarla.                                                                                        |
| [Masterizzazione di playlist contenenti file protetti](burning-playlists-that-contain-secure-files.md)                                 | Viene descritto come implementare la riproduzione di playlist nell'applicazione.                                                                                                                                |



 

L'SDK include diverse applicazioni di esempio che illustrano come leggere i file protetti. l'esempio più completo è DRMShow. Per altre informazioni, vedere [Applicazioni di esempio.](sample-applications.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità**](features.md)
</dt> </dl>

 

 




