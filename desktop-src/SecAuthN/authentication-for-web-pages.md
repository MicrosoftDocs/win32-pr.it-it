---
description: L'autenticazione sta dimostrando chi sei.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Autenticazione per le pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7c7bd37334f345ae16074c050b6b06c5fd644f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968142"
---
# <a name="authentication-for-web-pages"></a>Autenticazione per le pagine Web

L'autenticazione sta dimostrando chi sei.

**Obiettivo:** Per far apparire il broker di autenticazione Web come parte dell'app.

## <a name="prerequisites"></a>Prerequisiti

nessuno

**Tempo necessario per il completamento:** 15 minuti.

## <a name="instructions"></a>Istruzioni

### <a name="1-getting-started"></a>1. Guida introduttiva

Avviare il file di installazione per installare un sito Web contoso in Internet Information Services 8 nel computer locale per ospitare i file HTML e CSS di esempio.

1.  I file HTML e CSS di esempio verranno installati nella directory programmi in Microsoft \\ contoso.
2.  Inoltre, un'app di Windows Store "Fabrikam social" verrà disimballata sul desktop.

### <a name="2-getting-familiar"></a>2. acquisire familiarità

Per avere un'idea dell'aspetto delle pagine di esempio nel gestore di autenticazione Web, aprire il file di soluzione di Visual Studio 11 per Fabrikam social Visual Studio 11 nella cartella "Fabrikam social" sul desktop.

1.  Eseguire l'applicazione e fare clic su "Launch" (Avvia) per visualizzare le pagine di esempio nel gestore di autenticazione Web.
2.  L'app può essere ridimensionata in un lato o attivata condividendo alcuni dati nell'applicazione.

### <a name="3-authentication"></a>3. autenticazione

Quando l'API di autenticazione Web viene richiamata dall'app sottostante per connettersi al provider, ovvero "contoso social", viene visualizzata la pagina di accesso. Questa pagina è progettata per essere ottimale in un'esperienza di accesso veloce e fluida. Fornisce inoltre punti di ingresso ad altre azioni utente comuni, ad esempio il recupero dei dettagli della password, l'iscrizione a un account e la lettura di istruzioni sulla privacy e i termini e le condizioni completati nel browser. ![pagina di accesso di contoso](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a>Riepilogo e passaggi successivi

[Esercitazione di riepilogo per l'autenticazione di pagine Web](tutorial-for-authenticating-web-pages.md)

[Autorizzazione successiva per le pagine Web](authorization-for-web-pages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni relative allo sviluppo di pagine Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[App di esempio SDK Web Authentication broker](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
