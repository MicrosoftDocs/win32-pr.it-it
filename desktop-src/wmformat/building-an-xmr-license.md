---
title: Creazione di una licenza XMR
description: Creazione di una licenza XMR
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows Media Format SDK, importazione DRM
- Windows Media Format SDK, importazione
- Windows Media Format SDK, licenze XMR
- Windows Media Format SDK, licenze
- Windows Media Format SDK, diritti multimediali estendibili (XMR)
- Digital Rights Management (DRM), importazione
- DRM (Digital Rights Management), importazione
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), licenze XMR
- DRM (Digital Rights Management), licenze XMR
- Digital Rights Management (DRM), diritti multimediali estendibili (XMR)
- DRM (Digital Rights Management), diritti multimediali estendibili (XMR)
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, licenze XMR
- API estese client, licenze XMR
- API estese del client DRM, licenze
- API estese client, licenze
- API estese del client DRM, diritti multimediali estendibili (XMR)
- API estese client, diritti multimediali estendibili (XMR)
- licenze, XMR
- Diritti multimediali estendibili (XMR)
- XMR (diritti multimediali estendibili)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc275419116362c08cabe4dc70aa227687705fdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395323"
---
# <a name="building-an-xmr-license"></a>Creazione di una licenza XMR

Per generare una licenza per Windows Media DRM da elaborare, è necessario utilizzare lo schema binario XMR (Extensible Media Rights). XMR è uno schema per la trasmissione dei diritti e delle restrizioni di utilizzo dei supporti e deve essere concesso in licenza separatamente.

Il materiale importante in una licenza viene crittografato con la chiave pubblica nella raccolta di certificati DRM di Windows Media, quindi è visibile solo al sottosistema API client Windows Media DRM esteso. .

È responsabilità dell'utente assicurarsi che le impostazioni relative alla struttura e ai criteri di licenza siano valide e coerenti con l'intento dell'emittente di licenze e che siano conformi alle regole di conformità.

È necessario leggere le regole di conformità dell'importazione DRM di Windows Media per apprendere il set completo di oggetti XMR che devono essere presenti nella licenza.

Per passare la licenza XMR al sottosistema DRM, chiamare il metodo [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) . Usare il formato seguente per passare la licenza nel parametro *bstrLicenseResponse* :


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



Questa stringa deve essere in formato Unicode (UTF-16).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Importazione DRM**](drm-import.md)
</dt> </dl>

 

 




