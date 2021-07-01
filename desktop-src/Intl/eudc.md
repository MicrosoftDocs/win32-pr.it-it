---
description: La chiave del Registro di sistema EUDC contiene una o più sottochiavi contenenti valori che definiscono i tipi di carattere associati ai caratteri definiti dall'utente finale (EUDC) per una determinata tabella codici.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: Eudc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b583c7a0bfaa67684901e8d0a4a95ac5e45658
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120706"
---
# <a name="eudc"></a><span data-ttu-id="cfd97-103">Eudc</span><span class="sxs-lookup"><span data-stu-id="cfd97-103">EUDC</span></span>

<span data-ttu-id="cfd97-104">La chiave del Registro di sistema EUDC contiene una o più sottochiavi contenenti valori che definiscono i tipi di carattere associati ai caratteri definiti dall'utente [finale (EUDC)](end-user-defined-characters.md) per una determinata tabella codici.</span><span class="sxs-lookup"><span data-stu-id="cfd97-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="cfd97-105">Il percorso del Registro di sistema è il seguente:</span><span class="sxs-lookup"><span data-stu-id="cfd97-105">It has the following registry location:</span></span>

<span data-ttu-id="cfd97-106">HKEY \_ CURRENT \_ USER \\ EUDC</span><span class="sxs-lookup"><span data-stu-id="cfd97-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="cfd97-107">Il formato è:</span><span class="sxs-lookup"><span data-stu-id="cfd97-107">The format is:</span></span>

<span data-ttu-id="cfd97-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="cfd97-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="cfd97-109">dove:</span><span class="sxs-lookup"><span data-stu-id="cfd97-109">where:</span></span>



| <span data-ttu-id="cfd97-110">Valore</span><span class="sxs-lookup"><span data-stu-id="cfd97-110">Value</span></span>                         | <span data-ttu-id="cfd97-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfd97-111">Description</span></span>                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd97-112">SystemDefaultEUDCFont</span><span class="sxs-lookup"><span data-stu-id="cfd97-112">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="cfd97-113">Nome predefinito usato per impostare il tipo di carattere predefinito del sistema.</span><span class="sxs-lookup"><span data-stu-id="cfd97-113">Predefined name used to set the system default font.</span></span> <span data-ttu-id="cfd97-114">Non esiste alcun tipo di carattere EUDC predefinito di sistema, a meno che questa voce non venga specificata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="cfd97-114">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="cfd97-115">TrueTypeFontTypeface</span><span class="sxs-lookup"><span data-stu-id="cfd97-115">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="cfd97-116">Nome definito dall'utente associato a un tipo di carattere TrueType non EUDC.</span><span class="sxs-lookup"><span data-stu-id="cfd97-116">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="cfd97-117">TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="cfd97-117">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="cfd97-118">Stringa costituita dal nome file di un file del tipo di carattere EUDC separato.</span><span class="sxs-lookup"><span data-stu-id="cfd97-118">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="cfd97-119">Questo file identifica un tipo di carattere da associare a TrueTypeFontTypeface.</span><span class="sxs-lookup"><span data-stu-id="cfd97-119">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="cfd97-120">Nell'esempio seguente viene illustrata la chiave EUDC per la tabella codici 932.</span><span class="sxs-lookup"><span data-stu-id="cfd97-120">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="cfd97-121">L'esempio seguente imposta il tipo di carattere EUDC predefinito di sistema su Eudc.ttf e associa i tipi di carattere EUDC separati Mineudc.ttf e Goteudc.ttf rispettivamente ai nomi dei tipi di carattere MS Mincho e MS Fonts.</span><span class="sxs-lookup"><span data-stu-id="cfd97-121">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="cfd97-122">Quando la tabella codici di Windows associata alla lingua per i programmi non Unicode corrisponde alla sottochiave , il sottosistema GDI cerca le coppie di valori della sottochiave per ottenere informazioni di visualizzazione sul carattere.</span><span class="sxs-lookup"><span data-stu-id="cfd97-122">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="cfd97-123">Cerca innanzitutto un nome corrispondente al tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="cfd97-123">It first looks for a name matching the current font.</span></span> <span data-ttu-id="cfd97-124">Se non è presente, esamina il valore SystemDefaultEUDCFont.</span><span class="sxs-lookup"><span data-stu-id="cfd97-124">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="cfd97-125">Se non è definito alcun valore, GDI considera il carattere come non definito.</span><span class="sxs-lookup"><span data-stu-id="cfd97-125">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="cfd97-126">Si noti che il testo stesso non deve essere presente nella tabella codici di Windows.</span><span class="sxs-lookup"><span data-stu-id="cfd97-126">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="cfd97-127">Si supponga, ad esempio, che la tabella codici abbia l'identificatore 1252, la tabella codici predefinita di Windows per l'inglese.</span><span class="sxs-lookup"><span data-stu-id="cfd97-127">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="cfd97-128">Un'applicazione passa il singolo punto di codice Unicode U+E000, nell'area di utilizzo privato Unicode (PUA), a [**DrawText.**](/windows/win32/api/winuser/nf-winuser-drawtext)</span><span class="sxs-lookup"><span data-stu-id="cfd97-128">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="cfd97-129">In questo caso, GDI esamina i valori del Registro di sistema sotto 1252 per ottenere le informazioni sul tipo di carattere per le proprietà di visualizzazione dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="cfd97-129">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfd97-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cfd97-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfd97-131">Voci del Registro di sistema EUDC</span><span class="sxs-lookup"><span data-stu-id="cfd97-131">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="cfd97-132">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="cfd97-132">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
