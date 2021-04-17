---
description: Domande frequenti sul broker di autenticazione Web.
ms.assetid: 49ACB2E3-CF57-4D8E-9670-E7C18A06F76A
title: Domande frequenti sul broker di autenticazione Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95942a32bba86f7b2ccb12264cc1a50419b248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529400"
---
# <a name="faq-for-web-authentication-broker"></a>Domande frequenti sul broker di autenticazione Web

Domande frequenti sul broker di autenticazione Web.



| Domanda                                                                                                    | Risposta                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Come è possibile verificare che la pagina https://funzioni con il broker di autenticazione Web?                         | Provare a caricare la pagina in Windows Internet Explorer prima di provarla con il broker di autenticazione Web. Se la pagina Web viene caricata senza errori, il rendering verrà eseguito correttamente anche tramite il broker di autenticazione Web. |
| In caso di errore, i codici di errore verranno visualizzati all'utente?                                         | Quando viene visualizzata una pagina di errore all'utente, il codice di errore sottostante non viene visualizzato. Viene restituito solo all'app. In alternativa, è anche possibile usare i log operativi.                                    |
| Come è possibile trovare altri dettagli sull'errore rilevato?                                                       | Per informazioni dettagliate, usare i log operativi.                                                                                                                                                                             |
| Il contenitore dell'app Single Sign-On (SSO) condivide i cookie con Internet Explorer o altri browser? | No.                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni relative allo sviluppo di pagine Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[App di esempio SDK Web Authentication broker](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
