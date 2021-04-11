---
description: Quando si imposta un livello di rappresentazione per un'applicazione, si determina il grado di autorità che l'applicazione concede ad altre applicazioni per utilizzarne l'identità quando viene chiamata.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Impostazione di un livello di rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127014"
---
# <a name="setting-an-impersonation-level"></a>Impostazione di un livello di rappresentazione

Quando si imposta un livello di rappresentazione per un'applicazione, si determina il grado di autorità che l'applicazione concede ad altre applicazioni per utilizzarne l'identità quando viene chiamata. È possibile impostare questa impostazione solo per le applicazioni server COM+: le applicazioni di libreria vengono eseguite con l'identità del processo di hosting e utilizzano il livello di rappresentazione specificato. Per informazioni dettagliate, vedere [livelli di rappresentazione](/windows/desktop/com/impersonation-levels).

**Per selezionare un livello di rappresentazione**

1.  Fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si imposta la rappresentazione e quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .

3.  Nella casella **livello di rappresentazione** selezionare il livello appropriato. I livelli sono i seguenti, ordinati dalla concessione di almeno all'autorità più grande:

    -   **Anonimo**. Il client è anonimo per il server. Il server può rappresentare il client, ma il token di rappresentazione (credenziale locale) non contiene informazioni sul client.
    -   **Identificare**. Il server può ottenere l'identità del client e può rappresentare il client per eseguire controlli ACL.
    -   **Rappresenta**. Il server può rappresentare il client mentre agisce per suo conto, sebbene con restrizioni. Il server può accedere alle risorse nello stesso computer del client. Se il server si trova nello stesso computer del client, può accedere alle risorse di rete come client. Se il server si trova in un computer diverso da quello del client, può accedere solo alle risorse che si trovano nello stesso computer del server. Si tratta dell'impostazione predefinita per le applicazioni server COM+.
    -   **Delegato**. Il server può rappresentare il client mentre agisce per suo conto, sia nello stesso computer del client. Durante la rappresentazione, le credenziali del client, sia quelle con la validità locale che quella con la validità della rete, possono essere passate a un numero qualsiasi di computer.

4.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della sicurezza Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Configurazione dei criteri di restrizione software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Abilitazione dell'autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Impostazione di un livello di autenticazione per un'applicazione server](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
