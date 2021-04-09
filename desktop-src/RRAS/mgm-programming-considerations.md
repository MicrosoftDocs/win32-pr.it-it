---
title: Considerazioni sulla programmazione MGM
description: Quando si sviluppano client di gestione dei gruppi multicast, osservare le linee guida seguenti
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multicast, considerazioni sulla programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856505"
---
# <a name="mgm-programming-considerations"></a>Considerazioni sulla programmazione MGM

Quando si sviluppano client di gestione dei gruppi multicast, attenersi alle linee guida seguenti:

-   Le chiamate di funzione devono essere eseguite all'interno del processo del router. Se le funzioni vengono chiamate da un altro processo, i risultati non saranno validi. il client non interagisce con il gestore del gruppo multicast.
-   I client che usano l'API MGM devono fornire il proprio controllo degli errori, assicurando che solo i dati validi vengano passati al gestore del gruppo multicast. Le funzioni MGM non restituiscono messaggi di errore dettagliati sui parametri non validi. il \_ valore del parametro error non valido \_ viene restituito senza spiegazione.
-   I client devono prestare attenzione nell'uso dei blocchi durante la chiamata di funzioni MGM. Questa operazione può impedire i deadlock. Quando si chiamano le funzioni MGM, i client non devono contenere blocchi che possono essere mantenuti contemporaneamente in un callback da Gestione gruppi multicast.

 

 




