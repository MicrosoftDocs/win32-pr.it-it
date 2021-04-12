---
title: Esecuzione di query per ottenere informazioni semplici sui diritti
description: Esecuzione di query per ottenere informazioni semplici sui diritti
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- Windows Media Format SDK, esecuzione di query per diritti semplici
- Windows Media Format SDK, semplici query sui diritti
- Digital Rights Management (DRM), esecuzione di query per diritti semplici
- DRM (Digital Rights Management), esecuzione di query per diritti semplici
- Digital Rights Management (DRM), semplici query sui diritti
- DRM (Digital Rights Management), semplici query sui diritti
- API estese del client DRM, esecuzione di query per diritti semplici
- API estese del client, esecuzione di query per diritti semplici
- API estese del client DRM, query con diritti semplici
- API estese client, semplici query con diritti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d65929a369ad86753a0e549eb929ad344cdc368
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396011"
---
# <a name="querying-for-simple-rights-information"></a>Esecuzione di query per ottenere informazioni semplici sui diritti

Le API estese del client Windows Media DRM consentono di ottenere rapidamente informazioni semplici sul fatto che sia possibile accedere al contenuto protetto per varie azioni.

Il metodo [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) può essere usato per determinare rapidamente se un'azione è consentita da una licenza nell'archivio licenze locale. **QueryActionAllowed** è stato ottimizzato in modo da essere molto più veloce rispetto alle query per ottenere informazioni simili utilizzando gli oggetti di Windows Media Format SDK. Tuttavia, questo tipo di query aggrega le licenze nell'archivio licenze locale e deve essere utilizzato solo per le funzionalità semplici, ad esempio per gli elementi dell'interfaccia utente, ad esempio per la visualizzazione di un indicatore di autorizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Recupero di informazioni dalle licenze nell'archivio licenze locale**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




