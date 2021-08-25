---
title: Eliminazione della licenza
description: Eliminazione della licenza
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- Windows Media Format SDK, licenze
- Windows Media Format SDK, eliminazione delle licenze
- digital rights management (DRM), licenze
- DRM (digital rights management), licenze
- digital rights management (DRM), eliminazione di licenze
- DRM (digital rights management), eliminazione delle licenze
- API estese del client DRM, licenze
- API estese client,licenze
- API estese del client DRM, eliminazione delle licenze
- API estese client, eliminazione di licenze
- licenze, eliminazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd1e20c0e98fd2129b807cf11f27f5975701d851d9301eda894ccb24015360a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808301"
---
# <a name="license-deletion"></a>Eliminazione della licenza

Tutte le licenze di terze parti create in locale, ad esempio tramite l'importazione DRM, possono essere eliminate chiamando il metodo [**IWMDRMLicenseManagement::P rocessLicenseDeletionMessage.**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) La stringa passata a questo metodo sarà una licenza XMR simile alla seguente:


```C++
<response type="LRB">
  <DATA>
    <LICENSEDATA>
      <DATA>
        <KID>include Key ID here to revoke certain keys</KID>
        <LID>rights ID</LID
        <META>
          <LGPUBKEY>
            <PublicKey>
              <Modulus>base64 encoded public key</Modulus>
              <Exponent>Exponent in network byte order</Exponent>
            </PublicKey>
          </LGPUBKEY>
          <UID>content-owner-specific user ID</UID>
        </META>
      </DATA>
    </LICENSEDATA>
  </DATA>
</response>
```



Il campo ID utente (UID) specifico del proprietario è facoltativo. I campi facoltativi non devono essere inclusi nella risposta alla licenza se non sono associati dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di una licenza XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importazione DRM**](drm-import.md)
</dt> <dt>

[**Guida per programmatori**](drm-programming-guide.md)
</dt> </dl>

 

 




