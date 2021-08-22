---
description: Questa sezione descrive la sintassi e l'uso della gestione delle eccezioni strutturata implementata nel compilatore microsoft C/C++. Le parole chiave seguenti vengono interpretate dal compilatore come parte del meccanismo strutturato di gestione delle eccezioni.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Sintassi del gestore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5171a1de095faa0c3362a7998903d31f90eb630e51c5ec16e7e77d467117715c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260611"
---
# <a name="handler-syntax"></a>Sintassi del gestore

Questa sezione descrive la sintassi e l'uso della gestione delle eccezioni strutturata implementata nel compilatore microsoft C/C++. Le parole chiave seguenti vengono interpretate dal compilatore come parte del meccanismo strutturato di gestione delle eccezioni.



| Parola chiave         | Descrizione                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_\_Provare**     | Avvia un corpo di codice sorvegliato. Usato con la **\_ \_ parola chiave except** per costruire un gestore [eccezioni](exception-handler-syntax.md)o con la **\_ \_ parola chiave finally** per costruire un gestore di [terminazione](termination-handler-syntax.md). |
| **\_\_Tranne**  | Avvia un blocco di codice che viene eseguito solo quando si verifica un'eccezione all'interno del blocco **\_ \_ try** associato.                                                                                                                                   |
| **\_\_Infine** | Avvia un blocco di codice che viene eseguito ogni volta che il flusso di controllo lascia il blocco **\_ \_ try** associato.                                                                                                                                    |
| **\_\_Lasciare**   | Consente la terminazione immediata del blocco **\_ \_ try** senza causare la terminazione anomala e la relativa penalità per le prestazioni.                                                                                                                      |



 

Il compilatore interpreta anche le funzioni [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md)e [**AbnormalTermination**](abnormaltermination.md) come parole chiave e il loro uso all'esterno della sintassi di gestione delle eccezioni appropriata genera un errore del compilatore. Di seguito sono riportate brevi descrizioni di queste funzioni.



| Funzione                                                   | Descrizione                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExceptionCode**](getexceptioncode.md)               | Restituisce un codice che identifica il tipo di eccezione. Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro o del blocco del gestore eccezioni.                                                                                                |
| [**GetExceptionInformation**](getexceptioninformation.md) | Restituisce un puntatore a una [**struttura EXCEPTION \_ POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) contenente puntatori al record di contesto e al record dell'eccezione. Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro di un gestore eccezioni. |
| [**AbnormalTermination**](abnormaltermination.md)         | Indica se il flusso di controllo ha lasciato il blocco **\_ \_ try** associato in sequenza dopo l'esecuzione dell'ultima istruzione nel blocco. Questa funzione può essere chiamata solo dall'interno del **\_ \_ blocco finally** di un gestore di terminazione.              |



 

 

 



