---
description: Unicode è uno standard di codifica dei caratteri globale. Il sistema usa Unicode esclusivamente per la modifica di caratteri e stringhe. Per una descrizione dettagliata di tutti gli aspetti di Unicode, vedere Standard Unicode.
ms.assetid: ca5bcdee-ea13-4745-a565-5426c462892d
title: Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c99a7af4d4fbb6b7783f97ceba37b1bf6b0bf54811beaf9c7c2348ec0125c73b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764771"
---
# <a name="unicode"></a>Unicode

Unicode è uno standard di codifica dei caratteri globale. Il sistema usa Unicode esclusivamente per la modifica di caratteri e stringhe. Per una descrizione dettagliata di tutti gli aspetti di Unicode, vedere [Standard Unicode](https://www.unicode.org/standard/standard.html).

Rispetto ai meccanismi meno recenti per la gestione dei dati di tipo carattere e stringa, Unicode semplifica la localizzazione del software e migliora l'elaborazione del testo multilingue. Usando Unicode per rappresentare dati di tipo carattere e stringa nelle applicazioni, è possibile abilitare le funzionalità di scambio dei dati universali per il marketing globale, usando un singolo file binario per ogni possibile codice carattere. Unicode esegue le operazioni seguenti:

-   Consente la coesistenza di qualsiasi combinazione di caratteri, ricavata da qualsiasi combinazione di script e linguaggi, in un singolo documento.
-   Definisce la semantica per ogni carattere.
-   Standardizza il comportamento degli script.
-   Fornisce un algoritmo standard per il testo bidirezionale.
-   Definisce i mapping incrociati ad altri standard.
-   Definisce più codifiche del set di caratteri singolo: UTF-7, UTF-8, UTF-16 e UTF-32. La conversione dei dati tra queste codifiche è senza perdita di dati.

Unicode supporta numerosi script usati dalle lingue di tutto il mondo, oltre a un numero elevato di simboli tecnici e caratteri speciali usati nella pubblicazione. Gli script supportati includono, a titolo esempimento, latini, greco, cirillico, ebraico, arabo, Devanagari, Thai, Han, Hangul, Hiragana e Katakana. Le lingue supportate includono, ad esempio, tedesco, francese, inglese, greco, russo, ebraico, arabo, hindi, thai, cinese, coreano e giapponese. Unicode attualmente può rappresentare la maggior parte dei caratteri nell'uso di computer moderni in tutto il mondo e continua a essere aggiornato per renderlo ancora più completo.

Le funzioni abilitate per Unicode sono descritte in [Convenzioni per i prototipi di funzione.](conventions-for-function-prototypes.md) Queste funzioni usano la codifica UTF-16 (caratteri wide), che è la codifica unicode più comune e quella usata per la codifica Unicode nativa nei sistemi operativi Windows sistema operativo. Ogni valore di codice ha una larghezza di [](code-pages.md) 16 bit, a differenza dell'approccio della tabella codici precedente ai dati di tipo carattere e stringa, che usa valori di codice a 8 bit. L'uso di 16 bit consente la codifica diretta di 65.536 caratteri. Infatti, l'universo dei simboli usati per trascrivere le lingue umane è ancora più grande di questo e i punti di codice UTF-16 nell'intervallo da U+D800 a U+DFFF vengono usati per formare coppie di surrogati, che costituiscono codifiche a 32 bit di caratteri supplementari. Per [altre informazioni, vedere Surrogati](surrogates-and-supplementary-characters.md) e caratteri supplementari.

Il set di caratteri Unicode include numerosi caratteri di combinazione, ad esempio U+0308 (" ZIONA"), un dieresi di combinazione o umlaut. Unicode può spesso rappresentare lo stesso glifo in un formato "composto" o "scomposto": ad esempio, la forma composta di "°" è il singolo punto di codice Unicode "Ò" (U+00C4), mentre la forma scomposa è "A" + " UF" (U+0041 U+0308). Unicode non definisce un formato composto per ogni glifo. Ad esempio, la "o" minuscola del Nord con circonflesso e tilde ("ỗ") è rappresentata da U+006f U+0302 U+0303 (o + Circumflex + Tilde). Per altre informazioni sulla combinazione di caratteri e problemi correlati, vedere [Uso della normalizzazione Unicode per rappresentare stringhe.](using-unicode-normalization-to-represent-strings.md)

Per garantire la compatibilità con ambienti a 8 e 7 bit, Unicode può anche essere codificato rispettivamente come UTF-8 e UTF-7. Anche se le funzioni abilitate per Unicode in Windows usano UTF-16, è anche possibile usare i dati codificati in UTF-8 o UTF-7, supportati in Windows come tabella codici del [set](code-pages.md)di caratteri multibyte .

Le Windows devono usare UTF-16 come rappresentazione dei dati interni. Windows offre anche un supporto completo per le pagine di codice ed è possibile un uso misto nella stessa applicazione. Anche le nuove applicazioni basate su Unicode talvolta devono usare le pagine di codice. I motivi sono illustrati nelle [pagine codici.](code-pages.md)

Un'applicazione può usare [**le funzioni MultiByteToWideChar**](/windows/win32/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) per eseguire la conversione tra stringhe basate su tabella codici e stringhe Unicode. Anche se i nomi fanno riferimento a "MultiByte", queste funzioni funzionano ugualmente bene con le pagine codici SBCS [(Single Byte Character Set),](single-byte-character-sets.md) DBCS [(Double Byte Character Set)](double-byte-character-sets.md) e MBCS (Multibyte Character Set).

In genere, un'applicazione Windows deve usare UTF-16 internamente, convertendo solo come parte di un "livello thin" sull'interfaccia che deve usare un altro formato. Questa tecnica consente di proteggere dalla perdita e dal danneggiamento dei dati. Ogni tabella codici supporta caratteri diversi, ma nessuno di essi supporta l'intera gamma di caratteri forniti da Unicode. La maggior parte delle pagine di codice supporta subset diversi, codificati in modo diverso. Le pagine di codice per UTF-8 e UTF-7 sono un'eccezione, perché supportano il set di caratteri Unicode completo e la conversione tra queste codifiche e UTF-16 è senza perdita di dati.

I dati convertiti direttamente dalla codifica usata da una tabella codici alla codifica usata da un'altra sono soggetti a danneggiamento, perché lo stesso valore di dati in diverse pagine di codice può codificare un carattere diverso. Anche quando l'applicazione esegue la conversione il più vicino possibile all'interfaccia, è necessario considerare attentamente l'intervallo di dati da gestire.

I dati convertiti da Unicode in una tabella codici sono soggetti a perdita di dati, perché una determinata tabella codici potrebbe non essere in grado di rappresentare ogni carattere utilizzato nei dati Unicode specifici. Si noti quindi che [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) potrebbe perdere alcuni dati se la tabella codici di destinazione non può rappresentare tutti i caratteri nella stringa Unicode.

Durante la modernizzazione delle applicazioni legacy basate su tabella codici per l'uso di Unicode, è possibile usare le funzioni generiche e la macro [**TEXT**](/windows/win32/api/Winnt/nf-winnt-text) per mantenere un singolo set di origini da cui compilare due versioni dell'applicazione. Una versione supporta Unicode e l'altra funziona con Windows di codice. Usando questo meccanismo, è possibile convertire anche applicazioni di dimensioni molto grandi da Windows code pages Windows a Unicode, mantenendo al tempo stesso origini dell'applicazione che possono essere compilate, compilate e testate in tutte le fasi della conversione. Per altre informazioni, vedere [Convenzioni per i prototipi di funzione.](conventions-for-function-prototypes.md)

I caratteri Unicode e le stringhe usano tipi di dati diversi da quelli per stringhe e caratteri basati su tabella codici. Insieme a una serie di macro e convenzioni di denominazione, questa distinzione riduce al minimo la possibilità di combinare accidentalmente i due tipi di dati di tipo carattere. Facilita il controllo dei tipi del compilatore per garantire che solo i valori dei parametri Unicode siano usati con funzioni che prevedono stringhe Unicode.

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

 

 



