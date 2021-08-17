---
title: Visualizzazione degli attributi dei file protetti
description: Visualizzazione degli attributi dei file protetti
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows Media Format SDK, visualizzazione degli attributi dei file protetti
- Windows Media Format SDK, attributi dei file protetti
- Windows Media Format SDK,file protetti
- Advanced Systems Format (ASF), visualizzazione degli attributi dei file protetti
- ASF (Advanced Systems Format), visualizzazione degli attributi dei file protetti
- Advanced Systems Format (ASF), attributi dei file protetti
- ASF (Advanced Systems Format), attributi dei file protetti
- Advanced Systems Format (ASF), file protetti
- ASF (Advanced Systems Format), file protetti
- digital rights management (DRM), visualizzazione degli attributi dei file protetti
- DRM (digital rights management), visualizzazione degli attributi dei file protetti
- DRM (Digital Rights Management), attributi dei file protetti
- DRM (digital rights management),attributi dei file protetti
- digital rights management (DRM), file protetti
- DRM (digital rights management), file protetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37cd09e61dbd5515d643cbffe8cce809d0f828e8d153858c78ee52db7e714344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844914"
---
# <a name="viewing-attributes-of-protected-files"></a>Visualizzazione degli attributi dei file protetti

In alcuni scenari potrebbe essere necessario recuperare determinati attributi DRM in un file senza accedere effettivamente al contenuto del file. Questa funzionalità è utile, ad esempio, nelle applicazioni che elaborano batch di file in modi diversi in base alle informazioni nell'intestazione del file. Nelle versioni precedenti di Windows Media Format SDK, le applicazioni dovevano collegarsi alla libreria statica DRM per aprire qualsiasi file protetto. Le applicazioni che non dispongono della libreria DRM possono usare [**l'interfaccia IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) nell'oggetto editor di metadati per esaminare determinati attributi DRM.

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elenco attributi DRM**](drm-attribute-list.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interfaccia IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




