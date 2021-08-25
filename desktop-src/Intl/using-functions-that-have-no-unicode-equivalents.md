---
description: Le funzioni che non sono state implementate con una versione Unicode sono state in genere sostituite da funzioni più potenti o estese che supportano Unicode.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Uso di funzioni senza equivalenti Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00781db9bce98c335c4a9071b9643ef5fdcb3716478cbffe12a5b53b33e2313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787881"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a>Uso di funzioni senza equivalenti Unicode

Le funzioni che non sono state implementate con [una versione Unicode](unicode.md) sono in genere state sostituite da funzioni più potenti o estese che supportano Unicode. Ad esempio, se si porta il codice che chiama la funzione [**OpenFile,**](/windows/win32/api/winbase/nf-winbase-openfile) l'applicazione può supportare Unicode usando invece [**la funzione CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)

Se una funzione non ha un equivalente Unicode, l'applicazione può eseguire il mapping dei caratteri a e da set di caratteri a 8 bit prima e dopo la chiamata di funzione. Ad esempio, le funzioni di formattazione dei numeri **atoi** **e itoa** usano solo le cifre da 0 a 9. In genere, il mapping di Unicode a caratteri a 8 bit causa la perdita di dati, ma ciò può essere evitato rendendo indipendente il tipo di codice e rendendo le espressioni condizionali. Le istruzioni nell'esempio seguente, scritte per caratteri a 8 bit, dipendono dal tipo e devono essere modificate per supportare Unicode.


```C++
char str[4] = "137";

int num = atoi(str);
```



Queste istruzioni possono essere riscritte come indicato di seguito per renderle indipendenti dal tipo.


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



In questo esempio la funzione della libreria C standard **wcstombs** converte Unicode in ASCII. L'esempio si basa sul fatto che le cifre da 0 a 9 possono sempre essere convertite da Unicode ad ASCII, anche se non è possibile usare parte del testo circostante. La **funzione atoi** si arresta in corrispondenza di qualsiasi carattere che non sia una cifra.

L'applicazione può usare la funzione [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) NLS (National [](digit-shapes.md) Language Support) per elaborare il testo che include le cifre native fornite per alcuni script in Unicode.

> [!Caution]  
> L'uso non corretto della funzione **wcstombs** può compromettere la sicurezza dell'applicazione. Assicurarsi che il buffer dell'applicazione per la stringa di caratteri a 8 bit sia di dimensioni pari almeno a 2 ( lunghezza \* *\_ char* +1), dove *char \_ length* rappresenta la lunghezza della stringa Unicode. Questa restrizione viene [](double-byte-character-sets.md) fatta perché, con set di caratteri a byte doppio (DBCS), è possibile eseguire il mapping di ogni carattere Unicode a due caratteri consecutivi a 8 bit. Se il buffer non contiene l'intera stringa, la stringa di risultato non è con terminazione Null, esponendo un rischio per la sicurezza. Per altre informazioni sulla sicurezza delle applicazioni, vedere [Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di unicode e set di caratteri](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
