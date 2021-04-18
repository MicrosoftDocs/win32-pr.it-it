---
description: Se un utente modifica i privilegi o se i ruoli vengono aggiunti a un'applicazione, è possibile spostare un account da un ruolo a un altro.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Rimozione di un account utente o di un gruppo da un ruolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305211"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a>Rimozione di un account utente o di un gruppo da un ruolo

Se i privilegi di un utente cambiano o se i ruoli vengono aggiunti a un'applicazione, è possibile spostare un account da un ruolo a un altro. Per spostare un account utente o un gruppo di utenti da un ruolo a un altro, è necessario rimuovere l'account utente o il gruppo dal ruolo corrente e quindi assegnarlo al nuovo ruolo.

**Per spostare un account utente o un gruppo da un ruolo a un altro**

1.  Rimuovere l'account utente o il gruppo dal ruolo a cui non deve più appartenere, come indicato di seguito:

    1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il ruolo a cui si è interessati. Espandere la visualizzazione nell'albero della console fino a quando non saranno visibili gli utenti per il ruolo.

    2.  Fare clic con il pulsante destro del mouse sull'account utente o sul gruppo che si desidera rimuovere, quindi scegliere **Elimina**.

    3.  Quando richiesto dalla finestra di dialogo **Conferma eliminazione elemento** , fare clic su **Sì** per eliminare l'account utente o il gruppo.

    L'account utente o il gruppo rimosso dal ruolo non viene più visualizzato nella cartella **utenti** .

2.  Assegnare l'account utente o il gruppo rimosso ai ruoli a cui deve essere assegnato l'utente o il gruppo, come indicato di seguito:

    1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il ruolo a cui si desidera aggiungere l'account utente o il gruppo. Espandere la visualizzazione nell'albero della console fino a quando i ruoli dell'applicazione non sono visibili.

    2.  Individuare il ruolo a cui si desidera aggiungere l'account utente o il gruppo.

        > [!Note]  
        > Se il ruolo che si sta cercando non è presente nella cartella **roles** , il ruolo non è stato aggiunto all'applicazione. Prima di poter assegnare gli account utente al ruolo, è necessario aggiungerlo all'applicazione dallo sviluppatore.

         

    3.  Fare clic con il pulsante destro del mouse sulla cartella **utenti** del ruolo, scegliere **nuovo**, quindi fare clic su **utente**.

    4.  Nella finestra **Seleziona utenti o gruppi** , nel riquadro inferiore, digitare il nome completo dell'utente o del gruppo che si desidera aggiungere. Se non si conosce il nome, fare clic sul pulsante **Avanzate** , quindi fare clic su **trova** per visualizzare un elenco di utenti e gruppi nel dominio selezionato. Selezionare un utente o un gruppo dall'elenco **nome (RDN)** e fare clic su **OK**.

    5.  Al termine dell'aggiunta dell'account utente o del gruppo al ruolo, fare clic su **OK**.

    Per ogni account utente o gruppo assegnato al ruolo, viene visualizzata un'icona nella cartella **utenti** .

L'appartenenza al ruolo modificata per l'account utente o il gruppo diventa effettiva al successivo avvio dell'applicazione.

 

 



