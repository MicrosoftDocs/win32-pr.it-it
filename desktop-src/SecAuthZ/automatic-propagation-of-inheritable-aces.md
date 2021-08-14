---
description: Le funzioni SetNamedSecurityInfo e SetSecurityInfo supportano la propagazione automatica delle voci di controllo di accesso (ACE) ereditabili.
ms.assetid: 0aa49b9b-13e3-4ef9-921d-ea47a013e5a1
title: Propagazione automatica di ACE ereditabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257c038174549eebb8d960f8f4bc0601f95a928478e2a783f93f4a1444a22d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783718"
---
# <a name="automatic-propagation-of-inheritable-aces"></a>Propagazione automatica di ACE ereditabili

Le [**funzioni SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) e [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) supportano la propagazione automatica delle voci di controllo di accesso [*(ACE)*](/windows/desktop/SecGloss/a-gly) ereditabili. Ad esempio, se si usano queste funzioni per aggiungere una ACE ereditabile a una directory [](/windows/desktop/SecGloss/a-gly) in UN NTFS, il sistema applica la ACE in modo appropriato agli elenchi di controllo di accesso (ACL) di qualsiasi sottodirectory o file esistente.

Le voci ACE applicate direttamente hanno la precedenza sulle ACE ereditate. Il sistema implementa questa precedenza posizionando le voci ACE applicate direttamente prima delle voci ACE ereditate in un elenco di controllo di accesso [*discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL). Quando si chiamano le funzioni [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) e [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) per impostare le informazioni di sicurezza di un oggetto, il sistema impone il modello di ereditarietà corrente sugli ACL di tutti gli oggetti nella gerarchia sotto l'oggetto di destinazione. Per gli oggetti convertiti nel modello di ereditarietà corrente, i bit edizione Standard \_ DACL AUTO INHERITED e \_ edizione Standard \_ \_ SACL AUTO INHERITED \_ \_ [](/windows/desktop/SecGloss/s-gly) vengono impostati nel campo di controllo del descrittore di sicurezza dell'oggetto.

Quando si compila un nuovo descrittore di sicurezza che riflette il modello di ereditarietà corrente, è necessario non modificare la semantica del descrittore di sicurezza. Di conseguenza, le voci ACE di tipo Consenti e Nega non vengono mai spostate l'una rispetto all'altra. Se tale spostamento è necessario ,ad esempio per posizionare tutte le ACE non ereditate all'inizio di un ACL, l'ACL viene contrassegnato come protetto per impedire la modifica semantica.

Il sistema usa le regole seguenti per la propagazione delle voci ACE ereditate agli oggetti figlio:

-   Se un oggetto figlio senza DACL eredita una ACE, il risultato è un oggetto figlio con un dacl che contiene solo la ACE ereditata.
-   Se un oggetto figlio con un dacl vuoto eredita una ACE, il risultato è un oggetto figlio con un elenco DACL che contiene solo la ACE ereditata.
-   Se si rimuove una ACE ereditabile da un oggetto padre, l'ereditarietà automatica rimuove tutte le copie della ACE ereditate dagli oggetti figlio.
-   Se l'ereditarietà automatica comporta la rimozione di tutte le voci ACE dall'elenco DACL di un oggetto figlio, l'oggetto figlio ha un DACL vuoto anziché nessun DACL.

Queste regole possono avere il risultato imprevisto della conversione di un oggetto senza DACL in un oggetto con un dacl vuoto. Un oggetto senza DACL consente l'accesso completo, ma un oggetto con un DACL vuoto non consente l'accesso. Come esempio di come queste regole possono creare un DACL vuoto, si supponga di aggiungere una ACE ereditabile all'oggetto radice di un albero di oggetti. L'ereditarietà automatica propaga la ACE ereditabile a tutti gli oggetti nell'albero. Gli oggetti figlio avviati senza DACL dispongono ora di un elenco DACL con la ACE ereditata. Se si rimuove la ACE ereditabile dall'oggetto radice, il sistema propaga automaticamente la modifica agli oggetti figlio. Gli oggetti figlio avviati senza DACL (che consente l'accesso completo) hanno ora un DACL vuoto (che non consente l'accesso).

Per assicurarsi che un oggetto figlio senza DACL non sia interessato da ACE ereditabili, impostare il flag PROTECTED dacl di edizione Standard nel descrittore di sicurezza \_ \_ dell'oggetto.

Per informazioni su come creare correttamente un dacl, vedere [Creazione di un dacl.](/windows/desktop/SecBP/creating-a-dacl)

 

 
