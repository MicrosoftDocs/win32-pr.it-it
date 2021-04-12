---
title: Pagina Web di esempio inclusa con il controllo ActiveX Desktop remoto
description: Una pagina Web di esempio (Default.htm) si trova nella directory in cui è installato Connessione Web Desktop remoto.
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec07ee86dcb5d10dc289e8095c83771ebe9a8b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330404"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>Pagina Web di esempio inclusa con il controllo ActiveX Desktop remoto

Quando si installa il controllo ActiveX Desktop remoto di Connessione Web Desktop remoto, nella directory in cui è installato Connessione Web Desktop remoto viene copiata una pagina Web di esempio (Default.htm). Questa pagina può essere eseguita così com'è o personalizzata per soddisfare le esigenze di un utente o di un'organizzazione.

La pagina Web di esempio deve essere installata in un server Web che esegue Windows Server e Internet Information Server 4,0 o versione successiva. Inoltre, il browser nel computer client deve essere Internet Explorer versione 4,0 o successiva. Per ulteriori informazioni, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

Default.htm è una pagina Web di accesso predefinita che raccoglie le informazioni di connessione dall'utente. La pagina di accesso contiene un campo obbligatorio in cui l'utente immette il nome del server di host sessione Desktop remoto (host sessione Desktop remoto) o del computer remoto a cui connettersi. La pagina di accesso include anche campi facoltativi per le informazioni sulle dimensioni dello schermo e sull'accesso degli utenti, inclusi il nome utente e il dominio.

Dopo aver raccolto i dati dell'utente, Default.htm passati al controllo ActiveX Desktop remoto (Msrdp. ocx) per avviare una sessione di desktop remoto. I passaggi necessari per avviare la sessione sono i seguenti:

1.  Se necessario, Internet Explorer Scarica il file con estensione cab e lo installa nel computer dell'utente.
2.  L'utente immette il nome di dominio completo o l'indirizzo IP del computer remoto nel campo appropriato.

    -   L'utente può facoltativamente specificare le dimensioni dello schermo per la connessione. Se l'utente non specifica le dimensioni dello schermo, la sessione viene aperta in modalità schermo intero se l'utente si trova in un'area di sicurezza URL attendibile. In caso contrario, la sessione verrà aperta in modalità finestra.
    -   L'utente può facoltativamente fornire le informazioni di accesso automatico (nome utente, dominio) per la sessione remota.

3.  Quando l'utente fa clic sul pulsante **Connetti** , Default.htm passa i dati forniti dall'utente come parametri al controllo desktop remoto ActiveX.
4.  Il desktop remoto viene aperto nella finestra del browser o in modalità a schermo intero, come specificato dall'utente.

Quando Default.htm si apre per la prima volta tramite Internet Explorer, viene visualizzata una finestra di dialogo che consente all'utente di scaricare il controllo ActiveX Desktop remoto (Msrdp. ocx). La finestra di dialogo viene visualizzata nelle condizioni seguenti:

-   Il computer che ha eseguito l'accesso alla pagina Web non dispone di un'installazione completa del client di Connessione Web Desktop remoto (o del Servizi Desktop remoto Client avanzato) con supporto Web.
-   La versione installata del file con estensione cab nel computer client è precedente alla versione della pagina Web Default.htm.

La dimensione della sessione Desktop remoto visualizzata nella finestra del browser corrisponde alla dimensione specificata nella pagina Web Default.htm. Per modificare le dimensioni dello schermo, l'utente deve disconnettersi dalla sessione, tornare alla pagina Web Default.htm e modificare le informazioni di connessione. Se non è stata specificata alcuna dimensione dello schermo, la sessione viene aperta nella finestra del browser nella modalità predefinita a schermo intero. A questa risoluzione, il desktop remoto si espande in base alle dimensioni complete della schermata dell'utente e le barre degli strumenti del browser di Internet Explorer e le cornici della finestra non vengono visualizzate. Come per il client Connessione Desktop remoto completo, l'utente può passare dalla modalità a schermo intero a schermo intero e viceversa premendo la combinazione di [tasti di scelta rapida](terminal-services-shortcut-keys.md) per la modalità schermo intero (CTRL + ALT + INTERR).

Per motivi di sicurezza, alcune opzioni disponibili nella gestione connessione Servizi Desktop remoto sono limitate nel controllo ActiveX Desktop remoto a determinate zone di sicurezza URL di Internet Explorer. Per ulteriori informazioni su queste opzioni e sulla specifica di un programma da eseguire al momento della connessione, vedere la pagina [relativa alla sicurezza del client RDP](providing-for-rdp-client-security.md) .

 

 




