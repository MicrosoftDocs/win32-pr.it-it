---
title: Architettura del gestore
description: Architettura del gestore
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044816"
---
# <a name="handler-architecture"></a>Architettura del gestore

La funzione interna di un gestore di file o di flussi viene definita dal gestore stesso. Per un'applicazione, un gestore di file viene in genere visualizzato come modulo per la lettura e la scrittura di file AVI. Analogamente, un gestore di flusso viene visualizzato come modulo per la lettura e la scrittura di un tipo specifico di flusso di dati. L'interfaccia di flusso coerente rende l'origine e la destinazione del flusso non importanti per l'applicazione che utilizza il gestore.

Un gestore di file consente di accedere a un'origine dati costituita da uno o più flussi di dati. I gestori di file consentono in genere l'accesso a file su disco contenenti uno o più flussi di dati e le funzioni interne del gestore file leggono e scrivono i dati multimediali. Tuttavia, i gestori di file possono funzionare con qualsiasi origine dati, ad esempio un canale di trasmissione digitale che contiene diversi flussi di dati intermisti.

Un gestore di flusso elabora invece un tipo di dati e viene visualizzato come flusso di dati in un'applicazione. Un gestore di flusso può fornire dati che produce oppure può recuperare dati da un file o da un'origine esterna. Fornisce i dati in un formato che può essere usato dall'applicazione.

 

 




