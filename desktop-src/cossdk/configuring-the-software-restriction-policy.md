---
description: Configurazione dei criteri di restrizione software
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Configurazione dei criteri di restrizione software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049261"
---
# <a name="configuring-the-software-restriction-policy"></a>Configurazione dei criteri di restrizione software

Quando si impostano in modo esplicito i livelli di attendibilità dei criteri di restrizione software di un'applicazione COM+, viene eseguito l'override delle impostazioni predefinite di a livello. Questa operazione è spesso necessaria per le applicazioni server COM+ perché il livello di attendibilità a livello è impostato sullo stesso per tutte le applicazioni server (perché tutti vengono eseguiti nello stesso file, dllhost.exe). Tuttavia, quando si imposta il livello di attendibilità dei criteri di restrizione software di un'applicazione libreria COM+, si influisce sulla configurazione di a livello per l'applicazione. Per informazioni sull'utilizzo dei criteri di restrizione software in COM+, vedere [utilizzo dei criteri di restrizione software in com+](using-the-software-restriction-policy-in-com-.md).

**Per impostare i criteri di restrizione software**

1.  Fare clic con il pulsante destro del mouse sull'applicazione COM+ per la quale si stanno impostando i criteri di restrizione software, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .

3.  In **Criteri restrizione software** selezionare la casella di controllo **Applica criteri di restrizione software** ; in questo modo è possibile impostare il livello di attendibilità. Se si deseleziona la casella di controllo, COM+ utilizzerà la configurazione a livello dei criteri di restrizione software per l'applicazione. Questa casella di controllo corrisponde alla proprietà SRPEnabled della raccolta di [**applicazioni**](applications.md) .

4.  Nella casella **livello di restrizione** selezionare il livello appropriato. Questa casella di riepilogo a discesa corrisponde alla proprietà SRPTrustLevel della raccolta di [**applicazioni**](applications.md) . I livelli sono i seguenti, ordinati dal minimo al più attendibile:

    -   Non **consentito**. L'applicazione non è consentita per l'utilizzo dei privilegi completi dell'utente. È possibile caricare i componenti con un livello di attendibilità.
    -   **Senza restrizioni**. L'applicazione dispone di accesso illimitato ai privilegi dell'utente. Al suo interno possono essere caricati solo i componenti con un livello di attendibilità illimitato.

5.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della sicurezza Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Abilitazione dell'autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Impostazione di un livello di autenticazione per un'applicazione server](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[Impostazione di un livello di rappresentazione](setting-an-impersonation-level.md)
</dt> </dl>

 

 



