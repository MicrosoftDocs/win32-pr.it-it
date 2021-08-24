---
title: Considerazioni sulla programmazione MGM
description: Quando si sviluppano client di gestione di gruppi multicast, osservare le linee guida seguenti
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multicast, considerazioni sulla programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a749406384068cc7dce54fab237c261926149aaf9b2fbdca23327c7b75f3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029631"
---
# <a name="mgm-programming-considerations"></a>Considerazioni sulla programmazione MGM

Quando si sviluppano client di gestione di gruppi multicast, osservare le linee guida seguenti:

-   Le chiamate di funzione devono essere effettuate dall'interno del processo del router. Se le funzioni vengono chiamate da un altro processo, i relativi risultati non saranno validi. il client non interagirà con il gestore di gruppi multicast.
-   I client che usano l'API MGM devono fornire il proprio controllo degli errori, assicurando che al gestore di gruppi multicast siano passati solo dati validi. Le funzioni MGM non restituiscono messaggi di errore dettagliati sui parametri non validi. Il valore ERROR \_ INVALID \_ PARAMETER viene restituito senza spiegazione.
-   I client devono prestare attenzione nell'uso dei blocchi durante la chiamata alle funzioni MGM. In questo modo è possibile evitare deadlock. Quando si chiamano funzioni MGM, i client non devono contenere blocchi che potrebbero essere mantenuti contemporaneamente in un callback dal gestore di gruppi multicast.

 

 




