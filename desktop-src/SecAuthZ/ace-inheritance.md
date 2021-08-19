---
description: Un ACL di oggetti può contenere ACE ereditate dal contenitore padre.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: Ereditarietà ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd239801ea15dddb142c42d86e1aa44d0d644e5d217c50fc7c9cf9388747e45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785382"
---
# <a name="ace-inheritance"></a>Ereditarietà ACE

L'ACL di un oggetto può contenere ACE ereditate dal contenitore padre. Ad esempio, una sottochiave del Registro di sistema può ereditare le voci ACE dalla chiave precedente nella gerarchia del Registro di sistema. Analogamente, un file in un file system NTFS può ereditare le voci ACE dalla directory che lo contiene.

La [**struttura ACE \_ HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) di una ACE contiene un set di flag di ereditarietà che controllano l'ereditarietà della ACE e l'effetto di una ACE sull'oggetto a cui è associata. Il sistema interpreta i flag di ereditarietà e altre informazioni sull'ereditarietà in base [alle regole di ereditarietà ACE.](ace-inheritance-rules.md)

Queste regole sono state migliorate con le funzionalità seguenti:

-   Supporto per [la propagazione automatica di ACE ereditabili.](automatic-propagation-of-inheritable-aces.md)
-   Flag che differenzia le ACE ereditate e le voci ACE applicate direttamente a un oggetto .
-   ACE specifiche dell'oggetto che consentono di specificare il tipo di oggetto figlio che può ereditare la ACE.
-   Possibilità di impedire a un DACL o a un SACL di ereditare le voci ACE impostando i bit PROTECTED o SACL PROTECTED di edizione Standard edizione Standard nei bit di controllo del descrittore di sicurezza, ad eccezione di SYSTEM RESOURCE ATTRIBUTE ACE e \_ \_ SYSTEM \_ \_ [](/windows/desktop/SecGloss/s-gly) \_ \_ \_ \_ SCOPED POLICY ID \_ \_ \_ ACE.

 

 
