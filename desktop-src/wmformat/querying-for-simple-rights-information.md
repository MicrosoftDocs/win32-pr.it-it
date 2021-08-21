---
title: Esecuzione di query per informazioni semplici sui diritti
description: Esecuzione di query per informazioni semplici sui diritti
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- Windows Media Format SDK, esecuzione di query per diritti semplici
- Windows Media Format SDK, query semplici sui diritti
- DRM (Digital Rights Management), query per diritti semplici
- DRM (Digital Rights Management), query per diritti semplici
- DRM (Digital Rights Management), query semplici sui diritti
- DRM (Digital Rights Management),query semplici sui diritti
- API estese del client DRM, esecuzione di query per diritti semplici
- API estese client, esecuzione di query per diritti semplici
- API estese del client DRM, query semplici sui diritti
- API client estese, query semplici sui diritti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0686616bbc700c51a005c3e1e63eed889c42965aaebbba232fcf90b9cce26987
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027369"
---
# <a name="querying-for-simple-rights-information"></a>Esecuzione di query per informazioni semplici sui diritti

Le WINDOWS Client Extended di Media DRM consentono di ottenere rapidamente informazioni semplici sull'accesso al contenuto protetto per varie azioni.

Il [**metodo IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) può essere usato per determinare rapidamente se un'azione è consentita da una licenza nell'archivio licenze locale. **QueryActionAllowed è** stato ottimizzato per essere molto più veloce rispetto alle query per ottenere informazioni simili usando gli oggetti di Windows Media Format SDK. Tuttavia, questo tipo di query aggrega le licenze nell'archivio licenze locale e deve essere usato solo per funzionalità semplici, ad esempio potrebbe essere necessario per gli elementi dell'interfaccia utente, ad esempio la visualizzazione di un indicatore di autorizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Recupero di informazioni dalle licenze nell'archivio licenze locale**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




