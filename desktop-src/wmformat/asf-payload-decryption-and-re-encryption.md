---
title: Decrittografia e ricrittografia del payload ASF
description: Decrittografia e ricrittografia del payload ASF
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- Windows MEDIA Format SDK, decrittografia del payload ASF e ricrittografia
- Windows MEDIA Format SDK, decrittografia del payload e ricrittografia
- Windows MEDIA Format SDK, decrittografia
- Windows Media Format SDK, ricritto crittografia
- digital rights management (DRM), decrittografia e ricrittografia del payload ASF
- DRM (digital rights management), decrittografia e ricrittografia del payload ASF
- digital Rights Management (DRM), decrittografia del payload e ricrittografia
- DRM (digital rights management), decrittografia del payload e ricrittografia
- digital rights management (DRM), decrittografia
- DRM (digital rights management), decrittografia
- digital rights management (DRM), ri-crittografia
- DRM (digital rights management), ri-crittografia
- API estese del client DRM, decrittografia del payload ASF e ricrittografia
- API estese client, decrittografia del payload ASF e ricrittografia
- API estese del client DRM, decrittografia del payload e ricrittografia
- API estese client, decrittografia del payload e ricrittografia
- API estese del client DRM, decrittografia
- API estese client, decrittografia
- API estese del client DRM, nuova crittografia
- API estese client, nuova crittografia
- Advanced Systems Format (ASF), re-encryption
- ASF (Advanced Systems Format), re-encryption
- Advanced Systems Format (ASF), decrittografia
- ASF (Advanced Systems Format), decrittografia
- Advanced Systems Format (ASF), decrittografia del payload e ricrittografia
- ASF (Advanced Systems Format), decrittografia del payload e ricrittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c60469ff0b1408fcf51cb3dde899559980790a09c01b6619b3ff2ba797554a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007111"
---
# <a name="asf-payload-decryption-and-re-encryption"></a>Decrittografia e ricrittografia del payload ASF

La procedura seguente descrive le azioni che un'applicazione deve completare per decrittografare e crittografare nuovamente ogni payload:

1.  Incrementare il valore salt.
2.  Passare il payload (crittografato con Windows Media DRM) e il valore salt alla funzione di decrittografia, [**IWMDRMDecrypt::D ecrypt,**](iwmdrmdecrypt-decrypt.md)che restituirà il payload, crittografato usando la chiave pubblica RC4.
3.  Derivare una chiave RC4 transitoria applicando un hash SHA-1 del vettore di inizializzazione concatenato al valore salt.
4.  Usare la chiave transitoria per decrittografare il payload.
5.  Crittografare immediatamente il payload con lo schema di protezione del contenuto autorizzato in base Windows regole di conformità e affidabilità dell'esportazione di Media DRM.
6.  Individuare il payload successivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esportazione di contenuto compresso**](exporting-compressed-content.md)
</dt> </dl>

 

 




