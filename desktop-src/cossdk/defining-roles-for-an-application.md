---
description: Per determinare i criteri di sicurezza per un'applicazione, è necessario definire i privilegi di sicurezza necessari.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definizione dei ruoli per un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304627"
---
# <a name="defining-roles-for-an-application"></a>Definizione dei ruoli per un'applicazione

Per determinare i criteri di sicurezza per un'applicazione, è necessario definire i privilegi di sicurezza necessari. A tale scopo, è necessario dichiarare un livello simbolico di privilegio come ruolo, ovvero definire il ruolo per l'applicazione, quindi [assegnare il ruolo](assigning-roles-to-components--interfaces--or-methods.md) a risorse specifiche all'interno dell'applicazione. Questa progettazione viene soddisfatta quando viene distribuita l'applicazione e gli amministratori di sistema popolano il ruolo con utenti e gruppi di utenti effettivi. Per maggiori dettagli, vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).

**Per aggiungere un ruolo a un'applicazione**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ a cui si desidera aggiungere il ruolo. Espandere l'albero per visualizzare le cartelle per l'applicazione.

2.  Fare clic con il pulsante destro del mouse sulla cartella **ruoli** per l'applicazione, scegliere **nuovo**, quindi fare clic su **ruolo**.

3.  Nella finestra di dialogo **ruolo** Digitare il nome del nuovo ruolo nella casella specificata.

4.  Fare clic su **OK**.

> [!Note]  
> Dopo aver aggiunto i ruoli all'applicazione, è necessario assicurarsi di assegnare i ruoli ai componenti, alle interfacce e ai metodi appropriati. In caso contrario, se è stata scelta e abilitata la sicurezza basata sui ruoli e se i ruoli sono stati aggiunti ma non assegnati, tutte le chiamate all'applicazione avranno esito negativo. Per ulteriori informazioni, vedere [assegnazione di ruoli a componenti, interfacce o metodi](assigning-roles-to-components--interfaces--or-methods.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assegnazione di ruoli a componenti, interfacce o metodi](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configurazione della sicurezza Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Abilitazione dei controlli di accesso per un'applicazione](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Abilitazione dei controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



