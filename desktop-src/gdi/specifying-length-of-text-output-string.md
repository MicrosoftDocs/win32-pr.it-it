---
description: Diverse funzioni di tipo di carattere e di output di testo hanno un parametro che specifica la lunghezza della stringa di output di testo. Un esempio tipico è il parametro cchText di DrawTextEx.
ms.assetid: 695fd0f9-abd4-4666-acad-2c409624ddc6
title: Specifica della lunghezza della stringa di output di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35a673a23a310da33536f389c85a44af68b895e4f05e0a0f835656e7bc3fbd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885949"
---
# <a name="specifying-length-of-text-output-string"></a>Specifica della lunghezza della stringa di output di testo

Diverse funzioni di tipo di carattere e di output di testo hanno un parametro che specifica la lunghezza della stringa di output di testo. Un esempio tipico è il *parametro cchText* di [**DrawTextEx**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa).

Ognuna di queste funzioni ha sia una versione "ANSI" che una versione Unicode (ad esempio, [**DrawTextExA**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa) e **DrawTextExW,** rispettivamente). Per la versione "ANSI" di ogni funzione, la lunghezza viene specificata come conteggio BYTE e per la funzione Unicode viene specificata come conteggio WORD.

È tradizionale pensare a questo come a un "numero di caratteri". Questo è in genere accurato per molte lingue, incluso l'inglese, ma non è accurato in generale. Nelle stringhe "ANSI", i caratteri nelle code pages [SBCS](../intl/single-byte-character-sets.md) accettano un byte ciascuno, ma la maggior parte dei caratteri nelle code pages [DBCS](../intl/double-byte-character-sets.md) accetta due byte. Analogamente, la maggior parte dei caratteri Unicode attualmente definiti risiede nel piano BMP (Basic Multilingual Plane) e le relative rappresentazioni UTF-16 rientrano in un'unica parola, ma i caratteri supplementari sono rappresentati in Unicode da "surrogati", che richiedono due WORD.

Ognuna di queste funzioni accetta un conteggio di lunghezza. Per la versione "ANSI" di ogni funzione, la lunghezza viene specificata come lunghezza byte count di una stringa che non include il terminatore **NULL.** Per la funzione Unicode, il conteggio della lunghezza è il numero di byte diviso per sizeof(WCHAR), che è 2, senza includere il terminatore **NULL.** Il conteggio dei caratteri è il conteggio del numero di caratteri, che potrebbe non essere uguale al conteggio della lunghezza della stringa. In alcuni casi, i caratteri accettano più byte per ANSI (ad esempio, carattere [DBCS)](../intl/double-byte-character-sets.md) e più DI WORD per Unicode (ad esempio, caratteri surrogati). Inoltre, il numero di glifi potrebbe non essere uguale al numero di caratteri perché più caratteri potrebbero essere compositi per creare un glifo. Il conteggio della lunghezza è la quantità di dati. Il numero di caratteri è il numero di unità elaborate come un'unica entità. I glifi sono gli elementi di cui viene eseguito il rendering. Ad esempio, in Unicode è possibile avere una stringa di lunghezza pari a 3, ovvero 2 caratteri e che comporta il rendering di 1 glifo. In genere, tuttavia, la maggior parte delle stringhe Unicode, il numero di caratteri e il numero di glifi sottoposti a rendering sono uguali.

È possibile usare \_ tcslen() per ottenere la lunghezza della stringa. Per ANSI, \_ tcslen() restituisce il numero di byte. Per Unicode, \_ tcslen() restituisce il numero di WCHAR (ovvero WORD).

I caratteri di elaborazione speciali, ad esempio tabulazioni e trattini non sempre disegnati, possono influire sull'output disegnato. Vengono inclusi nella lunghezza della stringa e nei conteggi dei caratteri, ma potrebbero non essere rappresentati direttamente da un glifo sottoposto a rendering.

Alcune di queste funzioni consentono al chiamante di specificare la lunghezza come -1 per indicare che la stringa è con terminazione Null. in tal caso la funzione calcola automaticamente il numero di caratteri. Non tutte le funzioni offrono questa funzionalità. Che viene specificato in base a funzione per funzione; Vedere la documentazione relativa alle singole funzioni.

 

 
