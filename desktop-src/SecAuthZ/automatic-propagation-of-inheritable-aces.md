---
description: Le funzioni SetNamedSecurityInfo e SetSecurityInfo supportano la propagazione automatica di voci di controllo di accesso (ACE) ereditabili.
ms.assetid: 0aa49b9b-13e3-4ef9-921d-ea47a013e5a1
title: Propagazione automatica di ACE ereditabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fab03c73a1c926468e46a0d0492e512dab42af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234336"
---
# <a name="automatic-propagation-of-inheritable-aces"></a>Propagazione automatica di ACE ereditabili

Le funzioni [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) e [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) supportano la propagazione automatica di [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) ereditabili. Se ad esempio si usano queste funzioni per aggiungere una voce ACE ereditabile a una directory in NTFS, il sistema applica la voce ACE in modo appropriato agli [*elenchi di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) di eventuali sottodirectory o file esistenti.

Le voci ACE applicate direttamente hanno la precedenza sulle voci ACE ereditate. Il sistema implementa questa precedenza inserendo le voci ACE applicate direttamente in avanti rispetto alle voci ACE ereditate in un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL). Quando si chiamano le funzioni [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) e [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) per impostare le informazioni di sicurezza di un oggetto, il sistema impone il modello di ereditarietà corrente sugli ACL di tutti gli oggetti nella gerarchia sotto l'oggetto di destinazione. Per gli oggetti che sono stati convertiti nel modello di ereditarietà corrente, i bit ereditati automaticamente di SE \_ DACL \_ e il \_ \_ SACL \_ automatico \_ ereditati vengono impostati nel campo del controllo del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) dell'oggetto.

Quando si compila un nuovo descrittore di sicurezza che riflette il modello di ereditarietà corrente, è necessario non modificare la semantica del descrittore di sicurezza. Di conseguenza, le voci ACE Allow e Deny non vengono mai spostate in relazione tra loro. Se questo movimento è necessario, ad esempio per inserire tutte le voci ACE non ereditate all'inizio di un ACL, l'ACL viene contrassegnato come protetto per evitare la modifica semantica.

Il sistema usa le regole seguenti per la propagazione delle voci ACE ereditate agli oggetti figlio:

-   Se un oggetto figlio senza DACL eredita una voce ACE, il risultato è un oggetto figlio con un DACL che contiene solo la voce ACE ereditata.
-   Se un oggetto figlio con un DACL vuoto eredita una voce ACE, il risultato è un oggetto figlio con un DACL che contiene solo la voce ACE ereditata.
-   Se si rimuove una voce ACE ereditabile da un oggetto padre, l'ereditarietà automatica rimuove tutte le copie della voce ACE ereditate dagli oggetti figlio.
-   Se l'ereditarietà automatica comporta la rimozione di tutte le voci ACE dall'elenco DACL di un oggetto figlio, l'oggetto figlio ha un DACL vuoto anziché un DACL.

Queste regole possono avere il risultato imprevisto della conversione di un oggetto senza DACL in un oggetto con un DACL vuoto. Un oggetto senza DACL consente l'accesso completo, ma un oggetto con un DACL vuoto non consente l'accesso. Come esempio di come queste regole possano creare un DACL vuoto, si supponga di aggiungere una voce ACE ereditabile all'oggetto radice di un albero di oggetti. L'ereditarietà automatica propaga la voce ACE ereditabile a tutti gli oggetti nell'albero. Gli oggetti figlio che iniziano senza DACL ora hanno un DACL con la voce ACE ereditata. Se si rimuove la voce ACE ereditabile dall'oggetto radice, il sistema propaga automaticamente la modifica agli oggetti figlio. Gli oggetti figlio che iniziano senza DACL (che consentono l'accesso completo) ora hanno un DACL vuoto (che non consente l'accesso).

Per assicurarsi che un oggetto figlio senza DACL non sia influenzato dalle voci ACE ereditabili, impostare il \_ flag se DACL \_ protected nel descrittore di sicurezza dell'oggetto.

Per informazioni su come creare correttamente un DACL, vedere [creazione di un DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
