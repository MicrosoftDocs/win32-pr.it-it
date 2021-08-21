---
title: Conversione in Java da C++
description: Usando il linguaggio di programmazione C++, gli sviluppatori possono accedere direttamente alla memoria in cui è archiviata una determinata variabile. I puntatori di memoria forniscono questo accesso diretto. In Java i puntatori vengono gestiti per l'utente.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73efe022fa09ce13a2d5e4e04978033fc3ab8f33abb6afb3b5abf493dab12178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047749"
---
# <a name="translating-to-java-from-c"></a>Conversione in Java da C++

Usando il linguaggio di programmazione C++, gli sviluppatori possono accedere direttamente alla memoria in cui è archiviata una determinata variabile. I puntatori di memoria forniscono questo accesso diretto. In Java i puntatori vengono gestiti per l'utente.

In Java i tipi di dati compositi **struct**, **union** e **typedef** vengono gestiti esclusivamente tramite l'uso di classi. Ad esempio, il tipo di dati **VARIANT** C++ esegue il mapping **a com.ms.com.Variant** in Java.

In C++ le stringhe sono una matrice di caratteri. In Java le stringhe sono oggetti . I metodi che agiscono sulle stringhe trattano la stringa come un oggetto completo.

I metodi COM restituiscono un valore noto come **HRESULT,** che è un codice di errore a 32 bit. Il supporto Java per Microsoft Internet Explorer definisce una **classe, com.ms.com.ComException**, che esegue il wrapping del **codice di errore HRESULT.**

Java non supporta tipi di dati senza segno ad eccezione di **char**, che è un intero senza segno a 16 bit. I metodi che accettano o restituiscono altri tipi di dati senza segno non possono essere usati da Java.

Java non supporta le matrici multidimensionali. I metodi che accettano o restituiscono matrici multidimensionali non sono disponibili in Java.

Non è possibile eseguire il cast di valori booleani in Java su 0 e 1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Traduzione in Java](translating-to-java.md)
</dt> </dl>

 

 




