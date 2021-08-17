---
description: L'autorizzazione imposta le risorse a cui si ha accesso.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorizzazione per le pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4f64cbbf3dd9ac38a13719cd8835a198f1fbb3b522e8ac368ffaf4e759fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141329"
---
# <a name="authorization-for-web-pages"></a>Autorizzazione per le pagine Web

L'autorizzazione imposta le risorse a cui si ha accesso.

**Obiettivo:** Per consentire agli utenti di accedere all'app.

## <a name="prerequisites"></a>Prerequisiti

Nessuno

**Tempo di completamento:** 2 minuti.

## <a name="instructions"></a>Istruzioni

### <a name="1-authorization"></a>1. Autorizzazione

Quando l'utente immette le proprie credenziali e fa clic sul pulsante Accesso, viene visualizzata la pagina delle autorizzazioni. Questa pagina consente agli utenti di controllare le autorizzazioni granulari per concedere all'app l'accesso ai dati di Contoso. ![Pagina delle autorizzazioni contoso](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a>2. Come usare l'esempio

È necessario conoscere i file HTML e CSS seguenti.

1.  I file HTML seguenti corrispondono alle due pagine nel flusso di autorizzazione Web
    -   WebAuthLogin.html: codice HTML di esempio per la pagina di accesso
    -   WebAuthPermissions.html: codice HTML di esempio per la pagina delle autorizzazioni
2.  I file CSS contengono Windows 8 per creare una pagina Web dell Windows app Store.
    -   ui-light.css: derivato dal foglio di stile di base per Windows 8 controlli.
    -   ui-webauth.css: fornisce uno stile incrementale per ottimizzare il layout per le pagine di autenticazione Web.
    -   theme-colors.css: fornisce lo stile incrementale per eseguire l'override dei colori accentati predefiniti dei controlli con il colore del marchio del provider.

## <a name="summary-and-next-steps"></a>Riepilogo e passaggi successivi

Esercitazione [di riepilogo per l'autenticazione di pagine Web](tutorial-for-authenticating-web-pages.md)

Procedure [consigliate successive per la progettazione di pagine Web di autenticazione](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni relative allo sviluppo di pagine Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[App di esempio di Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
