---
description: Un ACL di oggetti può contenere voci ACE ereditate dal relativo contenitore padre.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: Ereditarietà ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967236"
---
# <a name="ace-inheritance"></a>Ereditarietà ACE

L'ACL di un oggetto può contenere voci ACE ereditate dal relativo contenitore padre. Una sottochiave del registro di sistema, ad esempio, può ereditare Ace dalla chiave precedente nella gerarchia del registro di sistema. Analogamente, un file in un file system NTFS può ereditare voci ACE dalla directory che lo contiene.

La struttura dell' [**\_ intestazione ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) di una voce ACE contiene un set di flag di ereditarietà che controllano l'ereditarietà della voce ACE e l'effetto di una voce ACE sull'oggetto a cui è collegato. Il sistema interpreta i flag di ereditarietà e altre informazioni sull'ereditarietà in base alle [regole dell'ereditarietà Ace](ace-inheritance-rules.md).

Queste regole sono state migliorate con le funzionalità seguenti:

-   Supporto per la [propagazione automatica di ACE ereditabili](automatic-propagation-of-inheritable-aces.md).
-   Flag che distingue le voci ACE ereditate e le voci ACE che sono state applicate direttamente a un oggetto.
-   Voci ACE specifiche dell'oggetto che consentono di specificare il tipo di oggetto figlio che può ereditare la voce ACE.
-   La possibilità di impedire a un DACL o un SACL di ereditare le voci ACE mediante l'impostazione dei bit protetti da SE \_ DACL \_ o se \_ SACL \_ nei bit di controllo del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) , ad eccezione di Ace attributo della risorsa di sistema \_ \_ \_ e \_ ACE con ID criteri con ambito di sistema \_ \_ \_ .

 

 
