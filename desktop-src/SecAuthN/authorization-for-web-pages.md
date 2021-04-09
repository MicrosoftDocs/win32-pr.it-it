---
description: Autorizzazione consente di impostare le risorse a cui si ha accesso.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorizzazione per le pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c26e9bc8333d74d18989c5c581cc54054a29ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880178"
---
# <a name="authorization-for-web-pages"></a>Autorizzazione per le pagine Web

Autorizzazione consente di impostare le risorse a cui si ha accesso.

**Obiettivo:** Per consentire agli utenti di accedere all'app.

## <a name="prerequisites"></a>Prerequisiti

nessuno

**Tempo necessario per il completamento:** 2 minuti.

## <a name="instructions"></a>Istruzioni

### <a name="1-authorization"></a>1. autorizzazione

Quando l'utente immette le credenziali e fa clic sul pulsante di accesso, viene visualizzata la pagina autorizzazioni. Questa pagina è ideale per consentire agli utenti di controllare le autorizzazioni granulari per concedere all'app l'accesso ai dati di contoso. ![pagina autorizzazioni di contoso](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a>2. come utilizzare l'esempio

È necessario conoscere i seguenti file HTML e CSS.

1.  I file HTML seguenti corrispondono alle due pagine del flusso di autorizzazione Web
    -   WebAuthLogin.html-HTML di esempio per la pagina di accesso
    -   WebAuthPermissions.html-HTML di esempio per la pagina autorizzazioni
2.  I file CSS contengono gli stili di Windows 8 per facilitare la creazione di una pagina Web dell'app di Windows Store.
    -   UI-Light. CSS: è stato derivato dal foglio di stile di base per i controlli di Windows 8.
    -   UI-WebAuth. CSS: fornisce lo stile incrementale per l'ottimizzazione del layout per le pagine di autenticazione Web.
    -   Theme-Colors. CSS: fornisce lo stile incrementale per l'override dei colori accentati predefiniti dei controlli con il colore del marchio del provider.

## <a name="summary-and-next-steps"></a>Riepilogo e passaggi successivi

[Esercitazione di riepilogo per l'autenticazione di pagine Web](tutorial-for-authenticating-web-pages.md)

[Procedure consigliate successive per la progettazione di pagine Web di autenticazione](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni relative allo sviluppo di pagine Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[App di esempio SDK Web Authentication broker](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
