---
description: Unicode è uno standard di codifica di caratteri in tutto il mondo. Il sistema usa esclusivamente Unicode per la manipolazione di caratteri e stringhe. Per una descrizione dettagliata di tutti gli aspetti di Unicode, vedere lo standard Unicode.
ms.assetid: ca5bcdee-ea13-4745-a565-5426c462892d
title: Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88facae63fbb365fd6f38cb09464de735e0759b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319492"
---
# <a name="unicode"></a>Unicode

Unicode è uno standard di codifica di caratteri in tutto il mondo. Il sistema usa esclusivamente Unicode per la manipolazione di caratteri e stringhe. Per una descrizione dettagliata di tutti gli aspetti di Unicode, vedere [lo standard Unicode](https://www.unicode.org/standard/standard.html).

Rispetto ai meccanismi meno recenti per la gestione di dati di tipo carattere e stringa, Unicode semplifica la localizzazione del software e migliora l'elaborazione del testo multilingue. Usando Unicode per rappresentare i dati di tipo carattere e stringa nelle applicazioni, è possibile abilitare le funzionalità di scambio universale dei dati per il marketing globale, usando un unico file binario per ogni possibile codice carattere. Unicode esegue le operazioni seguenti:

-   Consente di coesistere qualsiasi combinazione di caratteri, disegnata da qualsiasi combinazione di script e linguaggi, in un unico documento.
-   Definisce la semantica per ogni carattere.
-   Standardizza il comportamento dello script.
-   Fornisce un algoritmo standard per il testo bidirezionale.
-   Definisce i mapping incrociato ad altri standard.
-   Definisce più codifiche del set di caratteri singolo: UTF-7, UTF-8, UTF-16 e UTF-32. La conversione dei dati tra queste codifiche è senza perdita di dati.

Unicode supporta numerosi script utilizzati da linguaggi in tutto il mondo, oltre a un numero elevato di simboli tecnici e caratteri speciali utilizzati per la pubblicazione. Gli script supportati comprendono, ma non sono limitati a, Latino, greco, cirillico, ebraico, arabo, delimitatore, tailandese, Han, Hangul, Hiragana e katakana. Le lingue supportate comprendono, ma non sono limitate a, tedesco, francese, inglese, greco, russo, ebraico, arabo, Hindi, tailandese, cinese, coreano e giapponese. Attualmente, il formato Unicode può rappresentare la maggior parte dei caratteri nell'uso di computer moderni in tutto il mondo e continua a essere aggiornato per renderlo ancora più completo.

Le funzioni abilitate per Unicode sono descritte in [convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md). Queste funzioni usano la codifica UTF-16 (carattere wide), che è la codifica più comune di Unicode e quella usata per la codifica Unicode nativa nei sistemi operativi Windows. Ogni valore del codice è a 16 bit, a differenza dell'approccio precedente della [tabella codici](code-pages.md) ai dati di tipo carattere e stringa, che usa valori di codice a 8 bit. L'uso di 16 bit consente la codifica diretta di 65.536 caratteri. In realtà, l'universo dei simboli usati per la trascrizione dei linguaggi umani è ancora maggiore di quello e i punti di codice UTF-16 nell'intervallo tra U + D800 e U + DFFF vengono usati per formare coppie di surrogati, che costituiscono codifiche a 32 bit di caratteri supplementari. Per ulteriori informazioni, vedere [surrogati e caratteri supplementari](surrogates-and-supplementary-characters.md) .

Il set di caratteri Unicode include numerosi caratteri di combinazione, ad esempio U + 0308 ("̈"), una combinazione di dieresi o dieresi. Unicode spesso può rappresentare lo stesso glifo in un formato '' composto '' o '' scomposto '': ad esempio, il formato composto da "Ä" è il singolo punto di codice Unicode "Ä" (U + 00C4), mentre il formato decomposto è "A" + "̈" (U + 0041 U + 0308). Unicode non definisce un formato composto per ogni glifo. Ad esempio, "o" in minuscolo vietnamita con circonflesso e tilde ("ỗ") è rappresentato da U + 006F U + 0302 U + 0303 (o + circonflesso + tilde). Per ulteriori informazioni sulla combinazione di caratteri e problemi correlati, vedere [utilizzo della normalizzazione Unicode per rappresentare le stringhe](using-unicode-normalization-to-represent-strings.md).

Per la compatibilità con gli ambienti a 8 bit e a 7 bit, Unicode può anche essere codificato rispettivamente come UTF-8 e UTF-7. Sebbene le funzioni abilitate per Unicode in Windows usino UTF-16, è anche possibile utilizzare i dati codificati in UTF-8 o UTF-7, supportati in Windows come [tabelle codici](code-pages.md)multibyte character set.

Le nuove applicazioni Windows devono usare UTF-16 come rappresentazione dati interna. Windows fornisce inoltre un supporto completo per le tabelle codici e l'utilizzo misto nella stessa applicazione è possibile. Anche le nuove applicazioni basate su Unicode devono talvolta funzionare con le tabelle codici. I motivi di questo argomento sono illustrati nelle [tabelle codici](code-pages.md).

Un'applicazione può utilizzare le funzioni [**MultiByteToWideChar**](/windows/win32/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) per eseguire la conversione tra stringhe basate su tabelle codici e stringhe Unicode. Sebbene i relativi nomi facciano riferimento a "MultiByte", queste funzioni funzionano correttamente con il [set di caratteri a byte singolo](single-byte-character-sets.md) (SBCS), le tabelle codici DBCS ( [Double-byte character set](double-byte-character-sets.md) ) e multibyte character set (MBCS).

In genere, un'applicazione Windows deve usare UTF-16 internamente, convertendo solo come parte di un "Thin layer" sull'interfaccia che deve usare un altro formato. Questa tecnica difende dalla perdita e dal danneggiamento dei dati. Ogni tabella codici supporta caratteri diversi, ma nessuno di essi supporta l'intera gamma di caratteri forniti da Unicode. La maggior parte delle tabelle codici supporta subset diversi, codificati in modo diverso. Le tabelle codici per UTF-8 e UTF-7 sono un'eccezione, poiché supportano il set di caratteri Unicode completo e la conversione tra queste codifiche e UTF-16 è senza perdita di perdite.

I dati convertiti direttamente dalla codifica utilizzata da una tabella codici alla codifica utilizzata da un altro oggetto sono soggetti a danneggiamento, poiché lo stesso valore di dati in tabelle codici diverse può codificare un carattere diverso. Anche quando l'applicazione viene convertita il più vicino possibile all'interfaccia, è necessario considerare attentamente l'intervallo di dati da gestire.

I dati convertiti da Unicode a una tabella codici sono soggetti alla perdita di dati, perché una determinata tabella codici potrebbe non essere in grado di rappresentare ogni carattere utilizzato in tali dati Unicode specifici. Si noti pertanto che [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) potrebbe perdere alcuni dati se la tabella codici di destinazione non può rappresentare tutti i caratteri nella stringa Unicode.

Quando si modernizzano le applicazioni legacy basate su tabelle codici per l'utilizzo di Unicode, è possibile utilizzare funzioni generiche e la macro di [**testo**](/windows/win32/api/Winnt/nf-winnt-text) per mantenere un unico set di origini da cui compilare due versioni dell'applicazione. Una versione supporta Unicode e l'altra funziona con le tabelle codici di Windows. Grazie a questo meccanismo, è possibile convertire le applicazioni di grandi dimensioni dalle tabelle codici di Windows in Unicode mantenendo le origini delle applicazioni che possono essere compilate, compilate e testate in tutte le fasi della conversione. Per altre informazioni, vedere [convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md).

I caratteri e le stringhe Unicode utilizzano tipi di dati distinti da quelli per le stringhe e i caratteri basati sulla tabella codici. Insieme a una serie di macro e convenzioni di denominazione, questa distinzione riduce al minimo la possibilità di combinare accidentalmente i due tipi di dati di tipo carattere. Semplifica il controllo dei tipi del compilatore per garantire che vengano utilizzati solo valori di parametri Unicode con funzioni che prevedono stringhe Unicode.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Character Sets](character-sets.md)
</dt> <dt>

[Ordinamento](sorting.md)
</dt> <dt>

[Surrogati e caratteri supplementari](surrogates-and-supplementary-characters.md)
</dt> <dt>

[Uso della normalizzazione Unicode per rappresentare le stringhe](using-unicode-normalization-to-represent-strings.md)
</dt> </dl>

 

 



