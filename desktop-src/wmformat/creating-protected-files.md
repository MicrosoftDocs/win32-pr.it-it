---
title: Creazione di file protetti
description: Creazione di file protetti
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows Media Format SDK, creazione di file protetti
- Windows MEDIA Format SDK, file protetti
- Advanced Systems Format (ASF), creazione di file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- Advanced Systems Format (ASF), file protetti
- ASF (Advanced Systems Format),file protetti
- Advanced Systems Format (ASF),WMStubDRM.lib
- ASF (Advanced Systems Format),WMStubDRM.lib
- WMStubDRM.lib, creazione di file protetti
- WMStubDRM.lib, file protetti
- digital rights management (DRM),WMStubDRM.lib
- DRM (digital rights management),WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5be729f04f67e1a2e4319bcc8d267c798942293c2df2ee97dcc6a559af612aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809471"
---
# <a name="creating-protected-files"></a>Creazione di file protetti

Per creare file multimediali digitali protetti usando DRM versione 1 o DRM versione 7 e successive, collegarsi al file WMStubDRM.lib ottenuto da Microsoft e creare l'oggetto writer. Per la protezione della versione 1, usare [**l'interfaccia IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) per impostare gli attributi DRM da applicare. Per le versioni 7 e successive, usare i [**metodi di interfaccia IWMDRMWriter.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)

Gli argomenti seguenti descrivono in dettaglio come proteggere i file.

-   [Protezione dei file con DRM versione 1](protecting-files-with-drm-version-1.md)
-   [Protezione dei file con DRM versione 7 o successiva](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

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

[**Recupero della libreria DRM necessaria**](obtaining-the-required-drm-library.md)
</dt> <dt>

[**Lettura di file protetti**](reading-protected-files.md)
</dt> </dl>

 

 




