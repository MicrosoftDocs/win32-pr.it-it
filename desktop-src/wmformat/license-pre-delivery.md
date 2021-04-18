---
title: Pre-distribuzione della licenza
description: Pre-distribuzione della licenza
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- Windows Media Format SDK, pre-distribuzione delle licenze
- Windows Media Format SDK, licenze
- Digital Rights Management (DRM), pre-distribuzione delle licenze
- DRM (Digital Rights Management), pre-distribuzione delle licenze
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- API estese del client DRM, pre-distribuzione delle licenze
- API estese del client, pre-distribuzione delle licenze
- pre-distribuzione delle licenze
- licenze, pre-consegna delle licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300276"
---
# <a name="license-pre-delivery"></a>Pre-distribuzione della licenza

Il pre-recapito della licenza è il processo usato per effettuare il pull delle licenze in un computer client in modo preemptive. Uno scenario comune per l'uso del pre-recapito è quando un utente sottoscrive un servizio musicale. Senza dover consegnare le licenze prima che siano necessarie, l'utente deve attendere l'acquisizione delle licenze per ogni nuova canzone.

Poiché il pre-recapito non viene eseguito come risposta a un tentativo di accesso, viene in genere eseguito solo dal proprietario del contenuto. Ovvero è possibile predisporre solo le licenze per il contenuto controllato. Il processo di pre-distribuzione è un coordinamento tra un componente client e un server licenze compilato utilizzando gli oggetti di Windows Media Digital Rights Management SDK.

Il pre-recapito della licenza è simile all'acquisizione di una [licenza non invisibile all'utente](non-silent-license-acquisition.md). Seguire gli stessi passaggi, ad eccezione del fatto che non si ha un'intestazione DRM da passare a [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md). Il metodo genererà una richiesta di verifica non specifica del contenuto che è possibile inviare al server licenze.

In alternativa, è possibile usare [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) per la pre-distribuzione delle licenze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Acquisizione di licenze**](acquiring-licenses.md)
</dt> <dt>

[**Uso del modello di eventi Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 