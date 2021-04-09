---
description: Ogni tipo di oggetto a protezione diretta dispone di un set di diritti di accesso che corrispondono alle operazioni specifiche per quel tipo di oggetto.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Diritti di accesso standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879646"
---
# <a name="standard-access-rights"></a>Diritti di accesso standard

Ogni tipo di oggetto a protezione diretta dispone di un set di diritti di accesso che corrispondono alle operazioni specifiche per quel tipo di oggetto. Oltre a questi diritti di accesso specifici per gli oggetti, è disponibile un set di diritti di accesso standard che corrispondono alle operazioni comuni alla maggior parte dei tipi di oggetti a protezione diretta.

Il [formato della maschera di accesso](access-mask-format.md) include un set di bit per i diritti di accesso standard. Le costanti di Windows seguenti per i diritti di accesso standard sono definite in Winnt. h.



| Costante      | Significato                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE        | Diritto di eliminare l'oggetto.                                                                                                                                                                                                                                                                                                              |
| controllo di lettura \_ | Diritto di leggere le informazioni nel [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)dell'oggetto, senza includere le informazioni nell' [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL). |
| SYNCHRONIZE   | Diritto di utilizzare l'oggetto per la sincronizzazione. Ciò consente a un thread di attendere fino a quando l'oggetto non è nello stato segnalato. Alcuni tipi di oggetto non supportano questo diritto di accesso.                                                                                                                                                                |
| Scrivi \_ DAC    | Diritto di modificare l' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) nel descrittore di sicurezza dell'oggetto.                                                                                                                    |
| Scrivi \_ proprietario  | Diritto di cambiare il proprietario nel descrittore di sicurezza dell'oggetto.                                                                                                                                                                                                                                                                           |



 

Winnt. h definisce inoltre le seguenti combinazioni di costanti dei diritti di accesso standard.



| Costante                   | Significato                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| \_tutti i diritti standard \_      | Combina DELETE, READ \_ Control, Write \_ DAC, Write \_ Owner e Synchronize Access. |
| \_diritti di \_ esecuzione standard  | Attualmente definito per il controllo di lettura uguale \_ .                                         |
| \_diritti di \_ lettura standard     | Attualmente definito per il controllo di lettura uguale \_ .                                         |
| \_diritti standard \_ richiesti | Combina l'accesso DELETE, READ \_ Control, Write \_ DAC e Write \_ owner.              |
| \_scrittura diritti \_ standard    | Attualmente definito per il controllo di lettura uguale \_ .                                         |



 

 

 
