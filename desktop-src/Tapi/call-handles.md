---
description: Come indicato nella panoramica dell'identificatore di sessione, un handle di chiamata è il mezzo mediante il quale un'applicazione TAPI 2,2 identifica una determinata sessione di comunicazione.
ms.assetid: 5f6a7adf-c074-4bf6-9828-76604eb7609c
title: Handle di chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacad5b73d9d22caa006b734acaf8b992203d7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308087"
---
# <a name="call-handles"></a>Handle di chiamata

Come indicato nella panoramica dell' [identificatore di sessione](./session-identifier-ovr.md) , un handle di chiamata è il mezzo mediante il quale un'applicazione TAPI 2,2 identifica una determinata sessione di comunicazione. Quando un'applicazione avvia una sessione, TAPI restituisce un handle di chiamata per l'uso in ulteriori operazioni o query. Quando un'applicazione riceve una notifica di una sessione in ingresso, TAPI passa anche un handle di chiamata.

Dopo che una sessione è terminata e lo stato della sessione è inattivo, l'handle di chiamata rimane valido fino a quando l'applicazione non dealloca l'handle o la riga non viene chiusa. La riga potrebbe essere chiusa dall'applicazione o potrebbe ricevere un messaggio di [**\_ chiusura riga**](line-close.md) . Se una riga è chiusa, tutti gli handle di chiamata alle chiamate sulla riga diventano immediatamente non validi.

Quando una chiamata viene ripristinata allo stato *inattivo* , l'applicazione è ancora in grado di leggere la struttura e lo stato delle informazioni della chiamata. Questo consente alle applicazioni di usare operazioni come [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) per recuperare le informazioni sulle chiamate a scopo di registrazione.

Quando l'applicazione non viene utilizzata ulteriormente per l'handle di una chiamata inattiva, deve chiamare [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) per liberare la memoria allocata dal sistema relativa alla chiamata. TAPI alloca memoria per ogni chiamata per ogni applicazione che dispone di un handle per la chiamata. È probabile che i provider di servizi allocheranno memoria per conservare anche le informazioni sulle chiamate. La deallocazione dell'handle di chiamata di un'applicazione consente alla libreria e al provider di servizi di recuperare tali risorse di memoria. L'handle di un'applicazione per una chiamata diventa void dopo una deallocazione riuscita.

L'applicazione deve disporre di memoria libera relativa alla chiamata allocata per i propri scopi.

 

 
