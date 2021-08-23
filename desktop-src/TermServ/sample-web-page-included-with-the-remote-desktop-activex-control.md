---
title: Pagina Web di esempio inclusa nel controllo Desktop remoto ActiveX web
description: Una pagina Web di esempio (Default.htm) si trova nella directory in cui Connessione Web Desktop remoto è installato.
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c175bafe1ebde3367c20529a6d76d7933a42f343de56216649735c942105aa65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058539"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>Pagina Web di esempio inclusa nel controllo Desktop remoto ActiveX web

Quando si installa il controllo Desktop remoto ActiveX di Connessione Web Desktop remoto, una pagina Web di esempio (Default.htm) viene copiata nella directory in cui Connessione Web Desktop remoto è installato. Questa pagina può essere eseguita così come è o personalizzata in base alle esigenze di un utente o di un'organizzazione.

La pagina Web di esempio deve essere installata in un server Web che esegue Windows Server e Internet Information Server 4.0 o versione successiva. Inoltre, il browser nel computer client deve essere Internet Explorer versione 4.0 o successiva. Per altre informazioni, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

Default.htm è una pagina Web di accesso predefinita che raccoglie le informazioni di connessione dall'utente. La pagina di accesso contiene un campo obbligatorio in cui l'utente immette il nome del server host sessione Desktop remoto (Host sessione Desktop remoto) o del computer remoto a cui connettersi. La pagina di accesso include anche campi facoltativi per le dimensioni dello schermo e le informazioni di accesso utente, inclusi il nome utente e il dominio.

Dopo aver raccolto i dati utente, Default.htm al controllo Desktop remoto ActiveX (Msrdp.ocx) per avviare una sessione desktop remoto. I passaggi necessari per avviare la sessione sono i seguenti:

1.  Se necessario, Internet Explorer scarica il file .cab e lo installa nel computer dell'utente.
2.  L'utente immette il nome di dominio completo o l'indirizzo IP del computer remoto nel campo appropriato.

    -   L'utente può specificare facoltativamente le dimensioni dello schermo per la connessione. Se l'utente non specifica le dimensioni dello schermo, la sessione viene aperta in modalità schermo intero se l'utente si trova in un'area di sicurezza URL attendibile. In caso contrario, la sessione viene aperta in modalità finestra.
    -   L'utente può facoltativamente fornire informazioni di accesso automatico (nome utente, dominio) per la sessione remota.

3.  Quando l'utente fa clic **sul Connessione,** Default.htm passa i dati forniti dall'utente come parametri al Desktop remoto ActiveX controllo.
4.  Il desktop remoto viene aperto nella finestra del browser o in modalità schermo intero, come specificato dall'utente.

Quando Default.htm si apre per la prima volta usando Internet Explorer, viene visualizzata una finestra di dialogo che consente all'utente di scaricare il controllo Desktop remoto ActiveX (Msrdp.ocx). La finestra di dialogo viene visualizzata nelle condizioni seguenti:

-   Il computer che ha eseguito l'accesso alla pagina Web non dispone di un'installazione completa del client Connessione Web Desktop remoto (o del Servizi Desktop remoto Client avanzato) con supporto Web.
-   La versione installata del file .cab nel computer client è precedente alla versione nella pagina Default.htm web.

Le dimensioni della sessione desktop remoto visualizzata nella finestra del browser sono le dimensioni specificate nella pagina Default.htm pagina Web. Per modificare le dimensioni dello schermo, l'utente deve disconnettersi dalla sessione, tornare alla pagina Default.htm pagina Web e modificare le informazioni di connessione. Se non è stata specificata alcuna dimensione dello schermo, la sessione viene aperta nella finestra del browser in modalità schermo intero predefinita. A questa risoluzione il desktop remoto si espande in modo da corrispondere alle dimensioni complete dello schermo dell'utente e le barre degli strumenti del browser Internet Explorer e le finestre non vengono visualizzate. Come per il client Connessione Desktop remoto completo, l'utente può passare dalla modalità schermo intero [](terminal-services-shortcut-keys.md) alla modalità finestra premendo la combinazione di tasti di scelta rapida modalità schermo intero (CTRL+ALT+INTERR).

Per motivi di sicurezza, alcune opzioni disponibili nel Servizi Desktop remoto Gestione connessioni sono limitate nel controllo Desktop remoto ActiveX a determinate aree Internet Explorer di sicurezza URL. Per altre informazioni su queste opzioni e sulla specifica di un programma da eseguire al momento della connessione, vedere Fornire per [RDP Client Security.](providing-for-rdp-client-security.md)

 

 




