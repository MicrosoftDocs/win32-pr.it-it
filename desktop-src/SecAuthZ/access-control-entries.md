---
description: Una voce di controllo di accesso (ACE) è un elemento di un elenco di controllo di accesso (ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Voci di controllo di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adcc382da130c57c55b869c47c8837c7780a7cff4e6dbdd881e55aa7b724dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785651"
---
# <a name="access-control-entries"></a>Voci di controllo di accesso

Una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) è un elemento di un elenco di controllo di [*accesso*](/windows/desktop/SecGloss/a-gly) (ACL). Un ACL può avere zero o più ACE. Ogni ACE controlla o monitora l'accesso a un oggetto da parte di un fiduciare specificato. Per informazioni sull'aggiunta, la rimozione o la modifica delle voci ACE negli ACL di un oggetto, vedere Modifica degli ACL di un oggetto [in C++.](modifying-the-acls-of-an-object-in-c--.md)

Sono disponibili sei tipi di ACE, tre dei quali sono supportati da tutti gli oggetti a protezione diretta. Gli altri tre tipi sono [ACE specifiche dell'oggetto supportate](object-specific-aces.md) dagli oggetti del servizio directory.

Tutti i tipi di ACE contengono le informazioni di controllo di accesso seguenti:

-   Identificatore [di sicurezza](security-identifiers.md) (SID) che identifica il [trustee](trustees.md) a cui si applica la ACE.
-   Maschera [*di accesso che*](/windows/desktop/SecGloss/a-gly) specifica i diritti di [accesso](access-rights-and-access-masks.md) controllati dalla ACE.
-   Flag che indica il tipo di ACE.
-   Set di flag di bit che determinano se i contenitori o gli oggetti figlio possono ereditare la ACE dall'oggetto primario a cui è collegato l'elenco di controllo di accesso.

Nella tabella seguente sono elencati i tre tipi di ACE supportati da tutti gli oggetti a protezione diretta.



| Tipo               | Descrizione                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE negata dall'accesso  | Utilizzato in un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/d-gly) discrezionale (DACL) per negare i diritti di accesso a un fiduciare.                                       |
| ACE consentita per l'accesso | Usato in un elenco DACL per consentire i diritti di accesso a un fiduciare.                                                                                                                                                                                              |
| ACE di controllo di sistema   | Utilizzato in un [*elenco di controllo*](/windows/desktop/SecGloss/s-gly) di accesso di sistema (SACL) per generare un record di controllo quando il fiduciare tenta di esercitare i diritti di accesso specificati. |



 

Per una tabella di ACE specifiche dell'oggetto, vedere [ACE specifiche dell'oggetto](object-specific-aces.md).

> [!Note]  
> Le voci ACE degli oggetti di allarme di sistema non sono attualmente supportate.

 

 

 
