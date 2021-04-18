---
description: Creazione di una nuova applicazione COM+
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Creazione di una nuova applicazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305224"
---
# <a name="creating-a-new-com-application"></a>Creazione di una nuova applicazione COM+

Per la creazione di una nuova applicazione COM+ sono necessari due passaggi di base, come indicato di seguito:

-   Creazione di un'applicazione COM+ vuota (descritta di seguito).
-   Aggiunta di componenti all'applicazione. Vedere [installazione di nuovi componenti](installing-new-components.md) e [importazione di componenti](importing-components.md).

**Per creare un'applicazione COM+ vuota**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti selezionare il computer in cui si desidera creare un'applicazione.

2.  Selezionare la cartella **applicazioni com+** per il computer.

3.  Scegliere **nuovo** dal menu **azione** , quindi fare clic su **applicazione**. È anche possibile fare clic con il pulsante destro del mouse sulla cartella **applicazioni com+** , scegliere **nuovo**, quindi fare clic su **applicazione**.

4.  Nella pagina **iniziale** dell'installazione guidata dell'applicazione com+, fare clic su **Avanti**, quindi nella finestra di dialogo **Installa o crea una nuova applicazione** fare clic su **Crea un'applicazione vuota**.

5.  Nella casella specificata digitare un nome per la nuova applicazione. Si noti che non è possibile utilizzare i seguenti caratteri speciali in un nome di applicazione: \\ ,/, ~,!, @, \# ,%, ^, &, \* , (,), \| ,}, {, \] , \[ ,', ", >, <,.,?,: e;.) In **tipo di attivazione** fare clic su applicazione **libreria** o **applicazione server**. Fare clic su **Avanti**.

    > [!Note]  
    > Un'applicazione server viene eseguita in un proprio processo. Le applicazioni server possono supportare tutti i servizi COM+. Un'applicazione di libreria viene eseguita nel processo del client che la crea. Le applicazioni di libreria possono usare la sicurezza basata sui ruoli, ma non supportano l'accesso remoto o i componenti in coda.

     

6.  Nella finestra di dialogo **Imposta identità applicazione** scegliere un'identità con cui eseguire l'applicazione. Se si seleziona **questo utente**, digitare il nome utente e la password. È inoltre necessario digitare nuovamente la password nella casella **Conferma password** . Fare clic su **Avanti**. La selezione predefinita per l'identità dell'applicazione è **utente interattivo**. L'utente interattivo è l'utente connesso al computer server in un determinato momento. È possibile selezionare un utente diverso selezionando **l'utente** e immettendo un utente o un gruppo specifico.

    > [!Note]  
    > La finestra di dialogo **Imposta identità applicazione** viene visualizzata solo se è stata selezionata l'opzione **applicazione server** per il tipo di attivazione della nuova applicazione nella finestra di dialogo precedente della procedura guidata di installazione dell'applicazione com. La proprietà Identity non viene utilizzata per le applicazioni di libreria.

     

7.  Nella finestra di dialogo **Aggiungi ruoli applicazione** aggiungere i ruoli che si desidera associare all'applicazione. Per impostazione predefinita, viene definito solo il ruolo **CreatorOwner** . Per informazioni sui ruoli, vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).

8.  Nella finestra di dialogo **Aggiungi utenti ai ruoli** , popolare ogni ruolo creato nell'ultimo passaggio con gli utenti, i gruppi o le entità di sicurezza predefinite a cui si desidera concedere i privilegi associati a tale ruolo. Per impostazione predefinita, l'utente interattivo viene inserito nel ruolo **CreatorOwner** .

9.  Fare clic su **Fine**.

La nuova applicazione verrà ora visualizzata nella cartella **applicazioni com+** nell'albero della console dello strumento di amministrazione Servizi componenti.

> [!Note]  
> A partire da Windows Server 2003, i controlli di accesso sono abilitati per impostazione predefinita quando si crea un'applicazione COM+. Nelle versioni precedenti, i controlli di accesso erano disabilitati per impostazione predefinita a livello di applicazione. Il risultato è che, per impostazione predefinita, l'accesso a un'applicazione COM+ è consentito solo agli utenti inclusi nei ruoli associati all'applicazione. (Vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)). In alternativa, è possibile consentire l'accesso a tutti gli utenti disabilitando i controlli di accesso in un'applicazione COM+. Vedere [Abilitazione dei controlli di accesso per un'applicazione](enabling-access-checks-for-an-application.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Copia di componenti](copying-components.md)
</dt> <dt>

[Eliminazione di un'applicazione COM+](deleting-a-com--application.md)
</dt> <dt>

[Importazione di componenti](importing-components.md)
</dt> <dt>

[Installazione di nuovi componenti](installing-new-components.md)
</dt> <dt>

[Spostamento dei componenti](moving-components.md)
</dt> <dt>

[Rimozione di un componente da un'applicazione COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



