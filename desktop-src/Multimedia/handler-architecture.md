---
title: Architettura del gestore
description: Architettura del gestore
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0da7846f31c94202d8d50ac0566c87ef5db085a0b9efb3f9250468346512db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141094"
---
# <a name="handler-architecture"></a>Architettura del gestore

La funzione interna di un gestore di file o di flusso è definita dal gestore stesso. Per un'applicazione, un gestore di file viene in genere visualizzato come modulo per leggere e scrivere file AVI. Analogamente, un gestore di flusso viene visualizzato come modulo per leggere e scrivere un tipo specifico di flusso di dati. L'interfaccia di flusso coerente rende l'origine e la destinazione del flusso non importanti per l'applicazione che usa il gestore .

Un gestore di file fornisce l'accesso a un'origine dati costituita da uno o più flussi di dati. I gestori di file forniscono in genere l'accesso ai file su disco contenenti uno o più flussi di dati e le funzioni interne del gestore di file leggono e scrivono i dati multimediali. Tuttavia, i gestori di file possono funzionare con qualsiasi origine dati, ad esempio un canale di trasmissione digitale contenente diversi flussi di dati intermingled.

Al contrario, un gestore di flusso elabora un tipo di dati e viene visualizzato come flusso di dati per un'applicazione. Un gestore di flusso può fornire dati che produce oppure può recuperare dati da un file o da un'origine esterna. Fornisce i dati in un formato che l'applicazione può usare.

 

 




