---
title: Top-Level e incorporati
description: Per comprendere come vengono allocati i puntatori e i relativi elementi dati associati in Microsoft RPC, è necessario distinguere tra puntatori di primo livello e puntatori incorporati.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28fab18cfb345587f4c152f6890d94c5177e5bd9344e542592c33e462915beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011269"
---
# <a name="top-level-and-embedded-pointers"></a>Top-Level e incorporati

Per comprendere come vengono allocati i puntatori e i relativi  elementi dati associati in Microsoft RPC, è necessario distinguere tra i puntatori di primo livello e *i puntatori incorporati.* È anche utile fare riferimento al set di tutti i puntatori che non sono puntatori di primo livello.

*I puntatori di primo livello* sono quelli specificati come nomi di parametri nei prototipi di funzione. I puntatori di primo livello e i relativi riferimenti vengono sempre allocati nel server.

*I puntatori* incorporati sono puntatori incorporati in strutture di dati quali matrici, strutture e unioni. Quando i puntatori incorporati scrivono l'output solo in un buffer e sono Null nell'input, l'applicazione server può modificare i relativi valori in valori non Null. In questo caso, gli stub client allocano nuova memoria per questi dati.

Se il puntatore incorporato non è Null nel client prima della chiamata, gli stub non allocano memoria sul client al ritorno. Al contrario, gli stub tentano di scrivere la memoria associata al puntatore incorporato nella memoria esistente nel client associato a tale puntatore, sovrascrivendo i dati già presenti.

> [!Note]  
> Per i dati letti o letti da un buffer e che non specificano le dimensioni del buffer, la lunghezza dell'output deve essere minore o uguale alla lunghezza di input. Quando viene rilevato un overflow, viene generata un'eccezione RPC. Per i dati stringa, la lunghezza dell'output viene determinata controllando la lunghezza della stringa di input. Pertanto, le stringhe di output non possono superare la lunghezza delle stringhe di input. Per evitare questo problema, è consigliabile includere sempre un parametro specificato dalle dimensioni per indicare le dimensioni del buffer.

 

I puntatori incorporati di sola scrittura sono descritti in [Combinazione di puntatore e attributi direzionali.](combining-pointer-and-directional-attributes.md)

Il termine *puntatori a* livello non superiore si riferisce a tutti i puntatori non specificati come nomi di parametro nel prototipo di funzione, inclusi sia i puntatori incorporati che più livelli di puntatori annidati.

 

 




