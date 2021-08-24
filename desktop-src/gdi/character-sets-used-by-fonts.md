---
description: Tutti i tipi di carattere usano un set di caratteri. Un set di caratteri contiene segni di punteggiatura, numeri, lettere maiuscole e minuscole e tutti gli altri caratteri stampabili. Ogni elemento di un set di caratteri è identificato da un numero.
ms.assetid: 7989c59e-2ec6-4d1a-bb86-f4037ca32764
title: Set di caratteri usati dai tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ec30a82c08a0b9ac1162034b6308bb68ff7dc1c6469e5e73bad2838b528eef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779361"
---
# <a name="character-sets-used-by-fonts"></a>Set di caratteri usati dai tipi di carattere

Tutti i tipi di carattere usano un set di caratteri. Un set di caratteri contiene segni di punteggiatura, numeri, lettere maiuscole e minuscole e tutti gli altri caratteri stampabili. Ogni elemento di un set di caratteri è identificato da un numero.

La maggior parte dei set di caratteri in uso è un superset del set di caratteri ASCII degli Stati Uniti, che definisce i caratteri per i 96 valori numerici da 32 a 127. Esistono cinque gruppi principali di set di caratteri:

-   Windows
-   Unicode
-   OEM (original equipment manufacturer)
-   Simbolo
-   Specifico del fornitore

## <a name="windows-character-set"></a>Windows Set di caratteri

Il Windows set di caratteri è il set di caratteri usato più di frequente. È essenzialmente equivalente al set di caratteri ANSI. Il carattere vuoto è il primo carattere nel set Windows caratteri. Ha un valore esadecimale di 0x20 (decimale 32). L'ultimo carattere nel set Windows set di caratteri ha un valore esadecimale di 0xFF (decimale 255).

Molti tipi di carattere specificano un carattere predefinito. Ogni volta che viene effettuata una richiesta per un carattere che non è nel tipo di carattere, il sistema fornisce questo carattere predefinito. Molti tipi di carattere che Windows set di caratteri specificano il punto (.) come carattere predefinito. I tipi di carattere TrueType e OpenType usano in genere una casella aperta come carattere predefinito.

I tipi di carattere usano un carattere di interruzione denominato quad per separare le parole e giustificare il testo. La maggior parte dei tipi di Windows set di caratteri specifica che il carattere vuoto verrà utilizzato come carattere di interruzione.

## <a name="unicode-character-set"></a>Set di caratteri Unicode.

Il Windows set di caratteri usa 8 bit per rappresentare ogni carattere. Pertanto, il numero massimo di caratteri che è possibile esprimere usando 8 bit è 256 (2^8). Ciò è in genere sufficiente per le lingue occidentali, inclusi i segni diacritici usati in francese, tedesco, spagnolo e altre lingue. Tuttavia, le lingue orientali usano migliaia di caratteri separati, che non possono essere codificati usando uno schema di codifica a byte singolo. Con la proliferazione del commercio informatico, sono stati sviluppati schemi di codifica a byte doppio in modo che i caratteri fossero rappresentati in sequenze a 8 bit, a 16 bit, a 24 bit o a 32 bit. A questo scopo sono necessari algoritmi di passaggio complessi. Anche in questo caso, l'uso di set di codice diversi potrebbe produrre risultati completamente diversi in due computer diversi.

Per risolvere il problema di più schemi di codifica, è stato sviluppato lo standard Unicode per la rappresentazione dei dati. Schema di codifica di caratteri a 16 bit, Unicode può rappresentare 65.536 caratteri (2^16), sufficienti per includere tutte le lingue attualmente in commercio informatico, nonché segni di punteggiatura, simboli matematici e spazio per l'espansione. Unicode stabilisce un codice univoco per ogni carattere per garantire che la conversione dei caratteri sia sempre accurata.

## <a name="oem-character-set"></a>Set di caratteri OEM

Il set di caratteri OEM viene in genere usato nelle sessioni MS-DOS a schermo intero per la visualizzazione su schermo. I caratteri da 32 a 127 sono in genere gli stessi nei set di caratteri OEM, ASCII degli Stati Uniti Windows caratteri. Gli altri caratteri nel set di caratteri OEM (da 0 a 31 e da 128 a 255) corrispondono ai caratteri che possono essere visualizzati in una sessione MS-DOS a schermo intero. Questi caratteri sono in genere diversi da Windows caratteri.

## <a name="symbol-character-set"></a>Set di caratteri simbolo

Il set di caratteri Symbol contiene caratteri speciali usati in genere per rappresentare formule matematiche e scientifiche.

## <a name="vendor-specific-character-sets"></a>Set di caratteri specifici del fornitore

Molte stampanti e altri dispositivi di output forniscono tipi di carattere basati su set di caratteri diversi dai set di caratteri Windows e OEM, ad esempio il set di caratteri Extended Binary Coded Decimal Interchange Code (EBCDIC). Per utilizzare uno di questi set di caratteri, il driver della stampante converte dal set Windows set di caratteri al set di caratteri specifico del fornitore.

 

 



