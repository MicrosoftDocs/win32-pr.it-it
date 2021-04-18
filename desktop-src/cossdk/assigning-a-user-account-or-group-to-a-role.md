---
description: È possibile utilizzare lo strumento di amministrazione Servizi componenti per popolare un ruolo con gli account utente o i gruppi.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Assegnazione di un account utente o di un gruppo a un ruolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53b37c9f0265e02c7abdf74eeaf81bd0b12e3d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305023"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a>Assegnazione di un account utente o di un gruppo a un ruolo

È possibile utilizzare lo strumento di amministrazione Servizi componenti per popolare un ruolo con gli account utente o i gruppi. Il modo migliore per assegnare un account utente a un ruolo consiste nell'assegnare l'account utente a un gruppo e quindi assegnare il gruppo al ruolo. L'utilizzo di gruppi per popolare i ruoli semplifica la gestione di un numero elevato di utenti. Per ulteriori informazioni sulla creazione di gruppi o sull'assegnazione di un account utente a un gruppo, vedere l'argomento relativo a utenti e gruppi locali nella Guida in linea per lo strumento di amministrazione Gestione computer.

> [!Note]  
> Per consentire agli utenti di rete non autenticati di eseguire un'applicazione COM+, i ruoli applicazione devono includere l'utente anonimo. A partire da Windows Server 2003, per impostazione predefinita, l'utente anonimo non è incluso nel gruppo Everyone.

 

Dopo aver assegnato l'account utente al gruppo di Windows appropriato, attenersi alla procedura seguente per assegnare il gruppo di Windows al ruolo.

**Per assegnare un gruppo di Windows a un ruolo di sicurezza**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ che contiene il ruolo a cui si desidera aggiungere l'account utente o il gruppo. Espandere la visualizzazione nell'albero della console fino a quando i ruoli dell'applicazione non sono visibili.

2.  Individuare il ruolo a cui si desidera aggiungere l'account utente o il gruppo.

    > [!Note]  
    > Se il ruolo che si sta cercando non è presente nella cartella **roles** , il ruolo non è stato aggiunto all'applicazione. Prima di poter assegnare gli account utente al ruolo, è necessario aggiungerlo all'applicazione dallo sviluppatore.

     

3.  Fare clic con il pulsante destro del mouse sulla cartella **utenti** del ruolo, scegliere **nuovo**, quindi fare clic su **utente**.

4.  Nella finestra **Seleziona utenti o gruppi** , nel riquadro inferiore, digitare il nome completo dell'utente o del gruppo che si desidera aggiungere. Se non si conosce il nome, fare clic sul pulsante **Avanzate** , quindi fare clic su **trova** per visualizzare un elenco di utenti e gruppi nel dominio selezionato. Selezionare un utente o un gruppo dall'elenco **nome (RDN)** , quindi fare clic su **OK**.

5.  Per aggiungere altri account utente o gruppi, ripetere il passaggio 4.

6.  Al termine dell'aggiunta di account utente e gruppi al ruolo, fare clic su **OK**.

Per ogni account utente o gruppo assegnato al ruolo, viene visualizzata un'icona nella cartella **utenti** . L'appartenenza al nuovo ruolo diventa effettiva al successivo avvio dell'applicazione.

 

 



