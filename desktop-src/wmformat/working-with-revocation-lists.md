---
title: Utilizzo degli elenchi di revoche
description: Utilizzo degli elenchi di revoche
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- Windows Media Format SDK, elenchi di revoche
- ASF (Advanced Systems Format), elenchi di revoche
- ASF (Advanced Systems Format), elenchi di revoche
- elenchi di revoche
- Digital Rights Management (DRM), elenchi di revoche
- DRM (Digital Rights Management), elenchi di revoche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f4eca82dd82c9225406a85034ff2a6df227fce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516579"
---
# <a name="working-with-revocation-lists"></a>Utilizzo degli elenchi di revoche

Per rispondere alle violazioni della sicurezza e garantire che le applicazioni dei giocatori note siano interrotte o compromesse non possano riprodurre o usare file protetti, ogni licenza rilasciata contiene un elenco di revoche. Un elenco di revoche contiene i certificati dell'applicazione di tutte le applicazioni del lettore note come interrotte o danneggiate. Quando viene ricevuta una nuova licenza, il componente DRM dell'applicazione Player verifica la presenza di un elenco di revoche. Se ne viene trovato uno più recente rispetto a quello attualmente presente nel computer, viene archiviato l'elenco più recente. Alla successiva riproduzione di un file ASF protetto da parte del consumer, il componente DRM confronta l'applicazione Player con l'elenco di revoche. Se l'applicazione del lettore viene revocata, il componente DRM Invia un messaggio di errore all'applicazione.

Le applicazioni Player possono ricevere un messaggio di errore di revoca negli scenari seguenti:

-   Il messaggio di errore viene ricevuto dopo che l'applicazione chiama il metodo [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) per un file protetto. La chiamata ha esito negativo con il codice **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revocato, fornito alla funzione di callback **OnStatus** con \_ \_ lo stato della licenza WMT Acquire. Se questo codice **HRESULT** viene ignorato, gli errori continueranno a verificarsi.
-   Il messaggio di errore viene ricevuto quando l'applicazione crea il lettore abilitato per DRM e chiama il metodo [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) per un file protetto. La chiamata ha esito negativo con il codice **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revocato, fornito al metodo [**IWMSTATUSCALLBACK:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback con WMT \_ opened status. Quando un'applicazione lettore riceve questo messaggio di errore, l'applicazione deve informare gli utenti finali e fornire un modo per ripristinare le funzionalità al lettore. Ad esempio, l'applicazione può aprire un URL in cui gli utenti finali possono scaricare un aggiornamento per l'applicazione compromessa.

**Nota** Il DRM non è supportato dalla versione basata su x64 di questo SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Gestione degli eventi di acquisizione delle licenze**](handling-license-acquisition-events.md)
</dt> </dl>

 

 




