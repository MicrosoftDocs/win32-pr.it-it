---
description: Diverse funzioni di tipo carattere e output di testo hanno un parametro che specifica la lunghezza della stringa di output di testo. Un esempio tipico è il parametro cchText di DrawTextEx.
ms.assetid: 695fd0f9-abd4-4666-acad-2c409624ddc6
title: Specifica della lunghezza della stringa di output di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c120026d1b65170b6fe35bc65400280f6f1ffa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968271"
---
# <a name="specifying-length-of-text-output-string"></a>Specifica della lunghezza della stringa di output di testo

Diverse funzioni di tipo carattere e output di testo hanno un parametro che specifica la lunghezza della stringa di output di testo. Un esempio tipico è il parametro *cchText* di [**DrawTextEx**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa).

Ognuna di queste funzioni ha una versione "ANSI" e una versione Unicode, ad esempio [**DrawTextExA**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa) e **DrawTextExW**, rispettivamente. Per la versione "ANSI" di ogni funzione, la lunghezza viene specificata come numero di BYTE e per la funzione Unicode viene specificata come conteggio di parole.

Si tratta di un'operazione tradizionale che può essere considerata come un "conteggio dei caratteri". Questo è in genere accurato per molte lingue, incluso l'inglese, ma in generale non è accurato. Nelle stringhe "ANSI", i caratteri nelle tabelle codici [SBCS](../intl/single-byte-character-sets.md) accettano un byte ogni, ma la maggior parte dei caratteri nelle tabelle codici [DBCS](../intl/double-byte-character-sets.md) accetta due byte. Analogamente, la maggior parte dei caratteri Unicode attualmente definiti si trova nel piano di base multilingue (BMP) e le relative rappresentazioni UTF-16 si adattano a una parola, ma i caratteri supplementari sono rappresentati in Unicode da' ' surrogati '', che richiedono due parole.

Ognuna di queste funzioni impiega un conteggio di lunghezza. Per la versione "ANSI" di ogni funzione, la lunghezza viene specificata come lunghezza del conteggio dei BYTE di una stringa che non include il carattere di terminazione **null** . Per la funzione Unicode, il conteggio di lunghezza è il numero di byte diviso per sizeof (WCHAR), ovvero 2, escluso il carattere di terminazione **null** . Il conteggio dei caratteri è il conteggio del numero di caratteri, che potrebbe non corrispondere al numero di lunghezza della stringa. In alcuni casi, i caratteri accettano più di un BYTE per ANSI (ad esempio, il carattere [DBCS](../intl/double-byte-character-sets.md) ) e più di una parola per Unicode, ad esempio i caratteri surrogati. Inoltre, il numero di glifi potrebbe non essere uguale al numero di caratteri perché più caratteri potrebbero essere compositi per creare un glifo. Il numero di lunghezze è la quantità di dati. Il conteggio dei caratteri è il numero di unità elaborate come un'unica entità. I glifi sono elementi di cui viene eseguito il rendering. In Unicode, ad esempio, è possibile avere una stringa con lunghezza 3, che è di 2 caratteri e che comporta il rendering di 1 glifo. Tuttavia, in genere la maggior parte delle stringhe Unicode, il numero di caratteri e il numero di glifi sottoposti a rendering sono uguali.

È possibile usare \_ tcslen () per ottenere la lunghezza della stringa. Per ANSI, \_ tcslen () restituisce il numero di byte. Per Unicode, \_ tcslen () restituisce il numero di WCHAR (ovvero parole).

I caratteri di elaborazione speciali come le schede e i trattini morbidi che non sono sempre disegnati possono influenzare l'output disegnato. Vengono inclusi nei conteggi della lunghezza della stringa e dei caratteri, ma potrebbero non essere rappresentati direttamente da un glifo sottoposto a rendering.

Alcune di queste funzioni consentono al chiamante di specificare la lunghezza di-1 per indicare che la stringa è con terminazione null. in tal caso, la funzione calcolerà automaticamente il numero di caratteri. Non tutte le funzioni offrono questa funzionalità. Viene specificato in base alla funzione. vedere la documentazione delle singole funzioni.

 

 
