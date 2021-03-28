---
description: Il sistema fornisce sei tipi di carattere predefiniti.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Uso di un tipo di carattere azionario per creare testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a7e580175956185bcc26a7ebbae8d46dfff078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968269"
---
# <a name="using-a-stock-font-to-draw-text"></a><span data-ttu-id="4872b-103">Uso di un tipo di carattere azionario per creare testo</span><span class="sxs-lookup"><span data-stu-id="4872b-103">Using a Stock Font to Draw Text</span></span>

<span data-ttu-id="4872b-104">Il sistema fornisce sei tipi di carattere predefiniti.</span><span class="sxs-lookup"><span data-stu-id="4872b-104">The system provides six stock fonts.</span></span> <span data-ttu-id="4872b-105">Un tipo di carattere Stock è un tipo di carattere logico che un'applicazione può ottenere chiamando la funzione [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) e specificando il tipo di carattere richiesto.</span><span class="sxs-lookup"><span data-stu-id="4872b-105">A stock font is a logical font that an application can obtain by calling the [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function and specifying the requested font.</span></span> <span data-ttu-id="4872b-106">L'elenco seguente contiene i valori che è possibile specificare per ottenere un tipo di carattere di magazzino.</span><span class="sxs-lookup"><span data-stu-id="4872b-106">The following list contains the values that you can specify to obtain a stock font.</span></span>



| <span data-ttu-id="4872b-107">Valore</span><span class="sxs-lookup"><span data-stu-id="4872b-107">Value</span></span>                 | <span data-ttu-id="4872b-108">Significato</span><span class="sxs-lookup"><span data-stu-id="4872b-108">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4872b-109">\_tipo di \_ carattere fisso ANSI</span><span class="sxs-lookup"><span data-stu-id="4872b-109">ANSI\_FIXED\_FONT</span></span>     | <span data-ttu-id="4872b-110">Specifica un tipo di carattere a spaziatura fissa basato sul set di caratteri di Windows.</span><span class="sxs-lookup"><span data-stu-id="4872b-110">Specifies a monospace font based on the Windows character set.</span></span> <span data-ttu-id="4872b-111">Viene in genere utilizzato un tipo di carattere Courier.</span><span class="sxs-lookup"><span data-stu-id="4872b-111">A Courier font is typically used.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="4872b-112">\_tipo di \_ carattere ANSI var</span><span class="sxs-lookup"><span data-stu-id="4872b-112">ANSI\_VAR\_FONT</span></span>       | <span data-ttu-id="4872b-113">Specifica un tipo di carattere proporzionale in base al set di caratteri di Windows.</span><span class="sxs-lookup"><span data-stu-id="4872b-113">Specifies a proportional font based on the Windows character set.</span></span> <span data-ttu-id="4872b-114">MS Sans Serif viene in genere usato.</span><span class="sxs-lookup"><span data-stu-id="4872b-114">MS Sans Serif is typically used.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="4872b-115">\_tipo di carattere predefinito del dispositivo \_</span><span class="sxs-lookup"><span data-stu-id="4872b-115">DEVICE\_DEFAULT\_FONT</span></span> | <span data-ttu-id="4872b-116">Specifica il tipo di carattere preferito per il dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="4872b-116">Specifies the preferred font for the specified device.</span></span> <span data-ttu-id="4872b-117">Si tratta in genere del tipo di carattere di sistema per i dispositivi di visualizzazione. per alcune stampanti a matrice di punti, tuttavia, si tratta di un tipo di carattere residente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4872b-117">This is typically the System font for display devices; however, for some dot-matrix printers this is a font that is resident on the device.</span></span> <span data-ttu-id="4872b-118">La stampa con questo tipo di carattere è in genere più veloce rispetto alla stampa con un tipo di carattere bitmap scaricato.</span><span class="sxs-lookup"><span data-stu-id="4872b-118">(Printing with this font is usually faster than printing with a downloaded, bitmap font).</span></span>    |
| <span data-ttu-id="4872b-119">\_tipo di \_ carattere fisso OEM</span><span class="sxs-lookup"><span data-stu-id="4872b-119">OEM\_FIXED\_FONT</span></span>      | <span data-ttu-id="4872b-120">Specifica un tipo di carattere a spaziatura fissa basato su un set di caratteri OEM.</span><span class="sxs-lookup"><span data-stu-id="4872b-120">Specifies a monospace font based on an OEM character set.</span></span> <span data-ttu-id="4872b-121">Per i computer IBM e compatibili, il tipo di carattere OEM è basato sul set di caratteri IBM PC.</span><span class="sxs-lookup"><span data-stu-id="4872b-121">For IBM computers and compatibles, the OEM font is based on the IBM PC character set.</span></span>                                                                                                                                                 |
| <span data-ttu-id="4872b-122">tipo di carattere del sistema \_</span><span class="sxs-lookup"><span data-stu-id="4872b-122">SYSTEM\_FONT</span></span>          | <span data-ttu-id="4872b-123">Specifica il tipo di carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="4872b-123">Specifies the System font.</span></span> <span data-ttu-id="4872b-124">Si tratta di un tipo di carattere proporzionale in base al set di caratteri di Windows e viene utilizzato dal sistema operativo per visualizzare i titoli delle finestre, i nomi dei menu e il testo nelle finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4872b-124">This is a proportional font based on the Windows character set, and is used by the operating system to display window titles, menu names, and text in dialog boxes.</span></span> <span data-ttu-id="4872b-125">Il tipo di carattere del sistema è sempre disponibile.</span><span class="sxs-lookup"><span data-stu-id="4872b-125">The System font is always available.</span></span> <span data-ttu-id="4872b-126">Altri tipi di carattere sono disponibili solo se sono stati installati.</span><span class="sxs-lookup"><span data-stu-id="4872b-126">Other fonts are available only if they have been installed.</span></span> |
| <span data-ttu-id="4872b-127">\_tipo di carattere fisso di sistema \_</span><span class="sxs-lookup"><span data-stu-id="4872b-127">SYSTEM\_FIXED\_FONT</span></span>   | <span data-ttu-id="4872b-128">Specifica un tipo di carattere a spaziatura fissa compatibile con il tipo di carattere di sistema nelle prime versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="4872b-128">Specifies a monospace font compatible with the System font in early versions of Windows.</span></span>                                                                                                                                                                                                        |



 

<span data-ttu-id="4872b-129">Per ulteriori informazioni sui tipi di carattere, vedere [informazioni sui tipi di carattere](about-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="4872b-129">For more information on fonts, see [About Fonts](about-fonts.md).</span></span>

<span data-ttu-id="4872b-130">Nell'esempio seguente viene recuperato un handle per il tipo di carattere di azione variabile, viene selezionato in un contesto di dispositivo e viene quindi scritta una stringa utilizzando il tipo di carattere seguente:</span><span class="sxs-lookup"><span data-stu-id="4872b-130">The following example retrieves a handle to the variable stock font, selects it into a device context, and then writes a string using that font:</span></span>


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



<span data-ttu-id="4872b-131">Se non sono disponibili altri tipi di carattere predefiniti, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) restituisce un handle per il tipo di carattere del sistema (tipo di carattere del sistema \_ ).</span><span class="sxs-lookup"><span data-stu-id="4872b-131">If other stock fonts are not available, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) returns a handle to the System font (SYSTEM\_FONT).</span></span> <span data-ttu-id="4872b-132">Usare i tipi di carattere predefiniti solo se la modalità di mapping per il contesto di dispositivo dell'applicazione è MM \_ testo.</span><span class="sxs-lookup"><span data-stu-id="4872b-132">You should use stock fonts only if the mapping mode for your application's device context is MM\_TEXT.</span></span>

 

 



