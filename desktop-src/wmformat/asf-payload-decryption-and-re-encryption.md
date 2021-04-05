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
# <a name="asf-payload-decryption-and-re-encryption"></a>Decrittografia e ricrittografia del payload ASF

Nei passaggi seguenti vengono descritte le azioni che un'applicazione deve completare per decrittografare e crittografare di nuovo ogni payload:

1.  Incrementare il valore salt.
2.  Passare il payload (crittografato con Windows Media DRM) e il valore salt alla funzione di decrittografia, [**IWMDRMDecrypt::D ecrypt**](iwmdrmdecrypt-decrypt.md), che restituirà il payload, crittografato con la chiave pubblica RC4.
3.  Derivare una chiave RC4 transitoria applicando un hash SHA-1 del vettore di inizializzazione concatenato con il valore salt.
4.  Usare la chiave temporanea per decrittografare il payload.
5.  Crittografare immediatamente il payload con lo schema di protezione del contenuto autorizzato secondo le regole di conformità e affidabilità dell'esportazione DRM di Windows Media.
6.  Individuare il payload successivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esportazione di contenuto compresso**](exporting-compressed-content.md)
</dt> </dl>

 

 




