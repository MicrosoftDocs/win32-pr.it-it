---
title: Ereditarietà del controllo di accesso
description: Le voci di controllo di accesso (ACE) in un elenco di controllo di accesso (ACL) di un oggetto possono appartenere a un ACL effettivo o ereditare l'ACL.
ms.assetid: 2530eef5-7804-4b27-8756-d97be1cea116
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec7514ab8cae8b07121d84e579ccb8492b67c45
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117511"
---
# <a name="access-control-inheritance"></a>Ereditarietà del controllo di accesso

Le voci di controllo di accesso (ACE) in un elenco di controllo di accesso (ACL) di un oggetto possono appartenere a una delle due categorie seguenti:

-   ACL effettivo: le voci ACE in questa categoria si applicano all'oggetto.
-   Inherit ACL: le voci ACE in questa categoria vengono ereditate dagli oggetti creati nel contenitore.

Ogni voce ACE nell'elenco DACL può appartenere a una o più categorie. Le categorie per cui appartiene una voce ACE sono determinate dai flag di controllo di ereditarietà impostati nella voce ACE.

Tre flag di controllo di ereditarietà possono essere impostati nella proprietà [**AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) di una voce ACE.



| Flag                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ ACEFLAG \_ eredita \_ ACE**                | Questo flag indica che la voce ACE è inclusa nell'ACL di ereditarietà e che gli oggetti figlio ereditano i flag di controllo di ereditarietà di questa voce ACE.                                                                                                                                                                                                                                                                                                                         |
| **ADS \_ ACEFLAG \_ No \_ propagate \_ eredita \_ ACE** | Questo flag indica che la voce ACE è inclusa nell'ACL di ereditarietà, ma che nessun flag di controllo di ereditarietà viene propagato agli oggetti figlio diretti (discendenti diretti) e la voce ACE è efficace sugli oggetti figlio diretti.                                                                                                                                                                                                                                          |
| **ADS \_ ACEFLAG \_ ereditano \_ solo \_ ACE**          | Questo flag indica che la voce ACE non è inclusa nell'ACL effettivo. Se questo flag non è impostato, la voce ACE fa parte dell'ACL effettivo. Questo flag è utile per l'impostazione di autorizzazioni ereditabili dagli oggetti SubObject, ma non influisce sull'accessibilità del contenitore. Se ad esempio una voce ACE deve essere ereditata da oggetti utente in un'unità organizzativa, è probabile che non venga applicata per l'accesso all'unità organizzativa stessa.<br/> |



 

Gli **annunci \_ ACEFLAG \_ No \_ propagate \_ ereditano \_ ACE** e **Ads \_ ACEFLAG \_ ereditano \_ solo \_** i flag ACE sono significativi solo se gli **annunci \_ ACEFLAG \_ ereditano \_ ACE** è presente. Ciò è dovuto al fatto che il flag **\_ \_ \_ ACE ereditato da ADS ACEFLAG** aggiunge il comportamento di ereditarietà a una voce ACE ereditabile, ma non definisce il tipo di ereditarietà. Gli **annunci \_ ACEFLAG \_ No \_ propagate \_ ereditano \_ ACE** e **Ads \_ ACEFLAG \_ ereditano \_ solo \_** i flag ACE definiscono un tipo specifico di comportamento di ereditarietà.

È importante ricordare che il sistema imposta anche i flag seguenti in base al tipo e allo stato della voce ACE.



| Flag                                    | Descrizione                                           |
|-----------------------------------------|-------------------------------------------------------|
| **\_ \_ ACE ereditato ACEFLAG \_ ADS**        | Questo flag indica che la voce ACE è stata ereditata.       |
| **\_flag di \_ \_ ereditarietà validi \_ per ADS ACEFLAG** | Questo flag indica che i flag di ereditarietà sono validi. |



 

La tabella seguente elenca gli effetti delle diverse combinazioni di flag per la proprietà [**AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) di una voce ACE.



| Contrassegno                                                                                                                    | Effetto sull'oggetto che contiene la voce ACE                     | Effetti sugli oggetti figlio diretti                                                      | Effetti sugli oggetti sotto gli elementi figlio diretti               |
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------|
| Nessun contrassegno impostato.                                                                                                           | ACE effettivo: ACE si applica all'oggetto.               | ACE non viene ereditato.                                                               | ACE non viene ereditato.                                 |
| **ADS \_ ACEFLAG \_ eredita \_ ACE**                                                                                          | ACE efficace                                           | ACE viene ereditato. ACE è una voce ACE efficace.<br/>                               | ACE viene ereditato. ACE è una voce ACE efficace.<br/> |
| **Annunci \_ ACEFLAG \_ ereditano \_ ACE** \| **Ads \_ ACEFLAG \_ \_ solo eredita \_ ACE**                                                  | Non è un ACE efficace: ACE non si applica all'oggetto. | ACE viene ereditato. ACE è una voce ACE efficace.<br/>                               | ACE viene ereditato. ACE è una voce ACE efficace.<br/> |
| **Annunci \_ ACEFLAG \_ eredita \_ ACE** \| **Ads \_ ACEFLAG \_ No \_ propagate \_ eredita \_ ACE**                                         | ACE efficace                                           | ACE viene ereditato ma senza flag di ereditarietà. ACE è una voce ACE efficace<br/>  | ACE non viene ereditato.                                 |
| **Annunci \_ ACEFLAG \_ \_ ereditano** gli \| **annunci Ace \_ ACEFLAG \_ ereditano \_ solo \_ ACE** \| **Ads \_ ACEFLAG \_ No \_ propagate \_ eredita \_ ACE** | Non è una voce ACE valida.                                   | ACE viene ereditato ma senza flag di ereditarietà. ACE è una voce ACE efficace.<br/> | ACE non viene ereditato.                                 |



 

 

