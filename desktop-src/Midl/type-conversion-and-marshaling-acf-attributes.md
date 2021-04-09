---
title: Type-Conversion e marshalling degli attributi ACF
description: Usare questi attributi per controllare la modalità di trasmissione dei dati in rete.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- MIDL, attributi, conversione di tipi e marshalling di ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14367be3df97cc1185fca64e46aafe1d342f3526
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955717"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a>Type-Conversion e marshalling degli attributi ACF

Usare questi attributi per controllare la modalità di trasmissione dei dati in rete.



| Attributo                                        | Utilizzo                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**codifica**](encode.md)[ decodifica](decode.md) | Indica a MIDL di esporre le routine di serializzazione di tipo o routine (selezione) generate per gli stub. L'applicazione client può chiamare le routine per effettuare il marshalling dei dati in base al valore.                                                                                                                                                                                                                                                                                  |
| [**rappresenta \_ come**](represent-as.md)            | Specifica la modalità di rappresentazione di un tipo di dati in transito, quando la natura esatta del tipo di dati di un client non è importante per il server, perché richiede solo i dati stessi e non la struttura effettiva, oppure il tipo di client effettivo è sconosciuto a MIDL in fase di compilazione. Se, ad esempio, l'applicazione client usa un elenco collegato di numeri a virgola mobile, è possibile specificare che la rappresentazione Wire di tale elenco sia una matrice di tipo [**float**](float.md). |
| [**\_marshalling utente**](user-marshal.md)            | Controlla il modo in cui i dati vengono trasmessi in rete implementando routine di marshalling personalizzate. Questo attributo è utile se si dispone di un tipo di dati sconosciuto a MIDL o se si passano informazioni tra le piattaforme big-endian e Little-endian.                                                                                                                                                                                                                 |



 

Gli attributi di marshalling DCE [**in \_ linea**](in-line.md) e non in [**\_ \_ linea**](out-of-line.md) non sono implementati in Microsoft RPC. Il compilatore MIDL esegue automaticamente il marshalling dei tipi di dati complessi out-of-line.

 

 




