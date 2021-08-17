---
description: L'autenticazione dimostra chi si è.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Autenticazione per le pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46a063cdd63631f84aa21980f89a143b3d1e9b42af020799d0f9f1bb7502b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141439"
---
# <a name="authentication-for-web-pages"></a>Autenticazione per le pagine Web

L'autenticazione dimostra chi si è.

**Obiettivo:** Per fare in modo che il broker di autenticazione Web venga visualizzato come parte dell'app.

## <a name="prerequisites"></a>Prerequisiti

Nessuno

**Tempo di completamento:** 15 minuti.

## <a name="instructions"></a>Istruzioni

### <a name="1-getting-started"></a>1. Guida introduttiva

Avviare il file di installazione per installare un sito Web Contoso in Internet Information Services 8 nel computer locale per ospitare i file HTML e CSS di esempio.

1.  I file HTML e CSS di esempio verranno installati nella directory dei file di programma in Microsoft \\ Contoso.
2.  Inoltre, un'app "Fabrikam Social" Windows Store verrà decomballata sul desktop.

### <a name="2-getting-familiar"></a>2. Acquisire familiarità

Per avere un'occhiata all'aspetto delle pagine di esempio in Web Authentication Broker, aprire il file di soluzione Fabrikam Social Visual Studio 11 nella cartella "Fabrikam Social" sul desktop.

1.  Eseguire l'applicazione e premere "Avvia" per visualizzare le pagine di esempio in Web Authentication Broker.
2.  L'app può essere ridimensionata su un lato o attivata condividendo alcuni dati con l'applicazione.

### <a name="3-authentication"></a>3. Autenticazione

Quando l'API di autenticazione Web viene richiamata dall'app sottostante per connettersi al provider, "Contoso Social", viene visualizzata la pagina di accesso. Questa pagina è progettata per essere ottimale in un'esperienza di accesso veloce e fluida. Fornisce anche punti di ingresso ad altre azioni comuni dell'utente, ad esempio il recupero dei dettagli della password, l'immissione di un account e la lettura delle istruzioni sulla privacy e i termini e le condizioni completati nel browser. ![Pagina di accesso contoso](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a>Riepilogo e passaggi successivi

Esercitazione [di riepilogo per l'autenticazione di pagine Web](tutorial-for-authenticating-web-pages.md)

Autorizzazione [successiva per le pagine Web](authorization-for-web-pages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni relative allo sviluppo di pagine Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[App di esempio di Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
