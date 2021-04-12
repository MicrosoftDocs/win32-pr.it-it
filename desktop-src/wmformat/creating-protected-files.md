---
title: Creazione di file protetti
description: Creazione di file protetti
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows Media Format SDK, creazione di file protetti
- Windows Media Format SDK, file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- ASF (Advanced Systems Format), file protetti
- ASF (Advanced Systems Format), file protetti
- Formato Advanced Systems (ASF), WMStubDRM. lib
- ASF (formato avanzato dei sistemi), WMStubDRM. lib
- WMStubDRM. lib, creazione di file protetti
- WMStubDRM. lib, file protetti
- Digital Rights Management (DRM), WMStubDRM. lib
- DRM (Digital Rights Management), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a14d96da924bdb2a307bc804514a1ec3de083
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336313"
---
# <a name="creating-protected-files"></a>Creazione di file protetti

Per creare file multimediali digitali protetti usando DRM versione 1 o DRM 7 e versioni successive, eseguire il collegamento al file WMStubDRM. lib ottenuto da Microsoft e creare l'oggetto writer. Per la protezione della versione 1, utilizzare l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) per impostare gli attributi DRM che si desidera applicare. Per le versioni 7 e successive, usare i metodi di interfaccia [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) .

Negli argomenti seguenti viene descritto in dettaglio come proteggere i file.

-   [Protezione dei file con DRM versione 1](protecting-files-with-drm-version-1.md)
-   [Protezione dei file con DRM 7 o versione successiva](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elenco attributi DRM**](drm-attribute-list.md)
</dt> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> <dt>

[**Versioni DRM**](drm-versions.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**Ottenere la libreria DRM necessaria**](obtaining-the-required-drm-library.md)
</dt> <dt>

[**Lettura di file protetti**](reading-protected-files.md)
</dt> </dl>

 

 




