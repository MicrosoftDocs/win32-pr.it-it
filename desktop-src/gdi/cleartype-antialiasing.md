---
description: Anti-aliasing di Microsoft ClearType è un metodo di smussatura che migliora la risoluzione dello schermo del tipo di carattere rispetto all'anti-aliasing tradizionale.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: ClearType Antialiasing (Anti-aliasing ClearType)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbe7ae1a6c99fcee826c576b7671aea6e9ce6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978775"
---
# <a name="cleartype-antialiasing"></a><span data-ttu-id="c250d-103">ClearType Antialiasing (Anti-aliasing ClearType)</span><span class="sxs-lookup"><span data-stu-id="c250d-103">ClearType Antialiasing</span></span>

<span data-ttu-id="c250d-104">Anti-aliasing di Microsoft ClearType è un metodo di smussatura che migliora la risoluzione dello schermo del tipo di carattere rispetto all'anti-aliasing tradizionale.</span><span class="sxs-lookup"><span data-stu-id="c250d-104">Microsoft ClearType antialiasing is a smoothing method that improves font display resolution over traditional antialiasing.</span></span> <span data-ttu-id="c250d-105">Migliora significativamente la leggibilità dei monitor LCD a colori con un'interfaccia digitale, ad esempio i computer portatili e le visualizzazioni desktop flat di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="c250d-105">It dramatically improves readability on color LCD monitors with a digital interface, such as those in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="c250d-106">Anche la leggibilità sulle schermate CRT è stata migliorata.</span><span class="sxs-lookup"><span data-stu-id="c250d-106">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="c250d-107">Tuttavia, ClearType dipende dall'orientamento e dall'ordinamento dei nastri LCD.</span><span class="sxs-lookup"><span data-stu-id="c250d-107">However, ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="c250d-108">Attualmente, ClearType viene implementato solo per gli LCD con striping verticali ordinati RGB.</span><span class="sxs-lookup"><span data-stu-id="c250d-108">Currently, ClearType is implemented only for LCDs with vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="c250d-109">In particolare, ciò influiscono sui Tablet PC, in cui la visualizzazione può essere orientata in qualsiasi direzione e le schermate che è possibile trasformare dall'orizzontale al verticale.</span><span class="sxs-lookup"><span data-stu-id="c250d-109">In particular, this affects tablet PCs, where the display can be oriented in any direction, and those screens that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="c250d-110">Anti-aliasing ClearType consentito:</span><span class="sxs-lookup"><span data-stu-id="c250d-110">ClearType antialiasing is allowed:</span></span>

-   <span data-ttu-id="c250d-111">Per il colore a 16, 24 e 32 bit (disabilitato per 256 colori o meno)</span><span class="sxs-lookup"><span data-stu-id="c250d-111">For 16-, 24-, and 32-bit color (disabled for 256 colors or less)</span></span>
-   <span data-ttu-id="c250d-112">Per il controller di dominio della schermata e della memoria</span><span class="sxs-lookup"><span data-stu-id="c250d-112">For screen DC and memory DC (not for printer DC)</span></span>
-   <span data-ttu-id="c250d-113">Per i tipi di carattere TrueType e OpenType con le strutture TrueType</span><span class="sxs-lookup"><span data-stu-id="c250d-113">For TrueType fonts and OpenType fonts with TrueType outlines</span></span>

<span data-ttu-id="c250d-114">Anti-aliasing ClearType disabilitato:</span><span class="sxs-lookup"><span data-stu-id="c250d-114">ClearType antialiasing is disabled:</span></span>

-   <span data-ttu-id="c250d-115">In Terminal Server client</span><span class="sxs-lookup"><span data-stu-id="c250d-115">Under terminal server client</span></span>
-   <span data-ttu-id="c250d-116">Per i tipi di carattere bitmap, i tipi di carattere vettoriali, i tipi di carattere del dispositivo, i tipi 1 o i tipi di carattere OpenType</span><span class="sxs-lookup"><span data-stu-id="c250d-116">For bitmap fonts, vector fonts, device fonts, Type 1 fonts, or Postscript OpenType fonts without TrueType outlines</span></span>
-   <span data-ttu-id="c250d-117">Se il tipo di carattere ha ottimizzato le bitmap incorporate, solo per le dimensioni dei tipi di carattere che contengono le bitmap incorporate</span><span class="sxs-lookup"><span data-stu-id="c250d-117">If the font has tuned embedded bitmaps, only for those font sizes that contain the embedded bitmaps</span></span>

<span data-ttu-id="c250d-118">Per attivare l'anti-aliasing ClearType, chiamare [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) una volta per attivare la smussatura dei caratteri e quindi una seconda volta per impostare il tipo di smussatura su Fe \_ FONTSMOOTHINGCLEARTYPE, come illustrato nell'esempio di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="c250d-118">To activate ClearType antialiasing, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) once to turn on font smoothing and then a second time to set the smoothing type to FE\_FONTSMOOTHINGCLEARTYPE, as shown in the following code sample:</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHING,
                     TRUE,
                     0,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE);
SystemParametersInfo(SPI_SETFONTSMOOTHINGTYPE,
                     0,
                     (PVOID)FE_FONTSMOOTHINGCLEARTYPE,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="c250d-119">È possibile modificare l'aspetto del testo modificando il valore di contrasto usato nell'algoritmo ClearType.</span><span class="sxs-lookup"><span data-stu-id="c250d-119">You can adjust the appearance of text by changing the contrast value used in the ClearType algorithm.</span></span> <span data-ttu-id="c250d-120">Il valore predefinito è 1.400, ma può essere qualsiasi valore compreso tra 1.000 e 2.200.</span><span class="sxs-lookup"><span data-stu-id="c250d-120">The default is 1,400, but it can be any value from 1,000 to 2,200.</span></span> <span data-ttu-id="c250d-121">A seconda del dispositivo di visualizzazione e della sensibilità dell'utente ai colori, un valore di contrasto superiore o inferiore può migliorare la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="c250d-121">Depending on the display device and the user's sensitivity to colors, a higher or lower contrast value may improve readability.</span></span> <span data-ttu-id="c250d-122">Per modificare il contrasto, chiamare [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETFONTSMOOTHINGCONTRAST.</span><span class="sxs-lookup"><span data-stu-id="c250d-122">To change the contrast, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETFONTSMOOTHINGCONTRAST.</span></span> <span data-ttu-id="c250d-123">Il codice seguente imposta il valore di contrasto su 1.600.</span><span class="sxs-lookup"><span data-stu-id="c250d-123">The following code sets the contrast value to 1,600.</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="c250d-124">Per la compatibilità delle applicazioni, è necessario considerare i seguenti dettagli:</span><span class="sxs-lookup"><span data-stu-id="c250d-124">You should consider the following details for application compatibility:</span></span>

-   <span data-ttu-id="c250d-125">Il rendering del testo con ClearType è leggermente più lento rispetto all'anti-aliasing standard.</span><span class="sxs-lookup"><span data-stu-id="c250d-125">Text rendering with ClearType is slightly slower than with standard antialiasing.</span></span>
-   <span data-ttu-id="c250d-126">Le applicazioni non devono utilizzare XOR per visualizzare il testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="c250d-126">Applications should not use XOR to display selected text.</span></span> <span data-ttu-id="c250d-127">Le applicazioni devono impostare il colore di sfondo e visualizzare nuovamente il testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="c250d-127">Applications should set the background color and redisplay the selected text.</span></span>
-   <span data-ttu-id="c250d-128">Le applicazioni non devono disegnare lo stesso testo in modalità trasparente.</span><span class="sxs-lookup"><span data-stu-id="c250d-128">Applications should not paint the same text on top of itself in transparent mode.</span></span> <span data-ttu-id="c250d-129">In tal caso, i pixel perimetrali con antialias verranno colorati con se stessi anziché con il colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="c250d-129">If this occurs, the edge pixels that are antialiased will color merge with themselves instead of with the background color.</span></span> <span data-ttu-id="c250d-130">In questo modo si ottiene un bordo oscurato e colorato.</span><span class="sxs-lookup"><span data-stu-id="c250d-130">This results in darkened and colorful edges.</span></span>
-   <span data-ttu-id="c250d-131">Le applicazioni non devono disegnare il testo disegnando i caratteri singolarmente in modalità opaca poiché il bordo di un carattere può essere ritagliato in base al carattere seguente.</span><span class="sxs-lookup"><span data-stu-id="c250d-131">Applications should not paint text by painting the characters individually when in opaque mode because the edge of a character may be clipped by the following character.</span></span> <span data-ttu-id="c250d-132">Questo problema si verifica perché un carattere smussato con ClearType può avere una larghezza negativa A o C, dove il carattere regolare ha una larghezza positiva A o C.</span><span class="sxs-lookup"><span data-stu-id="c250d-132">This occurs because a character that is smoothed with ClearType may have a negative A or C width where the regular character has a positive A or C width.</span></span> <span data-ttu-id="c250d-133">È garantita solo la larghezza B del carattere.</span><span class="sxs-lookup"><span data-stu-id="c250d-133">Only the B width of the character is guaranteed to be the same.</span></span> <span data-ttu-id="c250d-134">Analogamente, le applicazioni devono prestare attenzione se il testo smussato è prossimo al testo non uniforme.</span><span class="sxs-lookup"><span data-stu-id="c250d-134">Likewise, applications should be careful if smoothed text is next to unsmoothed text.</span></span>
-   <span data-ttu-id="c250d-135">Se un'applicazione esegue il rendering del testo e quindi modifica la bitmap, la smussatura dei caratteri deve essere disattivata impostando il membro **lfQuality** della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) sulla \_ qualità NONANTIALIASED.</span><span class="sxs-lookup"><span data-stu-id="c250d-135">If an application renders text and then manipulates the bitmap, font smoothing should be turned off by setting the **lfQuality** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure to NONANTIALIASED\_QUALITY.</span></span> <span data-ttu-id="c250d-136">Ad esempio, un gioco può aggiungere un effetto ombreggiatura bitmap oppure il testo di cui è stato eseguito il rendering in una bitmap può essere ridimensionato per produrre un ThumbView.</span><span class="sxs-lookup"><span data-stu-id="c250d-136">For example, a game may add a bitmap shadow effect, or text rendered into a bitmap may be scaled to produce a thumbview.</span></span>
-   <span data-ttu-id="c250d-137">Se l'utente è in esecuzione in modalità verticale (ovvero lo striping di monitoraggio è orizzontale), l'anti-aliasing ClearType dovrebbe essere disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c250d-137">If the user is running in portrait mode (that is, monitor striping is horizontal) ClearType antialiasing should be disabled.</span></span>

<span data-ttu-id="c250d-138">Il parametro *fdwQuality* in [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) e il membro **lfQuality** di [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) accettano il flag di \_ qualità CLEARTYPE.</span><span class="sxs-lookup"><span data-stu-id="c250d-138">The *fdwQuality* parameter in [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) and the **lfQuality** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) accept the CLEARTYPE\_QUALITY flag.</span></span> <span data-ttu-id="c250d-139">La rasterizzazione dei tipi di carattere creati con questo flag utilizzerà l'rasterizzatore ClearType.</span><span class="sxs-lookup"><span data-stu-id="c250d-139">Rasterization of fonts created with this flag will use the ClearType rasterizer.</span></span> <span data-ttu-id="c250d-140">Questo flag non ha alcun effetto sulle versioni precedenti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c250d-140">This flag has no effect on previous versions of the operating system.</span></span>

 

 
