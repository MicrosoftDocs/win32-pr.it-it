---
description: Anteporre sempre un prefisso a un file di testo normale Unicode con una byte order mark, che informa un'applicazione che riceve il file che il file è ordinato per byte.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Uso di byte order mark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319485"
---
# <a name="using-byte-order-marks"></a><span data-ttu-id="055ad-103">Uso di byte order mark</span><span class="sxs-lookup"><span data-stu-id="055ad-103">Using Byte Order Marks</span></span>

<span data-ttu-id="055ad-104">Anteporre sempre un prefisso a un file di testo normale Unicode con una byte order mark, che informa un'applicazione che riceve il file che il file è ordinato per byte.</span><span class="sxs-lookup"><span data-stu-id="055ad-104">Always prefix a Unicode plain text file with a byte order mark, which informs an application receiving the file that the file is byte-ordered.</span></span> <span data-ttu-id="055ad-105">I contrassegni per l'ordine dei byte disponibili sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="055ad-105">Available byte order marks are listed in the following table.</span></span> <span data-ttu-id="055ad-106">Poiché il testo normale Unicode è una sequenza di valori di codice a 16 bit, è sensibile all'ordinamento dei byte utilizzato quando viene scritto il testo.</span><span class="sxs-lookup"><span data-stu-id="055ad-106">Because Unicode plain text is a sequence of 16-bit code values, it is sensitive to the byte ordering used when the text is written.</span></span>

> [!Note]  
> <span data-ttu-id="055ad-107">Un byte order mark non è un carattere di controllo che consente di selezionare l'ordine dei byte del testo.</span><span class="sxs-lookup"><span data-stu-id="055ad-107">A byte order mark is not a control character that selects the byte order of the text.</span></span>

 



| <span data-ttu-id="055ad-108">Indicatore dell'ordine dei byte</span><span class="sxs-lookup"><span data-stu-id="055ad-108">Byte order mark</span></span> | <span data-ttu-id="055ad-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="055ad-109">Description</span></span>           |
|-----------------|-----------------------|
| <span data-ttu-id="055ad-110">EF BB BF</span><span class="sxs-lookup"><span data-stu-id="055ad-110">EF BB BF</span></span>        | <span data-ttu-id="055ad-111">UTF-8</span><span class="sxs-lookup"><span data-stu-id="055ad-111">UTF-8</span></span>                 |
| <span data-ttu-id="055ad-112">FE FF</span><span class="sxs-lookup"><span data-stu-id="055ad-112">FF FE</span></span>           | <span data-ttu-id="055ad-113">UTF-16, little endian</span><span class="sxs-lookup"><span data-stu-id="055ad-113">UTF-16, little endian</span></span> |
| <span data-ttu-id="055ad-114">FF FE</span><span class="sxs-lookup"><span data-stu-id="055ad-114">FE FF</span></span>           | <span data-ttu-id="055ad-115">UTF-16, big endian</span><span class="sxs-lookup"><span data-stu-id="055ad-115">UTF-16, big endian</span></span>    |
| <span data-ttu-id="055ad-116">FF FE 00 00</span><span class="sxs-lookup"><span data-stu-id="055ad-116">FF FE 00 00</span></span>     | <span data-ttu-id="055ad-117">UTF-32, little endian</span><span class="sxs-lookup"><span data-stu-id="055ad-117">UTF-32, little endian</span></span> |
| <span data-ttu-id="055ad-118">00 00 FE FF</span><span class="sxs-lookup"><span data-stu-id="055ad-118">00 00 FE FF</span></span>     | <span data-ttu-id="055ad-119">UTF-32, big-endian</span><span class="sxs-lookup"><span data-stu-id="055ad-119">UTF-32, big-endian</span></span>    |



 

> [!Note]  
> <span data-ttu-id="055ad-120">Microsoft usa l'ordine di byte UTF-16 little endian.</span><span class="sxs-lookup"><span data-stu-id="055ad-120">Microsoft uses UTF-16, little endian byte order.</span></span>

 

<span data-ttu-id="055ad-121">Idealmente, tutto il testo Unicode segue solo un set di regole di ordinamento dei byte.</span><span class="sxs-lookup"><span data-stu-id="055ad-121">Ideally, all Unicode text follows only one set of byte ordering rules.</span></span> <span data-ttu-id="055ad-122">Questa operazione non è tuttavia possibile, perché i microprocessori differiscono dal posizionamento del byte meno significativo.</span><span class="sxs-lookup"><span data-stu-id="055ad-122">This is not possible, however, because microprocessors differ in the placement of the least significant byte.</span></span> <span data-ttu-id="055ad-123">I processori Intel e MIPS posizionano prima di tutto il byte meno significativo, mentre i processori Motorola (e tutti i file Unicode invertiti in byte) lo posizionano per ultimo.</span><span class="sxs-lookup"><span data-stu-id="055ad-123">Intel and MIPS processors position the least significant byte first, whereas Motorola processors (and all byte-reversed Unicode files) position it last.</span></span> <span data-ttu-id="055ad-124">Con un solo set di regole di ordinamento dei byte, gli utenti di un microprocessore sono costretti a scambiare l'ordine dei byte ogni volta che viene letto o scritto un file di testo normale, anche se il file non viene mai trasferito a un altro sistema operativo in base a un microprocessore diverso.</span><span class="sxs-lookup"><span data-stu-id="055ad-124">With only a single set of byte ordering rules, users of one type of microprocessor are forced to swap the byte order every time a plain text file is read from or written to, even if the file is never transferred to another operating system based on a different microprocessor.</span></span>

<span data-ttu-id="055ad-125">La posizione preferita per specificare l'ordine dei byte è l'intestazione di un file, ma i file di testo non hanno intestazioni.</span><span class="sxs-lookup"><span data-stu-id="055ad-125">The preferred place to specify byte order is in a file header, but text files do not have headers.</span></span> <span data-ttu-id="055ad-126">Di conseguenza, Unicode ha definito un carattere (U + FEFF) e un carattere non carattere (U + FFFE) come Byte Order Mark.</span><span class="sxs-lookup"><span data-stu-id="055ad-126">Therefore, Unicode has defined a character (U+FEFF) and a noncharacter (U+FFFE) as byte order marks.</span></span> <span data-ttu-id="055ad-127">Sono immagini di byte mirror.</span><span class="sxs-lookup"><span data-stu-id="055ad-127">They are mirror byte images of each other.</span></span>

<span data-ttu-id="055ad-128">Poiché la sequenza U + FEFF è estremamente rara all'inizio di un normale file di testo non Unicode, può fungere da marcatore o firma implicita per identificare il file come file Unicode.</span><span class="sxs-lookup"><span data-stu-id="055ad-128">Since the sequence U+FEFF is exceedingly rare at the beginning of a regular non-Unicode text file, it can serve as an implicit marker or signature to identify the file as a Unicode file.</span></span> <span data-ttu-id="055ad-129">Le applicazioni che leggono i file di testo sia Unicode che non Unicode devono usare la presenza di questa sequenza come indicatore del fatto che il file è probabilmente un file Unicode.</span><span class="sxs-lookup"><span data-stu-id="055ad-129">Applications that read both Unicode and non-Unicode text files should use the presence of this sequence as an indicator that the file is most likely a Unicode file.</span></span> <span data-ttu-id="055ad-130">Confrontare questa tecnica con l'uso del marcatore EOF di MS-DOS per terminare i file di testo.</span><span class="sxs-lookup"><span data-stu-id="055ad-130">Compare this technique to using the MS-DOS EOF marker to terminate text files.</span></span>

<span data-ttu-id="055ad-131">Quando un'applicazione trova U + FEFF all'inizio di un file di testo, in genere elabora il file come file Unicode, anche se può eseguire ulteriori controlli euristici per la verifica.</span><span class="sxs-lookup"><span data-stu-id="055ad-131">When an application finds U+FEFF at the beginning of a text file, it typically processes the file as a Unicode file, although it can perform further heuristic checks for verification.</span></span> <span data-ttu-id="055ad-132">Un controllo di questo tipo può essere semplice come il test per verificare se la variazione nei byte di ordine inferiore è molto più alta rispetto alla variazione nei byte di ordine superiore.</span><span class="sxs-lookup"><span data-stu-id="055ad-132">Such a check can be as simple as testing to find out if the variation in the low-order bytes is much higher than the variation in the high-order bytes.</span></span> <span data-ttu-id="055ad-133">Se, ad esempio, il testo ASCII viene convertito in testo Unicode, ogni secondo byte è 0.</span><span class="sxs-lookup"><span data-stu-id="055ad-133">For example, if ASCII text is converted to Unicode text, every second byte is 0.</span></span> <span data-ttu-id="055ad-134">Inoltre, il controllo per i caratteri di ritorno a capo e avanzamento riga (U + 000A e U + d) e per le dimensioni del file pari o dispari può fornire un indicatore forte della natura del file.</span><span class="sxs-lookup"><span data-stu-id="055ad-134">Also, checking both for the linefeed and carriage return characters (U+000A and U+000D) and for even or odd file size can provide a strong indicator of the nature of the file.</span></span>

<span data-ttu-id="055ad-135">Quando un'applicazione trova U + FFFE all'inizio di un file di testo, lo interpreta per indicare che si tratta di un file Unicode invertito in byte.</span><span class="sxs-lookup"><span data-stu-id="055ad-135">When an application finds U+FFFE at the beginning of a text file, it interprets it to mean that the file is a byte-reversed Unicode file.</span></span> <span data-ttu-id="055ad-136">L'applicazione può scambiare l'ordine dei byte o avvisare l'utente che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="055ad-136">The application can either swap the order of the bytes or alert the user that an error has occurred.</span></span>

<span data-ttu-id="055ad-137">Poiché il carattere di byte order mark Unicode non viene trovato in alcuna tabella codici, scompare se i dati vengono convertiti in ANSI.</span><span class="sxs-lookup"><span data-stu-id="055ad-137">Since the Unicode byte order mark character is not found in any code page, it disappears if data is converted to ANSI.</span></span> <span data-ttu-id="055ad-138">A differenza di altri caratteri Unicode, non viene sostituito da un carattere predefinito quando viene convertito.</span><span class="sxs-lookup"><span data-stu-id="055ad-138">Unlike other Unicode characters, it is not replaced by a default character when it is converted.</span></span> <span data-ttu-id="055ad-139">Se un byte order mark viene trovato al centro di un file, non viene interpretato come carattere Unicode e non ha alcun effetto sull'output di testo.</span><span class="sxs-lookup"><span data-stu-id="055ad-139">If a byte order mark is found in the middle of a file, it is not interpreted as a Unicode character and has no effect on text output.</span></span>

> [!Note]  
> <span data-ttu-id="055ad-140">Il valore Unicode U + FFFF non è valido in file di testo normale e non può essere passato tra le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="055ad-140">The Unicode value U+FFFF is illegal in plain text files and cannot be passed between applications.</span></span> <span data-ttu-id="055ad-141">È riservata per l'uso privato di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="055ad-141">It is reserved for the private use of an application.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="055ad-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="055ad-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="055ad-143">Utilizzo di caratteri speciali in Unicode</span><span class="sxs-lookup"><span data-stu-id="055ad-143">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



