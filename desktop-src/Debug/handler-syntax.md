---
description: In questa sezione vengono descritte la sintassi e l'utilizzo della gestione strutturata delle eccezioni come implementato nel compilatore di ottimizzazione Microsoft C/C++. Le parole chiave seguenti vengono interpretate dal compilatore come parte del meccanismo di gestione delle eccezioni strutturato.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Sintassi del gestore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877325"
---
# <a name="handler-syntax"></a>Sintassi del gestore

In questa sezione vengono descritte la sintassi e l'utilizzo della gestione strutturata delle eccezioni come implementato nel compilatore di ottimizzazione Microsoft C/C++. Le parole chiave seguenti vengono interpretate dal compilatore come parte del meccanismo di gestione delle eccezioni strutturato.



| Parola chiave         | Descrizione                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_\_provare**     | Inizia un corpo sorvegliato del codice. Usato con la parola chiave **\_ \_ except** per costruire un [gestore di eccezioni](exception-handler-syntax.md)o con la parola chiave **\_ \_ finally** per costruire un gestore di [terminazione](termination-handler-syntax.md). |
| **\_\_ad eccezione**  | Inizia un blocco di codice che viene eseguito solo quando si verifica un'eccezione all'interno del blocco **\_ \_ try** associato.                                                                                                                                   |
| **\_\_Infine** | Inizia un blocco di codice che viene eseguito ogni volta che il flusso di controllo lascia il blocco **\_ \_ try** associato.                                                                                                                                    |
| **\_\_lasciare**   | Consente la chiusura immediata del blocco **\_ \_ try** senza causare la terminazione anomala e la riduzione delle prestazioni.                                                                                                                      |



 

Il compilatore interpreta inoltre le funzioni [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md)e [**AbnormalTermination**](abnormaltermination.md) come parole chiave e il loro utilizzo al di fuori della sintassi di gestione delle eccezioni appropriata genera un errore del compilatore. Di seguito sono riportate brevi descrizioni di queste funzioni.



| Funzione                                                   | Descrizione                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExceptionCode**](getexceptioncode.md)               | Restituisce un codice che identifica il tipo di eccezione. Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro o dal blocco del gestore di eccezioni.                                                                                                |
| [**GetExceptionInformation**](getexceptioninformation.md) | Restituisce un puntatore a una struttura di [**\_ puntatori di eccezione**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) che contiene i puntatori al record di contesto e al record di eccezione. Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro di un gestore di eccezioni. |
| [**AbnormalTermination**](abnormaltermination.md)         | Indica se il flusso di controllo ha lasciato il blocco **\_ \_ try** associato in sequenza dopo l'esecuzione dell'ultima istruzione nel blocco. Questa funzione può essere chiamata solo dall'interno del blocco **\_ \_ finally** di un gestore di terminazione.              |



 

 

 



