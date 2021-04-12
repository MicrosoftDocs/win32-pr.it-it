---
title: Top-Level e puntatori incorporati
description: Per comprendere il modo in cui i puntatori e gli elementi dati associati vengono allocati in Microsoft RPC, è necessario distinguere tra puntatori di primo livello e puntatori incorporati.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471675"
---
# <a name="top-level-and-embedded-pointers"></a>Top-Level e puntatori incorporati

Per comprendere il modo in cui i puntatori e gli elementi dati associati vengono allocati in Microsoft RPC, è necessario distinguere tra *puntatori di primo livello* e *puntatori incorporati*. È inoltre utile fare riferimento al set di tutti i puntatori che non sono puntatori di primo livello.

I *puntatori di primo livello* sono quelli specificati come nomi dei parametri nei prototipi di funzione. I puntatori di primo livello e i relativi riferimenti sono sempre allocati nel server.

I *puntatori incorporati* sono puntatori incorporati in strutture di dati quali matrici, strutture e unioni. Quando i puntatori incorporati scrivono solo l'output in un buffer e sono null nell'input, l'applicazione server può modificare i valori in un valore diverso da null. In questo caso, gli stub client allocano la nuova memoria per questi dati.

Se il puntatore incorporato non è null nel client prima della chiamata, gli stub non allocano memoria sul client al ritorno. Al contrario, gli stub tentano di scrivere la memoria associata al puntatore incorporato nella memoria esistente sul client associato a tale puntatore, sovrascrivendo i dati già presenti.

> [!Note]  
> Per i dati letti o scritti in un buffer e che non specifica le dimensioni del buffer, la lunghezza di output deve essere minore o uguale alla lunghezza di input. Viene generata un'eccezione RPC quando viene rilevato un overflow. Per i dati di stringa, la lunghezza di output viene determinata controllando la lunghezza della stringa di input. Pertanto, le stringhe di output non possono superare la lunghezza delle stringhe di input. Le procedure consigliate consentono di evitare questo problema includendo sempre un parametro specificato per le dimensioni per indicare le dimensioni del buffer.

 

I puntatori di sola scrittura incorporati vengono descritti nella [combinazione di attributi direzionali e direzionali](combining-pointer-and-directional-attributes.md).

Il termine *puntatori a livello di nontop* fa riferimento a tutti i puntatori che non sono specificati come nomi di parametro nel prototipo di funzione, inclusi i puntatori incorporati e più livelli di puntatori annidati.

 

 




