---
title: Conversione in Java da C++
description: Utilizzando il linguaggio di programmazione C++, gli sviluppatori possono accedere direttamente alla memoria che archivia una determinata variabile. I puntatori alla memoria forniscono questo accesso diretto. In Java, i puntatori vengono gestiti per l'utente.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395410"
---
# <a name="translating-to-java-from-c"></a>Conversione in Java da C++

Utilizzando il linguaggio di programmazione C++, gli sviluppatori possono accedere direttamente alla memoria che archivia una determinata variabile. I puntatori alla memoria forniscono questo accesso diretto. In Java, i puntatori vengono gestiti per l'utente.

Nei tipi di dati compositi Java, **struct**, **Union** e **typedef** vengono gestiti esclusivamente tramite l'utilizzo delle classi. Il tipo di dati **Variant** C++, ad esempio, esegue il mapping a **com. ms. com. Variant** in Java.

In C++, le stringhe sono una matrice di caratteri. In Java le stringhe sono oggetti. I metodi che agiscono sulle stringhe gestiscono la stringa come oggetto completo.

I metodi COM restituiscono un valore noto come **HRESULT**, ovvero un codice di errore a 32 bit. Il supporto Java per Microsoft Internet Explorer definisce una classe, **com. ms. com. COMException**, che esegue il wrapping del codice di errore **HRESULT** .

Java non supporta i tipi di dati senza segno ad eccezione di **char**, che è un Unsigned Integer a 16 bit. I metodi che accettano o restituiscono altri tipi di dati non firmati non possono essere usati da Java.

Java non supporta le matrici multidimensionali. I metodi che accettano o restituiscono matrici multidimensionali non sono disponibili in Java.

Non è possibile eseguire il cast dei valori booleani in Java a 0 e 1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in Java](translating-to-java.md)
</dt> </dl>

 

 




