---
title: Eliminazione della licenza
description: Eliminazione della licenza
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- Windows Media Format SDK, licenze
- Windows Media Format SDK, eliminazione di licenze
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), eliminazione di licenze
- DRM (Digital Rights Management), eliminazione di licenze
- API estese del client DRM, licenze
- API estese client, licenze
- API estese del client DRM, eliminazione di licenze
- API estese client, eliminazione di licenze
- licenze, eliminazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f297db679ac2c8afe2c836d032fa045d6955665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298323"
---
# <a name="license-deletion"></a>Eliminazione della licenza

Tutte le licenze di terze parti create localmente, ad esempio tramite l'importazione DRM, possono essere eliminate chiamando il metodo [**IWMDRMLicenseManagement::P rocesslicensedeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) . La stringa passata a questo metodo sarà una licenza XMR simile alla seguente:


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



Il campo ID utente specifico del proprietario (UID) è facoltativo. I campi facoltativi non devono essere inclusi nella risposta della licenza se non vi sono dati associati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di una licenza XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importazione DRM**](drm-import.md)
</dt> <dt>

[**Guida per programmatori**](drm-programming-guide.md)
</dt> </dl>

 

 




