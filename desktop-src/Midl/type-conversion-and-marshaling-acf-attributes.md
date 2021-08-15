---
title: Type-Conversion e marshalling degli attributi ACF
description: Usare questi attributi per controllare la modalità di trasmissione dei dati in rete.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- ACF MIDL, attributi, conversione dei tipi e marshalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286de08a56aba5ffc7b73fc52791238a6af62b3f0545e95aedabcf79d5623464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382739"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a>Type-Conversion e marshalling degli attributi ACF

Usare questi attributi per controllare la modalità di trasmissione dei dati in rete.



| Attributo                                        | Utilizzo                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**codificare**](encode.md)[**la decodifica**](decode.md) | Indica a MIDL di esporre le routine di serializzazione di tipo o routine (pickling) generate per gli stub. L'applicazione client può chiamare tali routine per effettuare il marshalling dei dati in base al valore.                                                                                                                                                                                                                                                                                  |
| [**rappresentano \_ come**](represent-as.md)            | Specifica come verrà rappresentato un tipo di dati in transito, quando la natura esatta del tipo di dati di un client non è importante per il server (perché richiede solo i dati stessi e non la struttura effettiva) o il tipo di client effettivo è sconosciuto a MIDL in fase di compilazione. Ad esempio, se l'applicazione client usa un elenco collegato di numeri a virgola mobile, è possibile specificare che la rappresentazione cablata di tale elenco sia una matrice di tipo [**float**](float.md). |
| [**marshalling \_ utente**](user-marshal.md)            | Controlla la modalità di trasmissione dei dati in transito implementando routine di marshalling proprie. Questo attributo è utile se si dispone di un tipo di dati sconosciuto a MIDL o se si passano informazioni tra piattaforme big-endian e little-endian.                                                                                                                                                                                                                 |



 

Gli attributi di marshalling DCE [**\_ inline**](in-line.md) [**e \_ out-of-line \_**](out-of-line.md) non sono implementati in Microsoft RPC. Il compilatore MIDL effettua automaticamente il marshalling out-of-line di tipi di dati complessi.

 

 




