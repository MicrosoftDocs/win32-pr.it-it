---
title: Conversione in C++ da Visual Basic
description: Visual Basic gestisce i puntatori in modo implicito. In C++, l'applicazione è responsabile dell'esecuzione di qualsiasi aritmetica del puntatore necessaria.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221388"
---
# <a name="translating-to-c-from-visual-basic"></a>Conversione in C++ da Visual Basic

Visual Basic gestisce i puntatori in modo implicito. In C++, l'applicazione è responsabile dell'esecuzione di qualsiasi aritmetica del puntatore necessaria.

Per impostazione predefinita, Visual Basic passa i parametri per riferimento, come puntatori. I parametri che devono essere passati solo per valore sono specificati dalla parola chiave **ByVal**. Un parametro **ByVal** â  **Integer** in Visual Basic, ad esempio, è equivalente a un parametro **short** in C++, mentre un parametro **ByRef** â  **Integer** in Visual Basic è equivalente a un parametro **short \*** .

Un parametro dichiarato **come stringa** in Visual Basic viene dichiarato come puntatore a un **BSTR** in C++. L'impostazione di un puntatore di stringa su **null** in C++ equivale a impostare la stringa sulla costante **vbNullString** in Visual Basic. Il passaggio di una stringa di lunghezza zero ("") a una funzione progettata per la ricezione di **valori null** non funziona perché passa un puntatore a una stringa di lunghezza zero anziché a un puntatore zero.

C++ e Visual Basic differiscono leggermente per la rappresentazione delle proprietà. In C++ le proprietà sono rappresentate come un set di funzioni di accesso, una che imposta il valore della proprietà e una che recupera il valore della proprietà. In Visual Basic le proprietà sono rappresentate come un singolo elemento che può essere utilizzato per recuperare o impostare il valore della proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in C++](translating-to-c--.md)
</dt> </dl>

 

 




