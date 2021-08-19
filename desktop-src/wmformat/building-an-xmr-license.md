---
title: Creazione di una licenza XMR
description: Creazione di una licenza XMR
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows Media Format SDK, importazione DRM
- Windows Media Format SDK, importazione
- Windows Media Format SDK,licenze XMR
- Windows Media Format SDK, licenze
- Windows Media Format SDK,Extensible Media Rights (XMR)
- digital rights management (DRM), importazione
- DRM (digital rights management), importazione
- digital rights management (DRM), licenze
- DRM (digital rights management), licenze
- digital rights management (DRM), licenze XMR
- DRM (digital rights management),licenze XMR
- digital rights management (DRM), Extensible Media Rights (XMR)
- DRM (digital rights management),Extensible Media Rights (XMR)
- API estese del client DRM,importazione
- API estese client,importazione
- API estese del client DRM, licenze XMR
- API estese client,licenze XMR
- API estese del client DRM, licenze
- API estese client,licenze
- API estese del client DRM, diritti dei supporti estendibile (XMR)
- API estese client, Diritti multimediali estendibile (XMR)
- licenze, XMR
- Diritti dei supporti estendibili (XMR)
- XMR (Diritti multimediali estendibili)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a73406d36c6ec7903ee7966f162811336aaecccaac5093e6d467e02c1a56ec71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881402"
---
# <a name="building-an-xmr-license"></a>Creazione di una licenza XMR

Per generare una licenza per Windows media DRM da elaborare, è necessario usare lo schema binario XMR (Extensible Media Rights). XMR è uno schema per trasmettere diritti e restrizioni di utilizzo dei supporti e deve essere concesso in licenza separatamente.

Il materiale importante in una licenza viene crittografato usando la chiave pubblica nella raccolta di certificati DRM di Windows Media, in modo che sia visibile solo al sottosistema api estesa del client DRM di Windows Media. .

È responsabilità dell'utente assicurarsi che la struttura delle licenze e le impostazioni dei criteri siano valide e coerenti con la finalità dell'autorità emittente della licenza e che siano conformi alle regole di conformità.

Per informazioni sul set completo di oggetti XMR che devono essere presenti nella licenza, è consigliabile leggere le regole di conformità Windows'importazione di Media DRM.

Per passare la licenza XMR al sottosistema DRM, chiamare il metodo [**IWMDRMLicenseManagement::StoreLicense.**](iwmdrmlicensemanagement-storelicense.md) Usare il formato seguente per passare la licenza nel *parametro bstrLicenseResponse:*


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

 

 




