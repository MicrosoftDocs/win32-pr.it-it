---
description: Quando si imposta un livello di rappresentazione per un'applicazione, si determina il livello di autorità che l'applicazione concede ad altre applicazioni di usare la propria identità quando le chiama.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Impostazione di un livello di rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c23b8d0b54f12cbce92af43187681922854519c69e8614e952fda241e4fa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895951"
---
# <a name="setting-an-impersonation-level"></a>Impostazione di un livello di rappresentazione

Quando si imposta un livello di rappresentazione per un'applicazione, si determina il livello di autorità che l'applicazione concede ad altre applicazioni di usare la propria identità quando le chiama. È possibile impostare questo valore solo per le applicazioni server COM+: le applicazioni libreria vengono eseguite con l'identità del processo di hosting e usano il livello di rappresentazione specificato. Per altre informazioni, vedere [Livelli di rappresentazione](/windows/desktop/com/impersonation-levels).

**Per selezionare un livello di rappresentazione**

1.  Fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si sta impostando la rappresentazione e quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo delle proprietà dell'applicazione fare clic **sulla scheda** Sicurezza .

3.  Nella casella **Livello di rappresentazione** selezionare il livello appropriato. I livelli sono i seguenti, ordinati dalla concessione dell'autorità minima alla massima autorità:

    -   **Anonimo**. Il client è anonimo per il server. Il server può rappresentare il client, ma il token di rappresentazione (una credenziale locale) non contiene informazioni sul client.
    -   **Identificare**. Il server può ottenere l'identità del client e può rappresentare il client per eseguire i controlli ACL.
    -   **Rappresentare .** Il server può rappresentare il client mentre agisce per suo conto, anche se con restrizioni. Il server può accedere alle risorse nello stesso computer del client. Se il server si trova nello stesso computer del client, può accedere alle risorse di rete del client. Se il server si trova in un computer diverso dal client, può accedere solo alle risorse che si trova nello stesso computer del server. Si tratta dell'impostazione predefinita per le applicazioni server COM+.
    -   **Delegare**. Il server può rappresentare il client mentre agisce per suo conto, sia nello stesso computer del client. Durante la rappresentazione, le credenziali del client (sia quelle con validità locale che quelle con validità di rete) possono essere passate a qualsiasi numero di computer.

4.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della Role-Based sicurezza](configuring-role-based-security.md)
</dt> <dt>

[Configurazione dei criteri di restrizione software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Abilitazione dell'autenticazione per un'applicazione libreria](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Impostazione di un livello di autenticazione per un'applicazione server](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
