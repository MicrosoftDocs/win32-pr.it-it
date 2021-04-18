---
description: Una voce di controllo di accesso (ACE) è un elemento in un elenco di controllo di accesso (ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Voci di controllo di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fe98cf1c1c4d5fb23091a6539564ff964202cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310955"
---
# <a name="access-control-entries"></a>Voci di controllo di accesso

Una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) è un elemento in un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL). Un ACL può avere zero o più voci ACE. Ogni ACE controlla o monitora l'accesso a un oggetto da un trustee specificato. Per informazioni sull'aggiunta, la rimozione o la modifica delle voci ACE negli ACL di un oggetto, vedere [modifica degli ACL di un oggetto in C++](modifying-the-acls-of-an-object-in-c--.md).

Sono disponibili sei tipi di ACE, tre dei quali sono supportati da tutti gli oggetti a protezione diretta. Gli altri tre tipi sono [ACE specifici](object-specific-aces.md) degli oggetti supportati dagli oggetti del servizio directory.

Tutti i tipi di voci ACE contengono le informazioni di controllo di accesso seguenti:

-   [ID di sicurezza](security-identifiers.md) (SID) che identifica il [trustee](trustees.md) a cui viene applicata la voce ACE.
-   [*Maschera di accesso*](/windows/desktop/SecGloss/a-gly) che specifica i [diritti di accesso](access-rights-and-access-masks.md) controllati dalla voce ACE.
-   Flag che indica il tipo di voce ACE.
-   Set di flag di bit che determinano se i contenitori figlio o gli oggetti possono ereditare la voce ACE dall'oggetto primario a cui è collegato l'ACL.

Nella tabella seguente sono elencati i tre tipi ACE supportati da tutti gli oggetti a protezione diretta.



| Tipo               | Descrizione                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE con accesso negato  | Utilizzato in un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) per negare i diritti di accesso a un trustee.                                       |
| ACE consentito per l'accesso | Utilizzato in un DACL per consentire diritti di accesso a un trustee.                                                                                                                                                                                              |
| ACE di controllo del sistema   | Utilizzato in un [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL) per generare un record di controllo quando il trustee tenta di esercitare i diritti di accesso specificati. |



 

Per una tabella di voci ACE specifiche dell'oggetto, vedere [ACE specifici degli oggetti](object-specific-aces.md).

> [!Note]  
> Le voci ACE degli oggetti di sistema non sono attualmente supportate.

 

 

 
