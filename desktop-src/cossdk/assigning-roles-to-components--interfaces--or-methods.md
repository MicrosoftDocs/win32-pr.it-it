---
description: Assegnazione di ruoli a componenti, interfacce o metodi
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Assegnazione di ruoli a componenti, interfacce o metodi
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fcec11a52182bc0c9ac6f643c6c9cd75cb7b7462c35bbdea1ad0bc401f6ed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029861"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a>Assegnazione di ruoli a componenti, interfacce o metodi

È possibile assegnare in modo esplicito un ruolo a qualsiasi elemento all'interno di un'applicazione COM+ visibile tramite lo strumento di amministrazione Servizi componenti. In questo modo si garantisce che a tutti gli utenti membri del ruolo sia consentito l'accesso a tale elemento e a qualsiasi altro elemento in esso contenuto. Ad esempio, se si assegna il ruolo "Lettori" a un componente, a qualsiasi membro di "Lettori" è consentito l'accesso a tale componente ed eventuali interfacce e metodi esposti. "Lettori" verrà visualizzato come ruolo Ereditato per una qualsiasi di queste interfacce e metodi.

Un metodo è accessibile ai chiamanti solo se vi si assegna un ruolo, assegnando in modo esplicito il ruolo direttamente al metodo o assegnando un ruolo all'interfaccia del metodo o al componente del metodo, nel qual caso il ruolo verrà ereditato dal metodo. Se non viene assegnato alcun ruolo e se sono abilitati i controlli di accesso, tutte le chiamate al metodo avranno esito negativo.

Prima di poter assegnare un ruolo, è necessario [definirlo](defining-roles-for-an-application.md) per l'applicazione. Tutti i ruoli definiti per l'applicazione verranno visualizzati nella finestra Ruoli  impostati in modo esplicito per gli elementi selezionati nella scheda Sicurezza per tutti i componenti, i metodi e le interfacce all'interno dell'applicazione. 

**Per assegnare ruoli a un componente, un metodo o un'interfaccia**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione COM+ per cui è stato definito il ruolo. Espandere l'albero per visualizzare i componenti, le interfacce o i metodi dell'applicazione, a seconda dell'elemento a cui si sta assegnando il ruolo.

2.  Fare clic con il pulsante destro del mouse sull'elemento a cui si vuole assegnare il ruolo e quindi **scegliere Proprietà.**

3.  Nella finestra di dialogo delle proprietà fare clic **sulla scheda** Sicurezza .

4.  Nella casella **Ruoli impostati in modo esplicito per** gli elementi selezionati selezionare i ruoli da assegnare all'elemento.

5.  Fare clic su **OK**.

Tutti i ruoli impostati in modo esplicito per un elemento verranno ereditati da  tutti gli elementi di livello inferiore in esso contenuti e verranno visualizzati nella finestra Ruoli ereditati dagli elementi selezionati per tali elementi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della Role-Based sicurezza](configuring-role-based-security.md)
</dt> <dt>

[Definizione dei ruoli per un'applicazione](defining-roles-for-an-application.md)
</dt> <dt>

[Abilitazione dei controlli di accesso per un'applicazione](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Abilitazione dei controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



