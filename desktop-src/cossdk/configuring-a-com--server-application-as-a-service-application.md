---
description: Un'applicazione server COM+ può essere creata come servizio per l'avvio automatico durante l'avvio del sistema o manualmente da attivazioni.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Configurazione di un'applicazione server COM+ come applicazione di servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877497"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a>Configurazione di un'applicazione server COM+ come applicazione di servizio

Un'applicazione server COM+ può essere creata come servizio per l'avvio automatico durante l'avvio del sistema o manualmente da attivazioni. Se il servizio non viene avviato, l'opzione per la gestione degli errori specifica la gravità dell'errore e determina l'azione da intraprendere. È inoltre disponibile l'opzione per configurare un servizio da eseguire come account di sistema locale, nonché l'opzione per l'assegnazione di un account utente specifico per il quale verrà eseguita l'applicazione server COM+. Le dipendenze possono essere selezionate anche da un elenco di servizi registrati nel computer utilizzando Servizi componenti. In questo modo verranno determinati i servizi che devono essere eseguiti prima dell'avvio del servizio.

**Per configurare un'applicazione COM+ per l'esecuzione come servizio**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione server COM+ che si desidera eseguire come servizio.

2.  Fare clic con il pulsante destro del mouse sull'applicazione server COM+, quindi scegliere **Proprietà**.

3.  Nella finestra di dialogo **Proprietà** fare clic sulla scheda **attivazione** .

4.  Nella casella **tipo di attivazione** selezionare la casella di controllo **Esegui applicazione come servizio NT** .

    > [!Note]  
    > La casella di controllo **Esegui applicazione come servizio NT** è abilitata solo per le applicazioni server ed è disabilitata per le applicazioni di libreria.

     

5.  Fare clic sul pulsante **Imposta nuovo servizio** .

6.  Nella casella **tipo di avvio** nella finestra di dialogo **nome servizio** selezionare **automatico** o **manuale**.

7.  Opzionale Per specificare l'azione da intraprendere per un particolare errore, selezionare **Ignora**, **normale**, **grave** o **critico** nella casella **Gestione errori** . Il comportamento associato a ogni opzione è il seguente:

    1.  **Ignore**. Il programma di avvio registra l'errore ma continua l'operazione di avvio.
    2.  **Normale**. L'errore viene registrato, viene visualizzata una finestra di messaggio e il programma di avvio continua l'operazione di avvio.
    3.  **Grave**. L'errore viene registrato e il sistema viene riavviato con l'ultima configurazione corretta nota. Se è l'ultima configurazione ben nota che viene avviata quando viene registrato l'errore, l'operazione di avvio continua.
    4.  **Critica**. L'errore viene registrato e il sistema viene riavviato con l'ultima configurazione corretta nota. Se è l'ultima configurazione corretta nota che viene avviata quando viene registrato l'errore, l'operazione di avvio non riesce.

8.  Opzionale Per impostare altri servizi come dipendenti, selezionare i servizi dipendenti dall'elenco nella casella **dipendenze** .

9.  Opzionale Per indicare che il servizio deve essere autorizzato a interagire con il desktop, selezionare la casella **di controllo Consenti al servizio di interagire con il desktop** .

10. Fare clic su **Crea**.

11. Opzionale Per assegnare il servizio a un account utente:

    1.  Nella scheda **identità** selezionare **questo utente**.
    2.  Per selezionare l'utente, immettere il nome utente nella casella **utente** oppure fare clic sul pulsante **Sfoglia** .
    3.  Immettere la password per l'account utente nella casella **password** .
    4.  Immettere la stessa password nella casella **Conferma password** .

 

 



