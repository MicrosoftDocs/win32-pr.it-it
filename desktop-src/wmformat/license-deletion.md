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
# <a name="license-deletion"></a><span data-ttu-id="57cb0-114">Eliminazione della licenza</span><span class="sxs-lookup"><span data-stu-id="57cb0-114">License Deletion</span></span>

<span data-ttu-id="57cb0-115">Tutte le licenze di terze parti create localmente, ad esempio tramite l'importazione DRM, possono essere eliminate chiamando il metodo [**IWMDRMLicenseManagement::P rocesslicensedeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="57cb0-115">Any third-party licenses created locally, for example through DRM import, can be deleted by calling the [**IWMDRMLicenseManagement::ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) method.</span></span> <span data-ttu-id="57cb0-116">La stringa passata a questo metodo sarà una licenza XMR simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="57cb0-116">The string you pass to this method will be an XMR license that resembles the following:</span></span>


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



<span data-ttu-id="57cb0-117">Il campo ID utente specifico del proprietario (UID) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="57cb0-117">The owner specific user ID (UID) field is optional.</span></span> <span data-ttu-id="57cb0-118">I campi facoltativi non devono essere inclusi nella risposta della licenza se non vi sono dati associati.</span><span class="sxs-lookup"><span data-stu-id="57cb0-118">Optional fields must not be included in the license response if there is not any data associated with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57cb0-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57cb0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57cb0-120">**Creazione di una licenza XMR**</span><span class="sxs-lookup"><span data-stu-id="57cb0-120">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="57cb0-121">**Importazione DRM**</span><span class="sxs-lookup"><span data-stu-id="57cb0-121">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="57cb0-122">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="57cb0-122">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




