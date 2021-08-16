---
description: Il sistema propaga le voci di controllo di accesso (ACE) ereditabili agli oggetti figlio in base a un set di regole di ereditarietà.
ms.assetid: 08f76aaa-8379-4ba8-9735-7568001bcd53
title: Regole di ereditarietà ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77e5d9fcbef9125108e8f0be76cd5b7c79a2f99ba524c81f3fd1da84336f04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785365"
---
# <a name="ace-inheritance-rules"></a>Regole di ereditarietà ACE

Il sistema propaga le voci di controllo di [*accesso*](/windows/desktop/SecGloss/a-gly) (ACE) ereditabili agli oggetti figlio in base a un set di regole di ereditarietà. Il sistema inserisce le [](/windows/desktop/SecGloss/d-gly) voci ACE ereditate nell'elenco di controllo di accesso discrezionale (DACL) dell'elemento figlio in base all'ordine preferito delle voci ACE [in un elenco DACL.](order-of-aces-in-a-dacl.md) Il sistema imposta il \_ flag ACE EREDITATO in tutte le voci ACE ereditate.

Le voci ACE ereditate dagli oggetti figlio contenitore e non contenitore variano a seconda delle combinazioni di flag di ereditarietà. Queste regole di ereditarietà funzionano [](/windows/desktop/SecGloss/s-gly) allo stesso modo sia per gli elenchi di controllo di accesso di sistema (DACL) che per gli elenchi di controllo di accesso di sistema (SACL).



| Flag ACE padre                                  | Effetto sull'ACL figlio                                                                                                                                                                                                                      |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Solo \_ ACE OBJECT INHERIT \_                        | Oggetti figlio non contenitore: ereditati come ACE effettive. Oggetti figlio del contenitore: i contenitori ereditano una ACE di sola ereditarietà, a meno che non sia impostato anche il flag di bit NO \_ PROPAGATE \_ INHERIT \_ ACE.<br/>                                       |
| SOLO CONTAINER \_ INHERIT \_ ACE                     | Oggetti figlio non contenitore: nessun effetto sull'oggetto figlio. Oggetti figlio del contenitore: l'oggetto figlio eredita una ACE effettiva. La ACE ereditata è ereditabile a meno che non sia impostato anche il flag di bit NO \_ PROPAGATE \_ INHERIT \_ ACE.<br/> |
| CONTAINER \_ INHERIT \_ ACE e OBJECT INHERIT \_ \_ ACE | Oggetti figlio non contenitore: ereditati come ACE effettive. Oggetti figlio del contenitore: l'oggetto figlio eredita una ACE effettiva. La ACE ereditata è ereditabile a meno che non sia impostato anche il flag di bit NO \_ PROPAGATE \_ INHERIT \_ ACE.<br/> |
| Nessun flag di ereditarietà impostato                         | Nessun effetto sugli oggetti contenitore figlio o non contenitore.                                                                                                                                                                                    |



 

Se una ACE ereditata è una ACE effettiva per l'oggetto figlio, il sistema esegue il mapping di tutti i diritti generici ai diritti specifici per l'oggetto figlio. Analogamente, il sistema esegue il mapping degli ID di sicurezza [*generici*](/windows/desktop/SecGloss/s-gly) (SID), ad esempio CREATOR \_ OWNER, al SID appropriato. Se una ACE ereditata è una ACE di sola ereditarietà, tutti i diritti generici o i SID generici vengono lasciati invariati in modo che possano essere mappati in modo appropriato quando la ACE viene ereditata dalla generazione successiva di oggetti figlio.

Per un caso in cui un oggetto contenitore eredita una ACE effettiva nel contenitore e ereditabile dai relativi discendenti, il contenitore può ereditare due ACE. Ciò si verifica se la ACE ereditabile contiene informazioni generiche. Il contenitore eredita una ACE di sola ereditarietà che contiene le informazioni generiche e una ACE di sola efficacia in cui è stato eseguito il mapping delle informazioni generiche.

Una [ACE specifica dell'oggetto](object-specific-aces.md) ha un membro **InheritedObjectType** che può contenere un GUID per identificare il tipo di oggetto che può ereditare la ACE.

Se il GUID **InheritedObjectType** non viene specificato, le regole di ereditarietà per una ACE specifica dell'oggetto sono le stesse di una ACE standard.

Se viene specificato il GUID **InheritedObjectType,** la ACE può essere ereditata dagli oggetti che corrispondono al GUID se è impostata l'ACE OBJECT INHERIT e dai contenitori che corrispondono al GUID se container INHERIT ACE è \_ \_ \_ \_ impostato. Si noti che attualmente solo gli oggetti DS supportano ACE specifiche dell'oggetto e il servizio DS considera tutti i tipi di oggetto come contenitori.

 

