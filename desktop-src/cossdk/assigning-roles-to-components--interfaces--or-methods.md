---
description: Assegnazione di ruoli a componenti, interfacce o metodi
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Assegnazione di ruoli a componenti, interfacce o metodi
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401470"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a>Assegnazione di ruoli a componenti, interfacce o metodi

È possibile assegnare in modo esplicito un ruolo a qualsiasi elemento all'interno di un'applicazione COM+ visibile mediante lo strumento di amministrazione Servizi componenti. In questo modo si garantisce che a tutti gli utenti membri del ruolo verrà consentito l'accesso a tale elemento e a tutti gli altri elementi in esso contenuti. Se, ad esempio, si assegna il ruolo "Readers" a un componente, qualsiasi membro di "Readers" potrà accedere a tale componente e alle interfacce e ai metodi esposti. "Readers" viene visualizzato come ruolo ereditato per le interfacce e i metodi.

Un metodo è accessibile ai chiamanti solo se si assegna un ruolo, assegnando esplicitamente il ruolo direttamente al metodo o assegnando un ruolo all'interfaccia del metodo o al componente del metodo, nel qual caso il ruolo verrà ereditato dal metodo. Se non viene assegnato alcun ruolo e se sono abilitati i controlli di accesso, tutte le chiamate al metodo avranno esito negativo.

Prima di poter assegnare un ruolo, è necessario [definirlo](defining-roles-for-an-application.md) per l'applicazione. Tutti i ruoli definiti per l'applicazione verranno visualizzati nei **ruoli impostati in modo esplicito per la finestra elementi selezionati** nella scheda **sicurezza** per qualsiasi componente, metodo e interfaccia all'interno dell'applicazione.

**Per assegnare ruoli a un componente, a un metodo o a un'interfaccia**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ per la quale è stato definito il ruolo. Espandere l'albero per visualizzare i componenti, le interfacce o i metodi dell'applicazione, a seconda di ciò a cui viene assegnato il ruolo.

2.  Fare clic con il pulsante destro del mouse sull'elemento a cui si desidera assegnare il ruolo, quindi scegliere **Proprietà**.

3.  Nella finestra di dialogo Proprietà fare clic sulla scheda **sicurezza** .

4.  Nella casella **ruoli impostati in modo esplicito per gli elementi selezionati** selezionare i ruoli che si desidera assegnare all'elemento.

5.  Fare clic su **OK**.

Tutti i ruoli impostati in modo esplicito per un elemento verranno ereditati da tutti gli elementi di livello inferiore che contiene e verranno visualizzati nella finestra **ruoli ereditati da elementi selezionati** per tali elementi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della sicurezza Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Definizione dei ruoli per un'applicazione](defining-roles-for-an-application.md)
</dt> <dt>

[Abilitazione dei controlli di accesso per un'applicazione](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Abilitazione dei controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



