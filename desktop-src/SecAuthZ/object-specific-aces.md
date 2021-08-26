---
description: Le voci ACE specifiche dell'oggetto sono supportate per gli oggetti del servizio directory. Una ACE specifica dell'oggetto contiene una coppia di GUID che espandono i modi in cui la ACE può proteggere un oggetto.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: ACE specifiche dell'oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4212a0f7fe4eff7e38b41fe2636643c457cfeb51
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469578"
---
# <a name="object-specific-aces"></a>ACE specifiche dell'oggetto

Le voci [*ACE specifiche dell'oggetto*](/windows/desktop/SecGloss/a-gly) sono supportate per gli oggetti del servizio directory. Una ACE specifica dell'oggetto contiene una coppia di GUID che espandono i modi in cui la ACE può proteggere un oggetto.




| GUID | Descrizione | 
|------|-------------|
| <strong>ObjectType</strong> | Identifica uno degli elementi seguenti:<ul><li>Tipo di oggetto figlio. La ACE controlla il diritto di creare un tipo specificato di oggetto figlio. Per altre informazioni, vedere <a href="controlling-child-object-creation-in-c--.md">Controllo della creazione di oggetti figlio in C++.</a></li><li>Set di proprietà o proprietà. La ACE controlla il diritto di leggere o scrivere la proprietà o il set di proprietà. Per altre informazioni, vedere <a href="aces-to-control-access-to-an-object-s-properties.md">ACE per controllare l'accesso alle proprietà di un oggetto.</a></li><li>Diritto esteso. La ACE controlla il diritto di eseguire l'operazione associata al diritto esteso.</li><li>Scrittura convalidata. La ACE controlla il diritto di eseguire determinate operazioni di scrittura. Queste autorizzazioni di scrittura convalidate, definite ed esposte nell'Editor ACL, forniscono le autorizzazioni per le scritture convalidate delle proprietà anziché le scritture di basso livello non verificate di qualsiasi valore in una proprietà concessa con un'autorizzazione di "proprietà di scrittura".</li></ul> | 
| <strong>InheritedObjectType</strong> | Indica il tipo di oggetto figlio che può ereditare la ACE. L'ereditarietà è controllata anche dai flag di ereditarietà nel <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, nonché da qualsiasi protezione dall'ereditarietà inserita negli oggetti figlio. Per altre informazioni, vedere <a href="ace-inheritance.md">Ereditarietà ACE.</a> | 




 

Sono supportati tre tipi di ACE specifiche dell'oggetto.

> [!Note]  
> Le voci ACE degli oggetti allarme di sistema non sono attualmente supportate.

 



| Tipo                      | Descrizione                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Access-denied object ACE  | Utilizzato in un elenco DACL per negare a un trustee l'accesso a una proprietà o a un set di proprietà nell'oggetto o per limitare l'ereditarietà ACE a un tipo specificato di oggetto figlio. Utilizza la [**struttura \_ \_ \_ ACE ACCESS DENIED OBJECT.**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace)         |
| Access-allowed object ACE | Utilizzato in un elenco DACL per consentire a un trustee l'accesso a una proprietà o a un set di proprietà nell'oggetto o per limitare l'ereditarietà ACE a un tipo specificato di oggetto figlio. Utilizza la [**struttura \_ \_ \_ ACE ACCESS ALLOWED OBJECT.**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace)      |
| Voce ACE dell'oggetto di controllo di sistema   | Usato in un elenco SACL per registrare i tentativi di accesso a una proprietà o a un set di proprietà nell'oggetto o per limitare l'ereditarietà ACE a un tipo specificato di oggetto figlio. Utilizza la [**struttura \_ \_ \_ ACE SYSTEM AUDIT OBJECT.**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) |



 

Qualsiasi ACL che contiene una ACE specifica dell'oggetto deve utilizzare l'ACL \_ revisione REVISION \_ DS.

 

 
