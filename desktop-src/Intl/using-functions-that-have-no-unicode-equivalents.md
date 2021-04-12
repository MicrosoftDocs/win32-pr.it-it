---
description: Le funzioni che non sono state implementate con una versione Unicode sono in genere sostituite da funzioni più potenti o estese che supportano Unicode.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Utilizzo di funzioni senza equivalenti Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0850eea442b98c81918c7c6733da65f730936be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234196"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a>Utilizzo di funzioni senza equivalenti Unicode

Le funzioni che non sono state implementate con una versione [Unicode](unicode.md) sono in genere sostituite da funzioni più potenti o estese che supportano Unicode. Se, ad esempio, si esegue il porting di codice che chiama la funzione [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) , l'applicazione può supportare Unicode usando la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

Se una funzione non ha un equivalente Unicode, l'applicazione può eseguire il mapping dei caratteri da e verso i set di caratteri a 8 bit prima e dopo la chiamata di funzione. Ad esempio, le funzioni di formattazione dei numeri **atoi** e **ITOA** usano solo le cifre da 0 a 9. In genere, il mapping di caratteri Unicode a 8 bit causa la perdita di dati, ma ciò può essere evitato rendendo il codice indipendente dai tipi e rendendo le espressioni condizionali. Le istruzioni nell'esempio seguente, scritte per i caratteri a 8 bit, sono dipendenti dal tipo e devono essere modificate per supportare Unicode.


```C++
char str[4] = "137";

int num = atoi(str);
```



Queste istruzioni possono essere riscritte come indicato di seguito per renderle indipendenti dai tipi.


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



In questo esempio la funzione della libreria C standard **wcstombs** converte il formato Unicode in ASCII. Questo esempio si basa sul fatto che le cifre da 0 a 9 possono essere sempre convertite da Unicode a ASCII, anche se non è possibile eseguire una parte del testo circostante. La funzione **atoi** si arresta in corrispondenza di qualsiasi carattere diverso da una cifra.

L'applicazione può usare la funzione [**LCMAPSTRING**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) NLS (National Language Support) per elaborare il testo che include le [cifre native](digit-shapes.md) fornite per alcuni degli script in Unicode.

> [!Caution]  
> L'uso errato della funzione **wcstombs** può compromettere la sicurezza dell'applicazione. Verificare che il buffer dell'applicazione per la stringa di caratteri a 8 bit sia almeno di dimensioni 2 \* (*\_ lunghezza char* + 1), dove *char \_ length* rappresenta la lunghezza della stringa Unicode. Questa restrizione viene eseguita perché, con [set di caratteri a doppio byte](double-byte-character-sets.md) (DBCS), è possibile eseguire il mapping di ogni carattere Unicode a due caratteri consecutivi a 8 bit. Se il buffer non è in possesso dell'intera stringa, la stringa di risultato non è con terminazione null e costituisce un rischio per la sicurezza. Per ulteriori informazioni sulla sicurezza delle applicazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di set di caratteri e Unicode](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
