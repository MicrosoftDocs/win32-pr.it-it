---
title: Lettura di file protetti
description: Lettura di file protetti
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media Format SDK, lettura di file protetti
- Windows Media Format SDK, file protetti
- ASF (Advanced Systems Format), lettura di file protetti
- ASF (Advanced Systems Format), lettura di file protetti
- ASF (Advanced Systems Format), file protetti
- ASF (Advanced Systems Format), file protetti
- Formato Advanced Systems (ASF), WMStubDRM. lib
- ASF (formato avanzato dei sistemi), WMStubDRM. lib
- WMStubDRM. lib, lettura di file protetti
- WMStubDRM. lib, file protetti
- Digital Rights Management (DRM), WMStubDRM. lib
- DRM (Digital Rights Management), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723407"
---
# <a name="reading-protected-files"></a>Lettura di file protetti

La lettura di un file o di un flusso di rete protetto da DRM comporta fondamentalmente il tentativo di aprire il file (o connettersi al flusso) e quindi di gestire gli eventi che potrebbero essere inviati dai componenti di DRM.

Se un lettore non è abilitato per il DRM (non si collega a una libreria WMStubDRM. lib valida), la chiamata [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) non riesce quando tenta di aprire un file protetto e restituisce \_ contenuto protetto da NS e \_ \_ o un errore correlato.

Quando un'applicazione abilitata per DRM tenta di aprire un file protetto da DRM, il componente DRM cerca automaticamente nel sistema locale una licenza valida. Se ne viene individuato uno, il componente DRM decrittografa automaticamente il file in modo completamente trasparente per l'applicazione. L'azione che un'applicazione può eseguire sul file decrittografato dipende dai diritti specificati nella licenza. Per una descrizione completa dei diritti possibili, vedere la documentazione di Windows Media Rights Manager SDK.

Se l'applicazione non dispone di una licenza valida per un file, il lettore riceve una notifica di stato dal componente DRM. L'applicazione Player può quindi avviare il processo di [*acquisizione delle licenze*](wmformat-glossary.md) . Dopo la ricezione di una licenza valida, è possibile accedere al file. Nelle sezioni seguenti vengono descritte le attività di base che un'applicazione deve eseguire durante l'implementazione del processo di acquisizione della licenza:

-   [Specifica delle azioni da eseguire](specifying-the-actions-to-be-performed.md)
-   [Gestione degli eventi di acquisizione delle licenze](handling-license-acquisition-events.md)
-   [Applicazioni DRM individualizzazione](individualizing-drm-applications.md)
-   [Gestione degli eventi di individualizzazione](handling-individualization-events.md)

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Elenco attributi DRM**](drm-attribute-list.md)
</dt> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




