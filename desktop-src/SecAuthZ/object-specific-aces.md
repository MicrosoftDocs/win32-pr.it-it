---
description: Le voci ACE specifiche dell'oggetto sono supportate per gli oggetti del servizio directory (DS). Una voce ACE specifica dell'oggetto contiene una coppia di GUID che consente di espandere le modalità di protezione di un oggetto da parte della voce ACE.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: ACE specifiche dell'oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40760e5cd06af97e93f74c6ff8daff89cd5962f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057879"
---
# <a name="object-specific-aces"></a>ACE specifiche dell'oggetto

Le [*voci ACE*](/windows/desktop/SecGloss/a-gly) specifiche dell'oggetto sono supportate per gli oggetti del servizio directory (DS). Una voce ACE specifica dell'oggetto contiene una coppia di GUID che consente di espandere le modalità di protezione di un oggetto da parte della voce ACE.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ObjectType</strong></td>
<td>Identifica uno dei seguenti elementi:
<ul>
<li>Tipo di oggetto figlio. La voce ACE controlla il diritto di creare un tipo specificato di oggetto figlio. Per ulteriori informazioni, vedere <a href="controlling-child-object-creation-in-c--.md">controllo della creazione di oggetti figlio in C++</a>.</li>
<li>Set di proprietà o proprietà. La voce ACE controlla il diritto di leggere o scrivere la proprietà o il set di proprietà. Per altre informazioni, vedere <a href="aces-to-control-access-to-an-object-s-properties.md">ACE per controllare l'accesso alle proprietà di un oggetto</a>.</li>
<li>Un diritto esteso. La voce ACE controlla il diritto di eseguire l'operazione associata al diritto esteso.</li>
<li>Scrittura convalidata. La voce ACE controlla il diritto di eseguire determinate operazioni di scrittura. Queste autorizzazioni di scrittura convalidate, definite ed esposte nell'editor ACL, forniscono le autorizzazioni per le scritture convalidate delle proprietà anziché le scritture di basso livello non controllate di qualsiasi valore in una proprietà concessa con un'autorizzazione per la &quot; Proprietà Write &quot; .</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>InheritedObjectType</strong></td>
<td>Indica il tipo di oggetto figlio che può ereditare la voce ACE. L'ereditarietà è controllata anche dai flag di ereditarietà nel <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, nonché da qualsiasi protezione contro l'ereditarietà effettuata sugli oggetti figlio. Per ulteriori informazioni, vedere <a href="ace-inheritance.md">ereditarietà Ace</a>.</td>
</tr>
</tbody>
</table>



 

Sono supportati tre tipi di voci ACE specifiche dell'oggetto.

> [!Note]  
> Le voci ACE degli oggetti di sistema non sono attualmente supportate.

 



| Tipo                      | Descrizione                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE per oggetti con accesso negato  | Utilizzato in un DACL per negare a un trustee l'accesso a una proprietà o a una proprietà impostata sull'oggetto o per limitare l'ereditarietà ACE a un tipo specificato di oggetto figlio. Usa la [**struttura \_ \_ \_ ACE negata all'oggetto**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) .         |
| ACE oggetto consentito Access | Utilizzato in un DACL per consentire a un trustee di accedere a una proprietà o a una proprietà impostata sull'oggetto oppure per limitare l'ereditarietà ACE a un tipo specificato di oggetto figlio. Usa la [**struttura \_ \_ \_ ACE consentita dell'oggetto Access**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) .      |
| Controllo di sistema-ACE oggetto   | Utilizzato in un SACL per registrare i tentativi di accesso a una proprietà o a una proprietà impostata nell'oggetto o per limitare l'ereditarietà ACE a un tipo specificato di oggetto figlio. Usa la [**struttura \_ \_ \_ ACE dell'oggetto controllo di sistema**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) . |



 

Tutti gli ACL che contengono una voce ACE specifica dell'oggetto devono usare il servizio di revisione ACL Revisione ACL \_ \_ .

 

 
