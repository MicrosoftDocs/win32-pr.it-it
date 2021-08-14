---
description: A ogni oggetto di Active Directory è assegnato un descrittore di sicurezza.
ms.assetid: 2e4ed13f-f09e-43b4-9862-95a79c229f0c
title: Diritti di accesso ai servizi directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901c8eba5736750e0c91eb713993876c47858407110ca3c8ebc6ed8122e1b8d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913764"
---
# <a name="directory-services-access-rights"></a>Diritti di accesso ai servizi directory

A ogni oggetto di Active Directory è assegnato un [*descrittore*](/windows/desktop/SecGloss/s-gly) di sicurezza. È possibile impostare un set di diritti fiduciari specifici per gli oggetti del servizio directory all'interno di questi descrittori di sicurezza. Questi diritti sono elencati nella tabella seguente. Per altre informazioni, vedere [Controllare i diritti di accesso.](/windows/desktop/AD/control-access-rights)



| Diritti                                | Significato                                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTRL \_ DS \_ OPEN<br/>            | Aprire un oggetto DS.<br/>                                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ CREATE \_ CHILD<br/>   | Creare un oggetto DS figlio.<br/>                                                                                                                                                                                                                                                    |
| ACTRL \_ DS \_ DELETE \_ CHILD<br/>   | Eliminare un oggetto DS figlio.<br/>                                                                                                                                                                                                                                                    |
| ELENCO DI \_ DS \_ ACTRL<br/>            | Enumerare un oggetto DS.<br/>                                                                                                                                                                                                                                                       |
| ACTRL \_ DS \_ READ \_ PROP<br/>      | Leggere le proprietà di un oggetto DS.<br/>                                                                                                                                                                                                                                          |
| ACTRL \_ DS \_ WRITE \_ PROP<br/>     | Scrivere proprietà per un oggetto DS.<br/>                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ SELF<br/>            | Accesso consentito solo dopo l'esecuzione dei controlli dei diritti convalidati supportati dall'oggetto . Questo flag può essere usato da solo per eseguire tutti i controlli dei diritti convalidati dell'oggetto oppure può essere combinato con un identificatore di un diritto convalidato specifico per eseguire solo tale controllo.<br/> |
| ALBERO DI ELIMINAZIONE DI ACTRL \_ DS \_ \_<br/>    | Eliminare un albero di oggetti DS.<br/>                                                                                                                                                                                                                                                 |
| OGGETTO ACTRL \_ DS \_ \_ LIST<br/>    | Elencare un albero di oggetti DS.<br/>                                                                                                                                                                                                                                                   |
| ACTRL \_ DS \_ CONTROLLA \_ L'ACCESSO<br/> | Accesso consentito solo dopo l'esecuzione dei controlli dei diritti estesi supportati dall'oggetto . Questo flag può essere usato da solo per eseguire tutti i controlli dei diritti estesi sull'oggetto oppure può essere combinato con un identificatore di un diritto esteso specifico per eseguire solo tale controllo.<br/>    |



 

 

