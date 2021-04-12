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
# <a name="using-functions-that-have-no-unicode-equivalents"></a><span data-ttu-id="ca289-103">Utilizzo di funzioni senza equivalenti Unicode</span><span class="sxs-lookup"><span data-stu-id="ca289-103">Using Functions That Have No Unicode Equivalents</span></span>

<span data-ttu-id="ca289-104">Le funzioni che non sono state implementate con una versione [Unicode](unicode.md) sono in genere sostituite da funzioni più potenti o estese che supportano Unicode.</span><span class="sxs-lookup"><span data-stu-id="ca289-104">Functions that have not been implemented with a [Unicode](unicode.md) version have typically been replaced by more powerful or extended functions that do support Unicode.</span></span> <span data-ttu-id="ca289-105">Se, ad esempio, si esegue il porting di codice che chiama la funzione [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) , l'applicazione può supportare Unicode usando la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="ca289-105">For example, if you are porting code that calls the [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) function, your application can support Unicode by using the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function instead.</span></span>

<span data-ttu-id="ca289-106">Se una funzione non ha un equivalente Unicode, l'applicazione può eseguire il mapping dei caratteri da e verso i set di caratteri a 8 bit prima e dopo la chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="ca289-106">If a function has no Unicode equivalent, the application can map characters to and from 8-bit character sets before and after the function call.</span></span> <span data-ttu-id="ca289-107">Ad esempio, le funzioni di formattazione dei numeri **atoi** e **ITOA** usano solo le cifre da 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="ca289-107">For example, the number-formatting functions **atoi** and **itoa** use only the digits 0 through 9.</span></span> <span data-ttu-id="ca289-108">In genere, il mapping di caratteri Unicode a 8 bit causa la perdita di dati, ma ciò può essere evitato rendendo il codice indipendente dai tipi e rendendo le espressioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="ca289-108">Normally, mapping Unicode to 8-bit characters causes loss of data, but this can be avoided by making the code type-independent and making the expressions conditional.</span></span> <span data-ttu-id="ca289-109">Le istruzioni nell'esempio seguente, scritte per i caratteri a 8 bit, sono dipendenti dal tipo e devono essere modificate per supportare Unicode.</span><span class="sxs-lookup"><span data-stu-id="ca289-109">The statements in the following example, written for 8-bit characters, are type-dependent and should be changed to support Unicode.</span></span>


```C++
char str[4] = "137";

int num = atoi(str);
```



<span data-ttu-id="ca289-110">Queste istruzioni possono essere riscritte come indicato di seguito per renderle indipendenti dai tipi.</span><span class="sxs-lookup"><span data-stu-id="ca289-110">These statements can be rewritten as follows to make them type-independent.</span></span>


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



<span data-ttu-id="ca289-111">In questo esempio la funzione della libreria C standard **wcstombs** converte il formato Unicode in ASCII.</span><span class="sxs-lookup"><span data-stu-id="ca289-111">In this example, the standard C library function **wcstombs** translates Unicode to ASCII.</span></span> <span data-ttu-id="ca289-112">Questo esempio si basa sul fatto che le cifre da 0 a 9 possono essere sempre convertite da Unicode a ASCII, anche se non è possibile eseguire una parte del testo circostante.</span><span class="sxs-lookup"><span data-stu-id="ca289-112">The example relies on the fact that the digits 0 through 9 can always be translated from Unicode to ASCII, even if some of the surrounding text cannot.</span></span> <span data-ttu-id="ca289-113">La funzione **atoi** si arresta in corrispondenza di qualsiasi carattere diverso da una cifra.</span><span class="sxs-lookup"><span data-stu-id="ca289-113">The **atoi** function stops at any character that is not a digit.</span></span>

<span data-ttu-id="ca289-114">L'applicazione può usare la funzione [**LCMAPSTRING**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) NLS (National Language Support) per elaborare il testo che include le [cifre native](digit-shapes.md) fornite per alcuni degli script in Unicode.</span><span class="sxs-lookup"><span data-stu-id="ca289-114">Your application can use the National Language Support (NLS) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) function to process text that includes the [native digits](digit-shapes.md) provided for some of the scripts in Unicode.</span></span>

> [!Caution]  
> <span data-ttu-id="ca289-115">L'uso errato della funzione **wcstombs** può compromettere la sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ca289-115">Using the **wcstombs** function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="ca289-116">Verificare che il buffer dell'applicazione per la stringa di caratteri a 8 bit sia almeno di dimensioni 2 \* (*\_ lunghezza char* + 1), dove *char \_ length* rappresenta la lunghezza della stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="ca289-116">Make sure that the application buffer for the string of 8-bit characters is at least of size 2\*(*char\_length* +1), where *char\_length* represents the length of the Unicode string.</span></span> <span data-ttu-id="ca289-117">Questa restrizione viene eseguita perché, con [set di caratteri a doppio byte](double-byte-character-sets.md) (DBCS), è possibile eseguire il mapping di ogni carattere Unicode a due caratteri consecutivi a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="ca289-117">This restriction is made because, with [double-byte character sets](double-byte-character-sets.md) (DBCSs), each Unicode character can be mapped to two consecutive 8-bit characters.</span></span> <span data-ttu-id="ca289-118">Se il buffer non è in possesso dell'intera stringa, la stringa di risultato non è con terminazione null e costituisce un rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ca289-118">If the buffer does not hold the entire string, the result string is not null-terminated, posing a security risk.</span></span> <span data-ttu-id="ca289-119">Per ulteriori informazioni sulla sicurezza delle applicazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="ca289-119">For more information about application security, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ca289-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca289-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca289-121">Utilizzo di set di caratteri e Unicode</span><span class="sxs-lookup"><span data-stu-id="ca289-121">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
