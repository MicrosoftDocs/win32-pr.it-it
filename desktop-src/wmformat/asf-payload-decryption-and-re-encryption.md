---
title: Decrittografia e ricrittografia del payload ASF
description: Decrittografia e ricrittografia del payload ASF
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- Windows Media Format SDK, decrittografia e ricrittografia del payload ASF
- Windows Media Format SDK, decrittografia del payload e nuova crittografia
- Windows Media Format SDK, decrittografia
- Windows Media Format SDK, nuova crittografia
- Digital Rights Management (DRM), decrittografia e ricrittografia del payload ASF
- DRM (Digital Rights Management), decrittografia e ricrittografia del payload ASF
- Digital Rights Management (DRM), decrittografia e ricrittografia del payload
- DRM (Digital Rights Management), decrittografia e ricrittografia del payload
- Digital Rights Management (DRM), decrittografia
- DRM (Digital Rights Management), decrittografia
- Digital Rights Management (DRM), nuova crittografia
- DRM (Digital Rights Management), nuova crittografia
- API estese del client DRM, decrittografia del payload ASF e nuova crittografia
- API estese del client, decrittografia del payload ASF e nuova crittografia
- API estese del client DRM, decrittografia e ricrittografia del payload
- API estese del client, decrittografia del payload e nuova crittografia
- API estese del client DRM, decrittografia
- API estese client, decrittografia
- API estese del client DRM, nuova crittografia
- API estese client, nuova crittografia
- ASF (Advanced Systems Format), nuova crittografia
- ASF (Advanced Systems Format), nuova crittografia
- ASF (Advanced Systems Format), decrittografia
- ASF (formato avanzato dei sistemi), decrittografia
- ASF (Advanced Systems Format), decrittografia e ricrittografia del payload
- ASF (formato avanzato dei sistemi), decrittografia e ricrittografia del payload
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c6dcab1d483b737b6b05636b51b8af0502350
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707867"
---
# <a name="asf-payload-decryption-and-re-encryption"></a><span data-ttu-id="3ca30-129">Decrittografia e ricrittografia del payload ASF</span><span class="sxs-lookup"><span data-stu-id="3ca30-129">ASF Payload Decryption and Re-encryption</span></span>

<span data-ttu-id="3ca30-130">Nei passaggi seguenti vengono descritte le azioni che un'applicazione deve completare per decrittografare e crittografare di nuovo ogni payload:</span><span class="sxs-lookup"><span data-stu-id="3ca30-130">The steps below describe the actions that an application must complete to decrypt and re-encrypt each payload:</span></span>

1.  <span data-ttu-id="3ca30-131">Incrementare il valore salt.</span><span class="sxs-lookup"><span data-stu-id="3ca30-131">Increment the salt value.</span></span>
2.  <span data-ttu-id="3ca30-132">Passare il payload (crittografato con Windows Media DRM) e il valore salt alla funzione di decrittografia, [**IWMDRMDecrypt::D ecrypt**](iwmdrmdecrypt-decrypt.md), che restituirà il payload, crittografato con la chiave pubblica RC4.</span><span class="sxs-lookup"><span data-stu-id="3ca30-132">Pass the payload (encrypted with Windows Media DRM) and the salt value to the decryption function, [**IWMDRMDecrypt::Decrypt**](iwmdrmdecrypt-decrypt.md), which will return the payload, encrypted using the RC4 public key.</span></span>
3.  <span data-ttu-id="3ca30-133">Derivare una chiave RC4 transitoria applicando un hash SHA-1 del vettore di inizializzazione concatenato con il valore salt.</span><span class="sxs-lookup"><span data-stu-id="3ca30-133">Derive a transitory RC4 key by applying an SHA-1 hash of the initialization vector concatenated with the salt value.</span></span>
4.  <span data-ttu-id="3ca30-134">Usare la chiave temporanea per decrittografare il payload.</span><span class="sxs-lookup"><span data-stu-id="3ca30-134">Use your transitory key to decrypt the payload.</span></span>
5.  <span data-ttu-id="3ca30-135">Crittografare immediatamente il payload con lo schema di protezione del contenuto autorizzato secondo le regole di conformità e affidabilità dell'esportazione DRM di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3ca30-135">Immediately re-encrypt the payload with the authorized content protection scheme according to the Windows Media DRM export compliance and robustness rules.</span></span>
6.  <span data-ttu-id="3ca30-136">Individuare il payload successivo.</span><span class="sxs-lookup"><span data-stu-id="3ca30-136">Locate the next payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ca30-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3ca30-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ca30-138">**Esportazione di contenuto compresso**</span><span class="sxs-lookup"><span data-stu-id="3ca30-138">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




