---
title: Conversione in Visual Basic da C++
description: Conversione in Visual Basic da C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298423"
---
# <a name="translating-to-visual-basic-from-c"></a>Conversione in Visual Basic da C++

Utilizzando il linguaggio di programmazione C++, gli sviluppatori possono accedere direttamente alla memoria che archivia una determinata variabile. I puntatori alla memoria forniscono questo accesso diretto. In Visual Basic, i puntatori vengono gestiti per l'utente. Un parametro dichiarato come puntatore a **int** in C++, ad esempio, è equivalente a un parametro dichiarato in Visual Basic come un integer **ByRef** ****.

Un parametro dichiarato **come stringa** in Visual Basic viene dichiarato come puntatore a un **BSTR** in C++. L'impostazione di un puntatore di stringa su **null** in C++ equivale a impostare la stringa sulla costante **vbNullString** in Visual Basic. Il passaggio di una stringa di lunghezza zero ("") a una funzione progettata per la ricezione di **valori null** non funziona, poiché viene passato un puntatore a una stringa di lunghezza zero anziché a un puntatore zero.

C++ supporta i contenitori di dati, ovvero le strutture e le unioni, che non hanno equivalenti nelle prime versioni di Visual Basic. Per questo motivo, gli oggetti COM in genere incapsulano informazioni che in genere sono archiviate in strutture e unioni nelle classi di oggetti. Alcuni oggetti COM, tuttavia, possono contenere strutture, causando la inaccessibilità di parti dei metodi o delle funzionalità dell'oggetto per Visual Basic.

Alcuni tipi di dati C++ non sono supportati in Visual Basic, ad esempio tipi senza segno e tipi **HWND** . I metodi che accettano o restituiscono questi tipi di dati non sono disponibili in Visual Basic.

Visual Basic usa tipi di dati compatibili con l'automazione come tipi di dati interni. I tipi di dati C++ compatibili con l'automazione sono pertanto compatibili anche con Visual Basic. I tipi di dati che non sono compatibili con l'automazione potrebbero non essere in grado di essere convertiti in Visual Basic.

Nella tabella seguente sono elencati i tipi di dati supportati da Visual Basic e dai rispettivi equivalenti **VarType** . **VarType** è un'enumerazione che elenca i tipi Variant di automazione.



| Tipo di dati di Visual Basic  | Equivalente VARTYPE                |
|-------------------------|-----------------------------------|
| **Integer**<br/>  | 16 bit, firmato, VT \_ I2<br/> |
| **Long**<br/>     | 32 bit, firmato, VT \_ I4<br/> |
| **Data**<br/>     | \_Data VT<br/>               |
| **Valuta**<br/> | \_CY VT<br/>                 |
| **Object**<br/>   | \*\_invio VT<br/>         |
| **Stringa**<br/>   | \_BSTR VT<br/>               |
| **Boolean**<br/>  | \_bool VT<br/>               |
| **Valuta**<br/> | \_decimale VT<br/>            |
| **Singolo**<br/>   | \_R4 VT<br/>                 |
| **Double**<br/>   | VT \_ R8<br/>                 |
| **Decimale**<br/>  | \_decimale VT<br/>            |
| **Byte**<br/>     | \_decimale VT<br/>            |
| **Variante**<br/>  | \_variante VT<br/>            |



 

Tutti i parametri in Visual Basic, a meno che non siano contrassegnati con la parola chiave **ByVal**, vengono passati per riferimento (come puntatori) anziché per valore.

C++ e Visual Basic differiscono leggermente per la rappresentazione delle proprietà. In C++ le proprietà sono rappresentate come un set di funzioni di accesso, una che imposta il valore della proprietà e una che recupera il valore della proprietà. In Visual Basic le proprietà sono rappresentate come un singolo elemento che può essere utilizzato per recuperare o impostare il valore della proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 





