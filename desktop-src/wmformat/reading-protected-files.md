---
title: Lettura di file protetti
description: Lettura di file protetti
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media Format SDK, lettura di file protetti
- Windows MEDIA Format SDK, file protetti
- Advanced Systems Format (ASF), lettura di file protetti
- ASF (Advanced Systems Format), lettura di file protetti
- Advanced Systems Format (ASF), file protetti
- ASF (Advanced Systems Format),file protetti
- Advanced Systems Format (ASF),WMStubDRM.lib
- ASF (Advanced Systems Format),WMStubDRM.lib
- WMStubDRM.lib,lettura di file protetti
- WMStubDRM.lib, file protetti
- digital rights management (DRM),WMStubDRM.lib
- DRM (digital rights management),WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c700629fd66fdf0aa8bb1ff837b968232cf9301c39b951dd0a74678c9f1312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846102"
---
# <a name="reading-protected-files"></a>Lettura di file protetti

La lettura di un file protetto da DRM o di un flusso di rete implica fondamentalmente il tentativo di aprire il file (o connettersi al flusso) e quindi di gestire gli eventi che potrebbero essere inviati dai componenti DRM.

Se un lettore non è abilitato per DRM (non si collega a una libreria wmstubdrm.lib valida), la chiamata [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) ha esito negativo quando tenta di aprire un file protetto e restituisce NS E PROTECTED CONTENT o un errore \_ \_ \_ correlato.

Quando un'applicazione abilitata per DRM tenta di aprire un file protetto da DRM, il componente DRM cerca automaticamente una licenza valida nel sistema locale. Se ne viene trovato uno, il componente DRM decrittografa automaticamente il file in modo completamente trasparente per l'applicazione. L'azione che un'applicazione può eseguire sul file decrittografato dipende dai diritti specificati nella licenza. Per una descrizione completa dei diritti possibili, vedere la documentazione Windows Media Rights Manager SDK.

Se l'applicazione non ha una licenza valida per un file, il lettore riceve una notifica di stato dal componente DRM. L'applicazione lettore può quindi avviare il processo [*di acquisizione della*](wmformat-glossary.md) licenza. Dopo aver ricevuto una licenza valida, è possibile accedere al file. Le sezioni seguenti descrivono le attività di base che un'applicazione deve eseguire nell'implementazione del processo di acquisizione delle licenze:

-   [Specifica delle azioni da eseguire](specifying-the-actions-to-be-performed.md)
-   [Gestione degli eventi di acquisizione delle licenze](handling-license-acquisition-events.md)
-   [Individualizzazione di applicazioni DRM](individualizing-drm-applications.md)
-   [Gestione degli eventi di individualizzazione](handling-individualization-events.md)

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Elenco attributi DRM**](drm-attribute-list.md)
</dt> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




