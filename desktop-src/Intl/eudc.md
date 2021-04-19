---
description: La chiave del registro di sistema EUDC contiene una o più sottochiavi contenenti valori che definiscono i tipi di carattere associati ai caratteri definiti dall'utente finale (EUDCs) per una determinata tabella codici.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781f7c28460c2e56f4bcdb393277f509f88a0383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317153"
---
# <a name="eudc"></a><span data-ttu-id="e504b-103">EUDC</span><span class="sxs-lookup"><span data-stu-id="e504b-103">EUDC</span></span>

<span data-ttu-id="e504b-104">La chiave del registro di sistema EUDC contiene una o più sottochiavi contenenti valori che definiscono i tipi di carattere associati ai [caratteri definiti dall'utente finale (EUDCs)](end-user-defined-characters.md) per una determinata tabella codici.</span><span class="sxs-lookup"><span data-stu-id="e504b-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="e504b-105">Dispone del seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="e504b-105">It has the following registry location:</span></span>

<span data-ttu-id="e504b-106">HKEY \_ \_ utente corrente \\ EUDC</span><span class="sxs-lookup"><span data-stu-id="e504b-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="e504b-107">Il formato è:</span><span class="sxs-lookup"><span data-stu-id="e504b-107">The format is:</span></span>

<span data-ttu-id="e504b-108">EUDC SystemDefaultEUDCFont = TrueTypeEUDCFontFileName TrueTypeFontTypeface = TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="e504b-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="e504b-109">dove:</span><span class="sxs-lookup"><span data-stu-id="e504b-109">where:</span></span>



|                          |                                                                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e504b-110">SystemDefaultEUDCFont</span><span class="sxs-lookup"><span data-stu-id="e504b-110">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="e504b-111">Nome predefinito utilizzato per impostare il tipo di carattere predefinito del sistema.</span><span class="sxs-lookup"><span data-stu-id="e504b-111">Predefined name used to set the system default font.</span></span> <span data-ttu-id="e504b-112">Non esiste alcun tipo di carattere EUDC predefinito di sistema, a meno che questa voce non venga specificata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="e504b-112">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="e504b-113">TrueTypeFontTypeface</span><span class="sxs-lookup"><span data-stu-id="e504b-113">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="e504b-114">Nome definito dall'utente associato a un tipo di carattere TrueType non EUDC.</span><span class="sxs-lookup"><span data-stu-id="e504b-114">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="e504b-115">TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="e504b-115">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="e504b-116">Stringa costituita dal nome file di un file del tipo di carattere EUDC separato.</span><span class="sxs-lookup"><span data-stu-id="e504b-116">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="e504b-117">Questo file identifica un tipo di carattere da associare a TrueTypeFontTypeface.</span><span class="sxs-lookup"><span data-stu-id="e504b-117">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="e504b-118">Nell'esempio seguente viene illustrata la chiave EUDC per la tabella codici 932.</span><span class="sxs-lookup"><span data-stu-id="e504b-118">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="e504b-119">Nell'esempio seguente viene impostato il tipo di carattere EUDC predefinito di sistema come EUDC. ttf e vengono associati i tipi di carattere EUDC separati Mineudc. ttf e Goteudc. ttf con i nomi dei tipi di carattere MS Mincho e MS Gothic, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="e504b-119">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="e504b-120">Quando la tabella codici di Windows (System ACP) associata alla lingua per i programmi non Unicode corrisponde alla sottochiave, il sottosistema GDI Cerca le coppie di valori della sottochiave per ottenere le informazioni di visualizzazione relative al carattere.</span><span class="sxs-lookup"><span data-stu-id="e504b-120">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="e504b-121">Per prima cosa cerca un nome che corrisponda al tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="e504b-121">It first looks for a name matching the current font.</span></span> <span data-ttu-id="e504b-122">Se non è presente alcun valore, viene esaminato il valore SystemDefaultEUDCFont.</span><span class="sxs-lookup"><span data-stu-id="e504b-122">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="e504b-123">Se non è definito alcun valore, GDI considera il carattere come non definito.</span><span class="sxs-lookup"><span data-stu-id="e504b-123">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="e504b-124">Si noti che il testo non deve essere presente nella tabella codici di Windows.</span><span class="sxs-lookup"><span data-stu-id="e504b-124">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="e504b-125">Si supponga, ad esempio, che la tabella codici abbia l'identificatore 1252, la tabella codici di Windows predefinita per la lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="e504b-125">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="e504b-126">Un'applicazione passa il singolo punto di codice Unicode U + E000, nell'area di utilizzo privato Unicode (PUA), a [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="e504b-126">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="e504b-127">In questo caso, GDI esamina i valori del registro di sistema sotto 1252 per ottenere le informazioni sul carattere per le proprietà di visualizzazione dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="e504b-127">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e504b-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e504b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e504b-129">Voci del registro di sistema EUDC</span><span class="sxs-lookup"><span data-stu-id="e504b-129">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="e504b-130">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="e504b-130">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
