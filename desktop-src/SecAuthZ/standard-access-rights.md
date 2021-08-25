---
description: Ogni tipo di oggetto a protezione diretta ha un set di diritti di accesso che corrispondono a operazioni specifiche di tale tipo di oggetto.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Diritti di accesso standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56067a4ed31f9506aee0b326e82a9bd5b4b49b02d12e6d401cc04f8262b19da0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907111"
---
# <a name="standard-access-rights"></a>Diritti di accesso standard

Ogni tipo di oggetto a protezione diretta ha un set di diritti di accesso che corrispondono a operazioni specifiche di tale tipo di oggetto. Oltre a questi diritti di accesso specifici degli oggetti, esiste un set di diritti di accesso standard che corrispondono alle operazioni comuni alla maggior parte dei tipi di oggetti a protezione diretta.

Il [formato della maschera di accesso](access-mask-format.md) include un set di bit per i diritti di accesso standard. Le costanti Windows seguenti per i diritti di accesso standard sono definite in Winnt.h.



| Costante      | Significato                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE        | Diritto di eliminare l'oggetto.                                                                                                                                                                                                                                                                                                              |
| CONTROLLO \_ LETTURA | Diritto di leggere le informazioni nel descrittore di sicurezza dell'oggetto [*,*](/windows/desktop/SecGloss/s-gly)senza includere le informazioni nell'elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL). |
| SYNCHRONIZE   | Diritto di utilizzare l'oggetto per la sincronizzazione. Ciò consente a un thread di attendere finché l'oggetto non si trova nello stato segnalato. Alcuni tipi di oggetto non supportano questo diritto di accesso.                                                                                                                                                                |
| APPLICAZIONE \_ LIVELLO DATI WRITE    | Diritto di modificare l'elenco [*di controllo*](/windows/desktop/SecGloss/d-gly) di accesso discrezionale (DACL) nel descrittore di sicurezza dell'oggetto.                                                                                                                    |
| WRITE \_ OWNER  | Diritto di cambiare il proprietario nel descrittore di sicurezza dell'oggetto.                                                                                                                                                                                                                                                                           |



 

Winnt.h definisce anche le combinazioni seguenti delle costanti dei diritti di accesso standard.



| Costante                   | Significato                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| DIRITTI STANDARD \_ \_ TUTTI      | Combina l'accesso DELETE, READ \_ CONTROL, WRITE \_ DAC, WRITE \_ OWNER e SYNCHRONIZE. |
| ESECUZIONE \_ DEI DIRITTI \_ STANDARD  | Attualmente definito come uguale a READ \_ CONTROL.                                         |
| DIRITTI STANDARD \_ \_ DI LETTURA     | Attualmente definito come uguale a READ \_ CONTROL.                                         |
| DIRITTI \_ STANDARD \_ RICHIESTI | Combina l'accesso DELETE, READ \_ CONTROL, WRITE \_ DAC e WRITE \_ OWNER.              |
| SCRITTURA \_ DEI DIRITTI \_ STANDARD    | Attualmente definito come uguale a READ \_ CONTROL.                                         |



 

 

 
