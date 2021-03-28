---
description: Tutti i tipi di carattere utilizzano un set di caratteri. Un set di caratteri contiene segni di punteggiatura, numeri, lettere maiuscole e minuscole e tutti gli altri caratteri stampabili. Ogni elemento di un set di caratteri viene identificato da un numero.
ms.assetid: 7989c59e-2ec6-4d1a-bb86-f4037ca32764
title: Set di caratteri usati dai tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33c4c5cc193c4474b39113acdedafec699456e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978799"
---
# <a name="character-sets-used-by-fonts"></a>Set di caratteri usati dai tipi di carattere

Tutti i tipi di carattere utilizzano un set di caratteri. Un set di caratteri contiene segni di punteggiatura, numeri, lettere maiuscole e minuscole e tutti gli altri caratteri stampabili. Ogni elemento di un set di caratteri viene identificato da un numero.

La maggior parte dei set di caratteri in uso sono i superset del set di caratteri ASCII degli Stati Uniti, che definisce i caratteri per i valori numerici 96 da 32 a 127. Sono disponibili cinque gruppi principali di set di caratteri:

-   Windows
-   Unicode
-   OEM (Original Equipment Manufacturer)
-   Simbolo
-   Specifico del fornitore

## <a name="windows-character-set"></a>Set di caratteri di Windows

Il set di caratteri di Windows è il set di caratteri utilizzato più di frequente. È essenzialmente equivalente al set di caratteri ANSI. Il carattere Blank è il primo carattere del set di caratteri di Windows. Il valore esadecimale è 0x20 (decimale 32). L'ultimo carattere nel set di caratteri di Windows ha un valore esadecimale di 0xFF (decimale 255).

Molti tipi di carattere specificano un carattere predefinito. Ogni volta che viene effettuata una richiesta per un carattere non incluso nel tipo di carattere, il sistema fornisce questo carattere predefinito. Molti tipi di carattere che usano il set di caratteri di Windows specificano il punto (.) come carattere predefinito. I tipi di carattere TrueType e OpenType utilizzano in genere una casella di apertura come carattere predefinito.

I tipi di carattere utilizzano un carattere di break denominato quad per separare le parole e giustificare il testo. La maggior parte dei tipi di carattere che usano il set di caratteri di Windows specifica che il carattere vuoto fungerà da carattere di rottura.

## <a name="unicode-character-set"></a>Set di caratteri Unicode.

Il set di caratteri di Windows utilizza 8 bit per rappresentare ogni carattere; Pertanto, il numero massimo di caratteri che è possibile esprimere utilizzando 8 bit è 256 (2 ^ 8). Questa operazione è in genere sufficiente per le lingue occidentali, inclusi i segni diacritici utilizzati in francese, tedesco, spagnolo e altre lingue. Tuttavia, le lingue orientali utilizzano migliaia di caratteri separati, che non possono essere codificati utilizzando uno schema di codifica a byte singolo. Con la proliferazione del commercio dei computer, sono stati sviluppati schemi di codifica a doppio byte in modo che i caratteri potessero essere rappresentati in sequenze a 8 bit, a 16 bit, a 24 bit o a 32 bit. È necessario un algoritmo di passaggio complicato; anche in questo caso, l'uso di set di codice diversi può produrre risultati completamente diversi in due computer diversi.

Per risolvere il problema di più schemi di codifica, è stato sviluppato lo standard Unicode per la rappresentazione dei dati. Uno schema di codifica dei caratteri a 16 bit, Unicode può rappresentare 65.536 (2 ^ 16) caratteri, che è sufficiente per includere attualmente tutte le lingue nel computer Commerce, nonché segni di punteggiatura, simboli matematici e spazio per l'espansione. Unicode stabilisce un codice univoco per ogni carattere per garantire che la conversione dei caratteri sia sempre precisa.

## <a name="oem-character-set"></a>Set di caratteri OEM

Il set di caratteri OEM viene in genere usato nelle sessioni MS-DOS a schermo intero per la visualizzazione dello schermo. I caratteri da 32 a 127 sono in genere gli stessi nei set di caratteri OEM, US ASCII e Windows. Gli altri caratteri del set di caratteri OEM (da 0 a 31 e da 128 a 255) corrispondono ai caratteri che possono essere visualizzati in una sessione MS-DOS a schermo intero. Questi caratteri sono generalmente diversi dai caratteri di Windows.

## <a name="symbol-character-set"></a>Set di caratteri simbolo

Il set di caratteri simbolo contiene caratteri speciali in genere utilizzati per rappresentare formule matematiche e scientifiche.

## <a name="vendor-specific-character-sets"></a>Set di caratteri specifici del fornitore

Molte stampanti e altri dispositivi di output forniscono tipi di carattere basati su set di caratteri diversi dall'esempio setsfor Windows e OEM, il set di caratteri Extended Binary Coded Decimal Interchange Code (EBCDIC). Per utilizzare uno di questi set di caratteri, il driver della stampante viene convertito dal set di caratteri di Windows al set di caratteri specifico del fornitore.

 

 



