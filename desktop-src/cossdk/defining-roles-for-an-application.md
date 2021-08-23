---
description: I criteri di sicurezza per un'applicazione vengono definiti definendo i privilegi di sicurezza necessari.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definizione dei ruoli per un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc4b4fb6aaee557eea69dec405254925cd669d18ac73cdea229f548145d8701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637711"
---
# <a name="defining-roles-for-an-application"></a>Definizione dei ruoli per un'applicazione

I criteri di sicurezza per un'applicazione vengono definiti definendo i privilegi di sicurezza necessari. A tale scopo, dichiarare un livello simbolico di privilegio come ruolo, [](assigning-roles-to-components--interfaces--or-methods.md) ovvero definire il ruolo per l'applicazione, e quindi assegnare il ruolo a risorse specifiche all'interno dell'applicazione. Questa progettazione viene soddisfatta quando l'applicazione viene distribuita e gli amministratori di sistema popolano il ruolo con utenti e gruppi di utenti effettivi. Per informazioni più dettagliate, vedere [Amministrazione della sicurezza basata sui ruoli.](role-based-security-administration.md)

**Per aggiungere un ruolo a un'applicazione**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ a cui si vuole aggiungere il ruolo. Espandere l'albero per visualizzare le cartelle per l'applicazione.

2.  Fare clic con il pulsante **destro del mouse** sulla cartella Ruoli per l'applicazione, scegliere **Nuovo** e quindi fare clic su **Ruolo**.

3.  Nella finestra **di** dialogo Ruolo digitare il nome del nuovo ruolo nella casella specificata.

4.  Fare clic su **OK**.

> [!Note]  
> Dopo aver aggiunto i ruoli all'applicazione, è necessario assicurarsi di assegnarli ai componenti, alle interfacce e ai metodi appropriati. In caso contrario, se è stata scelta e abilitata la sicurezza basata sui ruoli e se i ruoli sono stati aggiunti ma non assegnati, tutte le chiamate all'applicazione avranno esito negativo. Per altre informazioni, vedere [Assegnazione di ruoli a componenti, interfacce o metodi.](assigning-roles-to-components--interfaces--or-methods.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assegnazione di ruoli a componenti, interfacce o metodi](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configurazione della Role-Based sicurezza](configuring-role-based-security.md)
</dt> <dt>

[Abilitazione dei controlli di accesso per un'applicazione](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Abilitazione dei controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



