---
description: La maggior parte delle applicazioni scritte oggi gestisce i dati di tipo carattere principalmente come Unicode, usando la codifica UTF-16.
ms.assetid: 866f09f4-629e-4097-a974-fbda9389d077
title: Tabelle codici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28528ba13e3db3f0c72dd7c071eb8b7886ab003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312881"
---
# <a name="code-pages"></a>Tabelle codici

La maggior parte delle applicazioni scritte oggi gestisce i dati di tipo carattere principalmente come [Unicode](unicode.md), usando la codifica UTF-16. Molte applicazioni legacy, tuttavia, continuano a usare i set di caratteri in base alle tabelle codici. Anche le nuove applicazioni a volte devono funzionare con le tabelle codici, spesso per uno dei seguenti motivi:

-   Per comunicare con le applicazioni legacy.
-   Per comunicare con i server di posta elettronica e di notizie precedenti, che potrebbero non sempre supportare Unicode.
-   Per comunicare con la console di Windows.

> [!Note]  
> Le nuove applicazioni Windows devono utilizzare [Unicode](unicode.md) per evitare le incoerenze di diverse tabelle codici e per semplificare la localizzazione.

 

Ogni tabella codici è rappresentata da un identificatore della tabella codici, ad esempio 1252, e viene gestita dalle funzioni API del set di caratteri e Unicode. Per un elenco degli identificatori della tabella codici supportati, vedere [identificatori](code-page-identifiers.md)delle tabelle codici. Il riferimento "tabelle codici" in Microsoft [go Global Developer Center](https://msdn.microsoft.com/goglobal) fornisce descrizioni complete di molte tabelle codici.

Le tabelle codici di Windows, comunemente denominate "tabelle codici ANSI", sono tabelle codici per le quali i valori non ASCII (valori maggiori di 127) rappresentano caratteri internazionali. Queste tabelle codici vengono usate in modo nativo in Windows me e sono disponibili anche in Windows NT e versioni successive.

> [!Note]  
> In origine, la tabella codici di Windows 1252, la tabella codici utilizzata comunemente per la lingua inglese e altre lingue europee occidentali, era basata su una bozza di American National Standards Institute (ANSI). Tale bozza è stata infine ISO 8859-1, ma la tabella codici di Windows 1252 è stata implementata prima che lo standard diventasse finale e non è esattamente uguale a ISO 8859-1.

 

Molte funzioni API Windows hanno versioni "A" (ANSI) e "W" (Wide, Unicode). La versione "A" gestisce il testo in base alle tabelle codici di Windows, mentre la versione "W" gestisce il testo Unicode. Vedere [tipi di dati Windows per le stringhe](windows-data-types-for-strings.md) e le [convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md).

Le tabelle codici di Windows vengono anche definite "tabelle codici attive" o "tabelle codici attive del sistema". Un sistema operativo Windows ha sempre una tabella codici di Windows attualmente attiva. Tutte le [versioni ANSI delle funzioni API](conventions-for-function-prototypes.md) usano la tabella codici attualmente attiva.

Le tabelle codici OEM (Original Equipment Manufacturer) sono tabelle codici per le quali i valori non ASCII rappresentano il disegno a linee e i caratteri di punteggiatura. Queste tabelle codici sono state originariamente usate per MS-DOS e sono ancora usate per le applicazioni console. Vengono inoltre utilizzati per i nomi di file non estesi nei file system FAT12, FAT16 e FAT32, come descritto in set di [caratteri utilizzati nei nomi di file](character-sets-used-in-file-names.md). La tabella codici OEM usuale per la lingua inglese è la tabella codici 437.

Per le tabelle codici di Windows e le tabelle codici OEM, i valori del codice da 0x00 a 0x7F corrispondono al set di caratteri ASCII a 7 bit. I valori di codice da 0x00 a 0x19 e 0x7F rappresentano sempre caratteri di controllo standardizzati e 0x20 tramite 0x7E rappresentano caratteri visualizzabili standardizzati. I caratteri rappresentati dai codici rimanenti, 0x80 tramite 0xFF, variano tra i set di caratteri. Ogni set di caratteri include caratteri speciali diversi, in genere personalizzati per un linguaggio o un gruppo di lingue. Nella Stati Uniti vengono in genere utilizzate le tabelle codici di Windows 1252 e OEM 437.

Oltre alle tabelle codici di Windows e OEM, le applicazioni possono utilizzare tabelle codici non native. Esempi sono le tabelle codici EBCDIC e Macintosh.

Due codifiche di Unicode (UTF-7 e UTF-8) vengono implementate come tabelle codici. Analogamente ad altre tabelle codici, ogni pagina è nota da un identificatore numerico e può essere gestita con molte delle stesse funzioni API del set di caratteri e Unicode.

Le tabelle codici possono essere [di tipo set di caratteri a byte singolo](single-byte-character-sets.md) (SBCS) o di pagine DBCS ( [Double byte character set](double-byte-character-sets.md) ). Nelle pagine SBCS ogni byte codifica direttamente un singolo carattere, in modo che sia possibile rappresentare esattamente 256 caratteri distinti (inclusi i caratteri di controllo, le lettere, le cifre, la punteggiatura, i simboli e simili). Le tabelle codici DBCS vengono utilizzate per lingue come il giapponese e il cinese. In una tabella codici di questo tipo, alcuni caratteri hanno codifiche a due byte con determinati valori di byte (sempre valori maggiori di 127) che fungono da "byte di apertura". Anziché codificare i caratteri nella propria destra, è possibile eseguire il mapping dei byte di apertura a un carattere solo in combinazione con un "byte finale".

Alcuni protocolli legacy richiedono l'utilizzo di tabelle codici SBCS e DBCS. Ogni tabella codici SBCS/DBCS supporta caratteri diversi, ma nessuna tabella codici supporta l'intera gamma di caratteri forniti da Unicode. Ogni tabella codici SBCS/DBCS supporta un subset diverso, codificato in modo diverso.

> [!Note]  
> I dati convertiti da una tabella codici SBCS o DBCS a un'altra sono soggetti a danneggiamento, perché lo stesso valore di dati in tabelle codici diverse può codificare un carattere diverso. I dati convertiti da Unicode a SBCS o DBCS sono soggetti alla perdita di dati, perché una determinata tabella codici potrebbe non essere in grado di rappresentare ogni carattere utilizzato in tali dati Unicode specifici.

 

Oltre alle tabelle codici SBCS e DBCS, le applicazioni hanno a disposizione le tabelle codici Multibyte Character Set 52936, 54936, 51949 e 5022x, che usano un approccio simile a quello per un DBCS. Una tabella codici Multibyte Character Set supera tuttavia le codifiche a due byte di alcuni caratteri. UTF-7 e UTF-8 usano un approccio simile per codificare Unicode in base a un byte a 7 bit e a 8 bit, rispettivamente. Per ulteriori informazioni, vedere [Unicode](unicode.md).

Diverse funzioni di set di caratteri e Unicode consentono alle applicazioni di gestire le tabelle codici. Per ottenere informazioni su una tabella codici, un'applicazione può utilizzare le funzioni [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) e [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) . Queste informazioni includono il carattere predefinito utilizzato quando un carattere in una stringa convertita non dispone di una voce corrispondente nella tabella codici.

Un'applicazione può utilizzare le funzioni [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) per eseguire la conversione tra stringhe basate su tabelle codici di Windows e stringhe Unicode. Sebbene i relativi nomi facciano riferimento a "MultiByte", queste funzioni funzionano ugualmente correttamente con le tabelle codici SBCS, DBCS e Multibyte Character Set.

> [!Note]  
> [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) può perdere alcuni dati se la tabella codici fornita non può rappresentare tutti i caratteri in una stringa Unicode.

 

L'applicazione può eseguire la conversione tra tabelle codici di Windows e tabelle codici OEM usando le funzioni della libreria di runtime C standard. Tuttavia, l'utilizzo di queste funzioni presenta il rischio di perdita di dati perché i caratteri che possono essere rappresentati da ogni tabella codici non corrispondono esattamente.

Le applicazioni possono anche chiamare la funzione [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) . Questa funzione recupera l'identificatore della tabella codici corrente di Windows (ANSI).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Character Sets](character-sets.md)
</dt> </dl>

 

 



