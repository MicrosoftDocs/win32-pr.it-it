---
description: La maggior parte delle applicazioni scritte oggi gestisce i dati di tipo carattere principalmente come Unicode, usando la codifica UTF-16.
ms.assetid: 866f09f4-629e-4097-a974-fbda9389d077
title: Tabelle codici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad589183bbb64a2feb65079a2322dd148598c6c3542320ec2ce851b9de61cfa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754961"
---
# <a name="code-pages"></a>Tabelle codici

La maggior parte delle applicazioni scritte oggi gestisce i dati di tipo carattere [principalmente come Unicode,](unicode.md)usando la codifica UTF-16. Tuttavia, molte applicazioni legacy continuano a usare set di caratteri basati su tabella codici. Anche le nuove applicazioni talvolta devono usare le tabelle codici, spesso per uno dei motivi seguenti:

-   Per comunicare con le applicazioni legacy.
-   Per comunicare con server di posta elettronica e di notizie meno recenti, che potrebbero non supportare sempre Unicode.
-   Per comunicare con la console Windows.

> [!Note]  
> Le Windows devono usare [Unicode](unicode.md) per evitare le incoerenze di diverse pagine di codice e per semplificare la localizzazione.

 

Ogni tabella codici è rappresentata da un identificatore di tabella codici, ad esempio 1252, e viene gestita dalle funzioni API Unicode e set di caratteri. Per un elenco degli identificatori di tabella codici supportati, vedere [Identificatori della tabella codici.](code-page-identifiers.md) Le informazioni di riferimento sulle "code pages" in Microsoft [Go Global Developer Center (Centro](https://msdn.microsoft.com/goglobal) per sviluppatori globale di Microsoft Go) fornisce descrizioni complete di molte pagine di codice.

Windows code pages, comunemente denominate "code pages ANSI", sono le code pages per le quali i valori non ASCII (valori maggiori di 127) rappresentano caratteri internazionali. Queste code pages vengono usate in modo nativo in Windows Me e sono disponibili anche in Windows NT e versioni successive.

> [!Note]  
> In origine, Windows tabella codici 1252, la tabella codici comunemente usata per l'inglese e altre lingue dell'Europa occidentale, era basata su una bozza American National Standards Institute (ANSI). Tale bozza è infine diventata ISO 8859-1, ma la tabella codici 1252 di Windows è stata implementata prima che lo standard diventasse finale e non è esattamente uguale a ISO 8859-1.

 

Molte Windows API hanno versioni "A" (ANSI) e "W" (wide, Unicode). La versione "A" gestisce il testo in base Windows tabella codici, mentre la versione "W" gestisce il testo Unicode. Vedere [Windows tipi di dati per stringhe](windows-data-types-for-strings.md) e [convenzioni per i prototipi di funzione.](conventions-for-function-prototypes.md)

Windows code pages vengono talvolta definite anche "code pages attive" o "code pages attive del sistema". Un Windows sistema operativo ha sempre una tabella codici Windows attiva. Tutte [le versioni ANSI delle funzioni API usano](conventions-for-function-prototypes.md) la tabella codici attualmente attiva.

Le pagine codici OEM (Original Equipment Manufacturer) sono pagine codici per le quali i valori non ASCII rappresentano caratteri di punteggiatura e disegno di righe. Queste pagine codici sono state originariamente usate per MS-DOS e sono ancora usate per le applicazioni console. Vengono inoltre usati per i nomi di file non estesi nei file system FAT12, FAT16 e FAT32, come descritto in Set di caratteri usati [nei nomi file](character-sets-used-in-file-names.md). La tabella codici OEM consueta per l'inglese è la tabella codici 437.

Per le Windows codici e le code pages OEM, i valori del codice 0x00 da 0x7F corrispondono al set di caratteri ASCII a 7 bit. I valori 0x00 da 0x19 e 0x7F rappresentano sempre caratteri di controllo standardizzati e 0x20 da 0x7E rappresentano caratteri visualizzabili standardizzati. I caratteri rappresentati dai codici rimanenti, da 0x80 a 0xff, variano in base ai set di caratteri. Ogni set di caratteri include caratteri speciali diversi, in genere personalizzati per una lingua o un gruppo di lingue. Windows tabella codici 1252 e la tabella codici OEM 437 vengono in genere usate nel Stati Uniti.

Oltre alle Windows e OEM, le applicazioni possono usare le code pages non native. Ad esempio, le pagine codici EBCDIC e Macintosh.

Due codifiche di Unicode (UTF-7 e UTF-8) vengono implementate come tabella codici. Analogamente ad altre pagine codici, ogni pagina è nota da un identificatore numerico e può essere gestita con molte delle stesse funzioni API unicode e set di caratteri.

Le pagine di codice possono essere pagine di [set](single-byte-character-sets.md) di caratteri a byte singolo (SBCS) o pagine DBCS [(Double Byte Character Set).](double-byte-character-sets.md) Nelle pagine SBCS ogni byte codifica direttamente un singolo carattere, in modo che sia possibile rappresentare esattamente 256 caratteri distinti (inclusi caratteri di controllo, lettere, cifre, punteggiatura, simboli e simili). Le pagine codici DBCS vengono usate per lingue come il giapponese e il cinese. In una tabella codici di questo tipo, alcuni caratteri hanno codifiche a due byte con determinati valori di byte (sempre valori maggiori di 127) che servono come "byte di lead". Anziché codificare i caratteri a destra, è possibile eseguire il mapping dei byte iniziali a un carattere solo in combinazione con un "byte finale".

Alcuni protocolli legacy richiedono l'uso di tabella codici SBCS e DBCS. Ogni tabella codici SBCS/DBCS supporta caratteri diversi, ma nessuna tabella codici supporta l'intera gamma di caratteri forniti da Unicode. Ogni tabella codici SBCS/DBCS supporta un subset diverso con codifica diversa.

> [!Note]  
> I dati convertiti da una tabella codici SBCS o DBCS a un'altra sono soggetti a danneggiamento, perché lo stesso valore di dati in diverse pagine di codice può codificare un carattere diverso. I dati convertiti da Unicode a SBCS o DBCS sono soggetti a perdita di dati, perché una determinata tabella codici potrebbe non essere in grado di rappresentare tutti i caratteri utilizzati nei dati Unicode specifici.

 

Oltre alle pagine codici SBCS e DBCS, le applicazioni hanno a disposizione le code pages del set di caratteri multibyte 52936, 54936, 51949 e 5022x, che usano un approccio simile a quello per un DBCS. Una tabella codici del set di caratteri multibyte supera tuttavia le codifiche a due byte di alcuni caratteri. UTF-7 e UTF-8 usano un approccio simile per codificare Unicode in base rispettivamente a byte a 7 e a 8 bit. Per altre informazioni, vedere [Unicode.](unicode.md)

Diverse funzioni Unicode e set di caratteri consentono alle applicazioni di gestire le pagine di codice. Un'applicazione può usare [**le funzioni GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) [**e GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) per ottenere informazioni su una tabella codici. Queste informazioni includono il carattere predefinito usato quando un carattere in una stringa convertita non ha una voce corrispondente nella tabella codici.

Un'applicazione può usare [**le funzioni MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) per eseguire la conversione tra stringhe in base Windows tabella codici e stringhe Unicode. Anche se i nomi fanno riferimento a "MultiByte", queste funzioni funzionano ugualmente bene con le pagine codici SBCS, DBCS e set di caratteri multibyte.

> [!Note]  
> [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) può perdere alcuni dati se la tabella codici fornita non può rappresentare tutti i caratteri in una stringa Unicode.

 

L'applicazione può eseguire la conversione tra Windows e le pagine codici OEM usando le funzioni della libreria di runtime C standard. Tuttavia, l'uso di queste funzioni comporta un rischio di perdita di dati perché i caratteri che possono essere rappresentati da ogni tabella codici non corrispondono esattamente.

Le applicazioni possono anche chiamare la [**funzione GetACP.**](/windows/desktop/api/Winnls/nf-winnls-getacp) Questa funzione recupera l'identificatore della tabella Windows (ANSI) corrente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Character Sets](character-sets.md)
</dt> </dl>

 

 



