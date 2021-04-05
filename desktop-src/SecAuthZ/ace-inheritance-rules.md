---
description: Il sistema propaga le voci di controllo di accesso (ACE) ereditabili agli oggetti figlio in base a un set di regole di ereditarietà.
ms.assetid: 08f76aaa-8379-4ba8-9735-7568001bcd53
title: Regole di ereditarietà ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8c786ebcc8450e8e5da1833f34fc85c37ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756194"
---
# <a name="ace-inheritance-rules"></a>Regole di ereditarietà ACE

Il sistema propaga le voci di [*controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) ereditabili agli oggetti figlio in base a un set di regole di ereditarietà. Il sistema inserisce le voci ACE ereditate nell' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) dell'elemento figlio in base all'ordine preferenziale [delle voci ACE in un DACL](order-of-aces-in-a-dacl.md). Il sistema imposta il \_ flag ACE ereditato in tutte le voci ACE ereditate.

Le voci ACE ereditate dagli oggetti figlio contenitore e non contenitore sono diverse a seconda delle combinazioni di flag di ereditarietà. Queste regole di ereditarietà hanno lo stesso funzionamento sia per gli [*elenchi*](/windows/desktop/SecGloss/s-gly) DACL che per gli elenchi di controllo di accesso di sistema (SACL).



| Flag ACE padre                                  | Effetto sull'ACL figlio                                                                                                                                                                                                                      |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OGGETTO che \_ eredita \_ solo ACE                        | Oggetti figlio non contenitore: ereditato come ACE effettivo. Oggetti figlio del contenitore: i contenitori ereditano una voce ACE di solo ereditarietà a meno che non \_ \_ sia impostato anche il flag di bit a non ereditare \_ .<br/>                                       |
| Il contenitore \_ eredita \_ solo ACE                     | Oggetti figlio non contenitore: nessun effetto sull'oggetto figlio. Oggetti figlio del contenitore: l'oggetto figlio eredita una voce ACE efficace. La voce ACE ereditata è ereditabile, a meno che non \_ \_ \_ sia impostato anche il flag di bit Ace ereditare No.<br/> |
| Il contenitore \_ eredita \_ ACE e l'oggetto \_ ereditano \_ ACE | Oggetti figlio non contenitore: ereditato come ACE effettivo. Oggetti figlio del contenitore: l'oggetto figlio eredita una voce ACE efficace. La voce ACE ereditata è ereditabile, a meno che non \_ \_ \_ sia impostato anche il flag di bit Ace ereditare No.<br/> |
| Nessun flag di ereditarietà impostato                         | Nessun effetto sul contenitore figlio o sugli oggetti non contenitore.                                                                                                                                                                                    |



 

Se una voce ACE ereditata è una voce ACE efficace per l'oggetto figlio, il sistema esegue il mapping di qualsiasi diritto generico ai diritti specifici per l'oggetto figlio. Analogamente, il sistema esegue il mapping degli [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) generici (SID), ad esempio Creator \_ Owner, al SID appropriato. Se una voce ACE ereditata è una voce ACE ereditata, eventuali diritti generici o SID generici rimangono invariati, in modo che possano essere mappati correttamente quando la voce ACE viene ereditata dalla generazione successiva di oggetti figlio.

Per un caso in cui un oggetto contenitore eredita una voce ACE che sia efficace sul contenitore ed ereditabile dai relativi discendenti, il contenitore può ereditare due ACE. Questo errore si verifica se la voce ACE ereditabile contiene informazioni generiche. Il contenitore eredita una voce ACE di solo ereditarietà che contiene le informazioni generiche e una voce ACE solo valida in cui è stato eseguito il mapping delle informazioni generiche.

Una [voce ACE specifica dell'oggetto](object-specific-aces.md) ha un membro **InheritedObjectType** che può contenere un GUID per identificare il tipo di oggetto che può ereditare la voce ACE.

Se il GUID **InheritedObjectType** non è specificato, le regole di ereditarietà per una voce ACE specifica dell'oggetto sono uguali a quelle per una voce ACE standard.

Se viene specificato il GUID **InheritedObjectType** , la voce ACE è ereditabile da oggetti che corrispondono al GUID se l'oggetto \_ eredita \_ ACE è impostato e dai contenitori che corrispondono al GUID se il contenitore \_ eredita \_ ACE è impostato. Si noti che attualmente solo gli oggetti DS supportano le voci ACE specifiche dell'oggetto e il servizio DS considera tutti i tipi di oggetto come contenitori.

 

