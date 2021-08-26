---
title: Configurazione del servizio dei nomi
description: A partire da Windows 2000, quando si installa Windows SDK, il programma di installazione seleziona automaticamente Microsoft Locator come provider di servizi dei nomi. È possibile modificare il provider di servizi dei nomi tramite Pannello di controllo.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84450f4408ac0e90be04cfff7d1cbc92890cde4434969431a986e9cda378ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022441"
---
# <a name="configuring-the-name-service"></a>Configurazione del servizio dei nomi

A partire da Windows 2000, quando si installa Windows SDK, il programma di installazione seleziona automaticamente Microsoft Locator come provider di servizi dei nomi. È possibile modificare il provider di servizi dei nomi tramite Pannello di controllo.

Il computer host che esegue nsid funge da gateway per il servizio directory delle celle DCE, passando le chiamate di funzione NSI tra i computer che eseguono i sistemi operativi Microsoft e i computer DCE. Un indirizzo di rete può contenere fino a 80 caratteri, ad esempio 11.1.9.169 è un indirizzo valido.

> [!Note]  
> Per configurare DCE CDS come provider di servizi di nome, è necessario disporre del prodotto DCE CDS di Digital Equipment Corporation. Per informazioni su DCE CDS, vedere la documentazione fornita da Digital Equipment Corporation.

 

**Per riconfigurare il provider di servizi dei nomi**

1.  In Pannello di controllo fare clic **sull'icona Connessioni di** rete. Verrà **visualizzata la finestra Connessioni** di rete.
2.  Selezionare la connessione di rete da configurare, fare clic con il pulsante destro del mouse e **scegliere Proprietà** dal menu di scelta rapida. Verrà **visualizzata la finestra di dialogo** Proprietà connessione.
3.  Nella finestra **di dialogo Proprietà** connessione selezionare Client per reti Microsoft **e** fare clic sul **pulsante** Proprietà. Viene **visualizzata la finestra di dialogo Proprietà client per rete Microsoft.**
4.  Nella finestra **di dialogo Proprietà client** per rete Microsoft aprire l'elenco a discesa **Provider** di servizi dei nomi e selezionare un provider di nomi dall'elenco.
    1.  Quando si seleziona Microsoft Locator, fare clic su OK. Il processo di configurazione viene quindi completato.
    2.  Quando si seleziona DCE Cell Directory Service, nella casella **Network Address** (Indirizzo di rete) digitare il nome del computer host che esegue il daemon NSI (nsid) e quindi fare clic su OK.

**Per riconfigurare il provider di servizi dei nomi per Windows 2000**

1.  Nella Pannello di controllo fare clic **sull'icona** Rete.

    Verrà **visualizzata la** finestra di dialogo Rete .

2.  Nella finestra **di dialogo** Rete fare clic su **Configura**.
3.  **Nell'elenco NetworkSoftware** selezionare **Configurazione RPC**.

    Verrà visualizzata la finestra di dialogo Configurazione provider di servizi dei nomi **RPC.**

4.  Nella finestra **di dialogo Configurazione provider di servizi** dei nomi RPC selezionare un provider di servizi nomi dall'elenco.
    1.  Quando si seleziona Microsoft Locator, fare clic su OK. Il processo di configurazione viene quindi completato.
    2.  Quando si seleziona DCE Cell Directory Service, nella casella **Network Address** (Indirizzo di rete) digitare il nome del computer host che esegue il daemon NSI (nsid) e quindi fare clic su OK.

 

 




