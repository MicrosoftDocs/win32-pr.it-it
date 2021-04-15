---
title: Configurazione del servizio nome
description: A partire da Windows 2000, quando si installa il Windows SDK, il programma di installazione seleziona automaticamente Microsoft Locator come provider di servizi nome. È possibile modificare il nome del provider di servizi tramite il pannello di controllo.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471230"
---
# <a name="configuring-the-name-service"></a>Configurazione del servizio nome

A partire da Windows 2000, quando si installa il Windows SDK, il programma di installazione seleziona automaticamente Microsoft Locator come provider di servizi nome. È possibile modificare il nome del provider di servizi tramite il pannello di controllo.

Il computer host che esegue NSID funge da gateway per il servizio directory di celle DCE, passando le chiamate di funzione NSI tra computer che eseguono sistemi operativi Microsoft e computer DCE. Un indirizzo di rete può essere composto da un massimo di 80 caratteri, ad esempio 11.1.9.169 è un indirizzo valido.

> [!Note]  
> Per configurare i CD DCE come provider di servizi di nome, è necessario disporre del prodotto CDS digitale Digital Equipment Corporation. Per informazioni sui CD DCE, vedere la documentazione fornita da Digital Equipment Corporation.

 

**Per riconfigurare il provider di servizi dei nomi**

1.  Nel pannello di controllo fare clic sull'icona **connessioni di rete** . Verrà visualizzata la finestra **connessioni di rete** .
2.  Selezionare la connessione di rete da configurare, fare clic con il pulsante destro del mouse e scegliere **Proprietà** dal menu di scelta rapida. Verrà visualizzata la finestra di dialogo **Proprietà connessione** .
3.  Nella finestra di dialogo **Proprietà connessione** selezionare **client per reti Microsoft** e quindi fare clic sul pulsante **proprietà** . Verrà visualizzata la finestra **di dialogo client per proprietà rete Microsoft** .
4.  Nella finestra di dialogo **client for Microsoft Network Properties** aprire l'elenco a discesa **Nome provider di servizi** e selezionare un provider di nomi nell'elenco.
    1.  Quando si seleziona Microsoft Locator, fare clic su OK. Il processo di configurazione viene quindi completato.
    2.  Quando si seleziona il servizio directory celle DCE, nella casella **indirizzo di rete** Digitare il nome del computer host che esegue il daemon NSI (NSID), quindi fare clic su OK.

**Per riconfigurare il provider di servizi dei nomi per Windows 2000**

1.  Nel pannello di controllo fare clic sull'icona della **rete** .

    Verrà visualizzata la finestra di dialogo **rete** .

2.  Nella finestra di dialogo **rete** fare clic su **Configura**.
3.  Nell'elenco **NetworkSoftware** selezionare **configurazione RPC**.

    Verrà visualizzata la finestra di dialogo **Configurazione provider di servizi nome RPC** .

4.  Nella finestra di dialogo **Configurazione provider di servizi nome RPC** selezionare un provider di servizi di nome dall'elenco.
    1.  Quando si seleziona Microsoft Locator, fare clic su OK. Il processo di configurazione viene quindi completato.
    2.  Quando si seleziona il servizio directory celle DCE, nella casella **indirizzo di rete** Digitare il nome del computer host che esegue il daemon NSI (NSID), quindi fare clic su OK.

 

 




