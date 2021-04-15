---
title: Acquisizione di licenze
description: Acquisizione di licenze
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- Windows Media Format SDK, API client DRM estese
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, API estese
- Windows Media Format SDK, API
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, acquisizione di licenze
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), API estese del client
- DRM (Digital Rights Management), API estese client
- Digital Rights Management (DRM), API estese
- DRM (Digital Rights Management), API estese
- Digital Rights Management (DRM), API
- DRM (Digital Rights Management), API
- Digital Rights Management (DRM), acquisizione di licenze
- DRM (Digital Rights Management), acquisizione di licenze
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- API estese del client DRM, acquisizione di licenze
- API estese client, acquisizione di licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395362"
---
# <a name="acquiring-licenses"></a>Acquisizione di licenze

Uno scenario comune per l'acquisizione di licenze è quando un utente dispone di un file Windows Media protetto e tenta di accedere al contenuto per la prima volta. Poiché le API estese del client Windows Media DRM sono separate dalle routine di gestione dei file ASF, lo scenario di acquisizione della licenza di base, sebbene supportato, richiede più chiamate API rispetto all'uso di Windows Media Format SDK e di Media Foundation SDK.

Questa sezione descrive come usare le API estese del client Windows Media DRM per acquisire le licenze archiviate nell'archivio licenze locale in un computer client. Contiene gli argomenti seguenti.



| Argomento                                                                | Descrizione                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Acquisizione di una licenza invisibile all'utente](silent-license-acquisition.md)         | Viene descritto come acquisire licenze senza l'intervento dell'utente.                                                                               |
| [Acquisizione di licenza non invisibile all'utente](non-silent-license-acquisition.md) | Viene descritto come acquisire licenze quando è richiesto l'intervento dell'utente, ad esempio il pagamento del contenuto.                                     |
| [Pre-distribuzione della licenza](license-pre-delivery.md)                     | Viene descritto come eseguire il pull delle licenze da un server licenze a un computer client.                                                                 |
| [Creazione di licenze localmente](creating-licenses-locally.md)           | Viene descritto come creare licenze personalizzate senza scaricarle da un server licenze e come archiviarle nell'archivio licenze locale. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](drm-programming-guide.md)
</dt> </dl>

 

 




