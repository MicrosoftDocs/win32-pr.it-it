---
description: NTFS archivia i nomi di file in formato Unicode. Al contrario, i file system FAT12, FAT16 e FAT32 precedenti utilizzano il set di caratteri OEM. Per altre informazioni, vedere Tabelle codici.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: Set di caratteri utilizzati nei nomi file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79394c92b2886f715299855aae27f15753dc86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882749"
---
# <a name="character-sets-used-in-file-names"></a><span data-ttu-id="89857-105">Set di caratteri utilizzati nei nomi file</span><span class="sxs-lookup"><span data-stu-id="89857-105">Character Sets Used in File Names</span></span>

<span data-ttu-id="89857-106">NTFS archivia i nomi di file in formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="89857-106">NTFS stores file names in Unicode.</span></span> <span data-ttu-id="89857-107">Al contrario, i file system FAT12, FAT16 e FAT32 precedenti utilizzano il set di caratteri OEM.</span><span class="sxs-lookup"><span data-stu-id="89857-107">In contrast, the older FAT12, FAT16, and FAT32 file systems use the OEM character set.</span></span> <span data-ttu-id="89857-108">Per altre informazioni, vedere [Tabelle codici](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="89857-108">For more information, see [Code Pages](code-pages.md).</span></span>

<span data-ttu-id="89857-109">Le applicazioni non Unicode che creano file FAT talvolta devono usare le funzioni di conversione della libreria di runtime C standard per tradurre tra il set di caratteri della tabella codici di Windows e il set di caratteri della tabella codici OEM.</span><span class="sxs-lookup"><span data-stu-id="89857-109">Non-Unicode applications that create FAT files sometimes have to use the standard C runtime library conversion functions to translate between the Windows code page character set and the OEM code page character set.</span></span> <span data-ttu-id="89857-110">Con le implementazioni Unicode delle funzioni file system, non è necessario eseguire tali traduzioni.</span><span class="sxs-lookup"><span data-stu-id="89857-110">With Unicode implementations of the file system functions, it is not necessary to perform such translations.</span></span>

<span data-ttu-id="89857-111">L'applicazione può usare tipi stringa generici, come descritto in [tipi di dati di Windows per le stringhe](windows-data-types-for-strings.md).</span><span class="sxs-lookup"><span data-stu-id="89857-111">Your application can use generic string types, as described in [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span> <span data-ttu-id="89857-112">L'applicazione può anche usare i prototipi di funzione generici usando le tecniche descritte in [convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="89857-112">The application can also use generic function prototypes using techniques described in [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span> <span data-ttu-id="89857-113">Per i tipi di stringa generici o per i prototipi di funzione generica, l'applicazione può usare un unico file di origine per compilare una versione Unicode o non Unicode.</span><span class="sxs-lookup"><span data-stu-id="89857-113">For either generic string types or generic function prototypes, your application can use a single source file to compile either a Unicode or a non-Unicode version.</span></span> <span data-ttu-id="89857-114">Per consentire questa operazione, l'applicazione fornisce macro per le funzioni che non vengono richiamate durante la compilazione per Unicode.</span><span class="sxs-lookup"><span data-stu-id="89857-114">To allow for this, the application provides macros for functions that are not invoked when compiling for Unicode.</span></span>

<span data-ttu-id="89857-115">Nei file system NTFS e FAT, i caratteri speciali per il nome file sono:' \\ ','/',' .','?' è \* '.</span><span class="sxs-lookup"><span data-stu-id="89857-115">In both NTFS and FAT file systems, the special file name characters are: '\\', '/', '.', '?', and '\*'.</span></span> <span data-ttu-id="89857-116">Nelle tabelle codici OEM questi caratteri speciali si trovano nell'intervallo di caratteri ASCII (da 0x00 a 0x7F).</span><span class="sxs-lookup"><span data-stu-id="89857-116">On OEM code pages, these special characters are in the ASCII range of characters (0x00 through 0x7F).</span></span> <span data-ttu-id="89857-117">Gli equivalenti Unicode sono gli stessi valori in formato a 2 byte, 0x0000 tramite 0x007F.</span><span class="sxs-lookup"><span data-stu-id="89857-117">Their Unicode equivalents are the same values in a 2-byte form, 0x0000 through 0x007F.</span></span>

> [!Caution]  
> <span data-ttu-id="89857-118">I set di caratteri della tabella codici di Windows e della tabella codici OEM usati nei sistemi operativi in lingua giapponese contengono il simbolo Yen (¥) invece di una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="89857-118">Windows code page and OEM code page character sets used on Japanese-language operating systems contain the Yen symbol (¥) instead of a backslash (\\).</span></span> <span data-ttu-id="89857-119">Il simbolo Yen è quindi un carattere non consentito per i file system NTFS e FAT.</span><span class="sxs-lookup"><span data-stu-id="89857-119">Thus, the Yen symbol is a prohibited character for NTFS and FAT file systems.</span></span> <span data-ttu-id="89857-120">Quando si esegue il mapping di Unicode a una tabella codici in lingua giapponese, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) e altre funzioni di conversione mappano sia la barra rovesciata (u + 005C) che il normale simbolo di yen Unicode (u + 00A5) a questo stesso carattere.</span><span class="sxs-lookup"><span data-stu-id="89857-120">When mapping Unicode to a Japanese-language code page, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and other conversion functions map both backslash (U+005C) and the normal Unicode Yen symbol (U+00A5) to this same character.</span></span> <span data-ttu-id="89857-121">Per motivi di sicurezza, le applicazioni non dovrebbero in genere consentire il carattere U + 00A5 in una stringa Unicode che potrebbe essere convertita per essere usata come nome file FAT.</span><span class="sxs-lookup"><span data-stu-id="89857-121">For security reasons, your applications should not typically allow the character U+00A5 in a Unicode string that might be converted for use as a FAT file name.</span></span> <span data-ttu-id="89857-122">Per ulteriori informazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="89857-122">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="89857-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89857-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89857-124">Unicode nell'API Windows</span><span class="sxs-lookup"><span data-stu-id="89857-124">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> <dt>

[<span data-ttu-id="89857-125">Considerazioni sulla sicurezza: funzionalità internazionali</span><span class="sxs-lookup"><span data-stu-id="89857-125">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> </dl>

 

 



