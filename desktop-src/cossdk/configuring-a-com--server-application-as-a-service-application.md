---
description: Un'applicazione server COM+ può essere creata come servizio per l'avvio automatico durante l'avvio del sistema o manualmente dalle attivazioni.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Configurazione di un'applicazione server COM+ come applicazione di servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ad6ec0af4ddf6d7ac7bf703209af2412e1ca4e128a942e7e1ecd089b69e278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991191"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a>Configurazione di un'applicazione server COM+ come applicazione di servizio

Un'applicazione server COM+ può essere creata come servizio per l'avvio automatico durante l'avvio del sistema o manualmente dalle attivazioni. Se l'avvio del servizio non riesce, l'opzione per la gestione degli errori specifica la gravità dell'errore e determina l'azione da eseguire. È disponibile anche l'opzione per configurare un servizio per l'esecuzione come account di sistema locale, nonché l'opzione per assegnare un account utente specifico per il quale verrà eseguita l'applicazione server COM+. Le dipendenze possono essere selezionate anche da un elenco di servizi registrati nel computer tramite Servizi componenti. Ciò determinerà quali servizi devono essere eseguiti prima dell'avvio del servizio.

**Per configurare un'applicazione COM+ per l'esecuzione come servizio**

1.  Nell'albero della console dello strumento amministrativo Servizi componenti individuare l'applicazione server COM+ che si vuole eseguire come servizio.

2.  Fare clic con il pulsante destro del mouse sull'applicazione server COM+ e quindi scegliere **Proprietà**.

3.  Nella finestra **di dialogo** Proprietà fare clic sulla **scheda** Attivazione.

4.  Nella casella **Tipo di attivazione** selezionare la casella di controllo Esegui applicazione come servizio **NT.**

    > [!Note]  
    > La **casella di controllo Esegui applicazione come servizio NT** è abilitata solo per le applicazioni server ed è disabilitata per le applicazioni di libreria.

     

5.  Fare clic **sul pulsante Configura nuovo** servizio.

6.  Nella casella **Tipo di** avvio della finestra di **dialogo Nome** servizio selezionare **Automatico** o **Manuale**.

7.  (Facoltativo) Per specificare l'azione da eseguire per un determinato errore, selezionare **Ignora** **,** Normale **,** Grave o **Critico** nella casella **Gestione** errori . Il comportamento associato a ogni opzione è il seguente:

    1.  **Ignore**. Il programma di avvio registra l'errore ma continua l'operazione di avvio.
    2.  **Normale**. L'errore viene registrato, viene visualizzata una finestra di messaggio e il programma di avvio continua l'operazione di avvio.
    3.  **Grave**. L'errore viene registrato e il sistema viene riavviato con l'ultima configurazione valida nota. Se è l'ultima configurazione valida nota che viene avviata quando viene registrato l'errore, l'operazione di avvio continua.
    4.  **Critica**. L'errore viene registrato e il sistema viene riavviato con l'ultima configurazione valida nota. Se è l'ultima configurazione valida nota che viene avviata quando viene registrato l'errore, l'operazione di avvio ha esito negativo.

8.  (Facoltativo) Per impostare altri servizi come dipendenti, selezionare i servizi dipendenti dall'elenco nella **casella** Dipendenze .

9.  (Facoltativo) Per indicare che al servizio deve essere consentito l'interazione con il desktop, selezionare la casella di controllo Consenti al servizio **di interagire con il desktop.**

10. Fare clic su **Crea**.

11. (Facoltativo) Per assegnare il servizio a un account utente:

    1.  Nella scheda **Identity** (Identità) selezionare **This user (Questo utente).**
    2.  Per selezionare l'utente, immettere il nome utente nella **casella Utente** o fare clic sul **pulsante** Sfoglia.
    3.  Immettere la password per l'account utente nella **casella Password** .
    4.  Immettere la stessa password nella casella **Conferma** password .

 

 



