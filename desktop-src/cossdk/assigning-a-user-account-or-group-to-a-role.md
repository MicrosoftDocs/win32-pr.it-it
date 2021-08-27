---
description: È possibile usare lo strumento amministrativo Servizi componenti per popolare un ruolo con account utente o gruppi.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Assegnazione di un account utente o di un gruppo a un ruolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0d2883f9aedb5f3a0edf5dc33de54a03767e53a48f2dd8b9b6ea86c3a6211f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047669"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a>Assegnazione di un account utente o di un gruppo a un ruolo

È possibile usare lo strumento amministrativo Servizi componenti per popolare un ruolo con account utente o gruppi. Il modo preferito per assegnare un account utente a un ruolo è assegnare l'account utente a un gruppo e quindi assegnare il gruppo al ruolo. L'uso di gruppi per popolare i ruoli semplifica la gestione di un numero elevato di utenti. Nella Guida in linea dello strumento amministrativo Gestione computer vedere l'argomento "Utenti e gruppi locali" per altre informazioni sulla creazione di gruppi o sull'assegnazione di un account utente a un gruppo.

> [!Note]  
> Per consentire agli utenti di rete non autenticati di eseguire un'applicazione COM+, i ruoli applicazione devono includere l'utente anonimo. A partire Windows Server 2003, per impostazione predefinita, l'utente anonimo non è incluso nel gruppo Everyone.

 

Dopo aver assegnato l'account utente al gruppo di Windows appropriato, seguire questa procedura per assegnare il gruppo Windows al ruolo.

**Per assegnare un Windows a un ruolo di sicurezza**

1.  Nell'albero della console dello strumento amministrativo Servizi componenti individuare l'applicazione COM+ che contiene il ruolo a cui si vuole aggiungere l'account utente o il gruppo. Espandere la visualizzazione nell'albero della console fino a quando i ruoli dell'applicazione non sono visibili.

2.  Individuare il ruolo a cui si vuole aggiungere l'account utente o il gruppo.

    > [!Note]  
    > Se il ruolo che si sta cercando non si trova nella **cartella Ruoli,** il ruolo non è stato aggiunto all'applicazione. Deve essere aggiunto all'applicazione dallo sviluppatore prima di poter assegnare gli account utente al ruolo.

     

3.  Fare clic con il pulsante **destro del mouse** sulla cartella Users nel ruolo, scegliere **Nuovo** e quindi fare clic su **Utente**.

4.  Nel riquadro **inferiore della** finestra Seleziona utenti o gruppi digitare il nome completo dell'utente o del gruppo da aggiungere. Se non si conosce il  nome, fare  clic sul pulsante Avanzate e quindi su Trova per visualizzare un elenco di utenti e gruppi nel dominio selezionato. Selezionare un utente o un gruppo **dall'elenco Nome (RDN)** e fare clic su **OK.**

5.  Per aggiungere altri account utente o gruppi, ripetere il passaggio 4.

6.  Al termine dell'aggiunta di account utente e gruppi al ruolo, fare clic su **OK.**

Per ogni account utente o gruppo assegnato al ruolo, nella **cartella Utenti** viene visualizzata un'icona. La nuova appartenenza al ruolo viene impostata al successivo avvio dell'applicazione.

 

 



