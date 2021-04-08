---
title: Informazioni sui controlli SysLink
description: Un controllo SysLink è una finestra che esegue il rendering del testo contrassegnato e invia una notifica all'applicazione quando gli utenti fanno clic sui collegamenti ipertestuali incorporati. Questo controllo offre una comoda alternativa all'uso del pulsante di collegamento al comando. Per altre informazioni, vedere tipi di pulsanti.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047425"
---
# <a name="about-syslink-controls"></a><span data-ttu-id="cbf50-105">Informazioni sui controlli SysLink</span><span class="sxs-lookup"><span data-stu-id="cbf50-105">About SysLink Controls</span></span>

<span data-ttu-id="cbf50-106">Un controllo SysLink è una finestra che esegue il rendering del testo contrassegnato e invia una notifica all'applicazione quando gli utenti fanno clic sui collegamenti ipertestuali incorporati.</span><span class="sxs-lookup"><span data-stu-id="cbf50-106">A SysLink control is a window that renders marked-up text, and notifies the application when users click its embedded hyperlinks.</span></span> <span data-ttu-id="cbf50-107">Questo controllo offre una comoda alternativa all'uso del [**pulsante di collegamento al comando**](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="cbf50-107">This control provides a convenient alternative to using the [**Command link button**](button-styles.md).</span></span> <span data-ttu-id="cbf50-108">Per altre informazioni, vedere [tipi di pulsanti](button-types-and-styles.md).</span><span class="sxs-lookup"><span data-stu-id="cbf50-108">For more information, see [Button Types](button-types-and-styles.md).</span></span>

<span data-ttu-id="cbf50-109">Ogni controllo SysLink può supportare più collegamenti ipertestuali ed è possibile accedere a ogni collegamento ipertestuale tramite un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="cbf50-109">Each SysLink control can support multiple hyperlinks, and you can access each hyperlink through a zero-based index.</span></span> <span data-ttu-id="cbf50-110">Il controllo SysLink è definito nel ComCtl32.dll versione 6 ed è necessario un manifesto o una direttiva che specifichi che la versione 6 della DLL deve essere utilizzata se disponibile.</span><span class="sxs-lookup"><span data-stu-id="cbf50-110">The SysLink control is defined in the ComCtl32.dll version 6, and it requires a manifest or directive that specifies that version 6 of the DLL should be used if it is available.</span></span> <span data-ttu-id="cbf50-111">Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cbf50-111">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

<span data-ttu-id="cbf50-112">Questo articolo include le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="cbf50-112">This article contains the following sections.</span></span>

-   [<span data-ttu-id="cbf50-113">Markup SysLink</span><span class="sxs-lookup"><span data-stu-id="cbf50-113">SysLink Markup</span></span>](#syslink-markup)
-   [<span data-ttu-id="cbf50-114">Attributi di collegamento</span><span class="sxs-lookup"><span data-stu-id="cbf50-114">Link Attributes</span></span>](#link-attributes)
-   [<span data-ttu-id="cbf50-115">Stati di collegamento</span><span class="sxs-lookup"><span data-stu-id="cbf50-115">Link States</span></span>](#link-states)
-   [<span data-ttu-id="cbf50-116">Limitazioni sulla visualizzazione del testo bidirezionale</span><span class="sxs-lookup"><span data-stu-id="cbf50-116">Limitations on Bidirectional Text Display</span></span>](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a><span data-ttu-id="cbf50-117">Markup SysLink</span><span class="sxs-lookup"><span data-stu-id="cbf50-117">SysLink Markup</span></span>

<span data-ttu-id="cbf50-118">Il controllo SysLink supporta il tag di ancoraggio ( &lt; a &gt; ) insieme agli attributi **href** e **ID**.</span><span class="sxs-lookup"><span data-stu-id="cbf50-118">The SysLink control supports the anchor tag(&lt;a&gt;) along with the attributes **HREF** and **ID**.</span></span> <span data-ttu-id="cbf50-119">Un **href** può essere qualsiasi protocollo, ad esempio http, FTP e mailto.</span><span class="sxs-lookup"><span data-stu-id="cbf50-119">An **HREF** can be any protocol, such as http, ftp, and mailto.</span></span> <span data-ttu-id="cbf50-120">Un **ID** è un nome facoltativo, univoco all'interno di un controllo Syslink, ed è associato a un singolo collegamento.</span><span class="sxs-lookup"><span data-stu-id="cbf50-120">An **ID** is an optional name, unique within a SysLink control, and it is associated with an individual link.</span></span> <span data-ttu-id="cbf50-121">Ai collegamenti viene inoltre assegnato un indice in base zero in base alla relativa posizione all'interno della stringa.</span><span class="sxs-lookup"><span data-stu-id="cbf50-121">Links are also assigned a zero-based index according to their position within the string.</span></span> <span data-ttu-id="cbf50-122">Questo indice viene utilizzato per accedere a un collegamento.</span><span class="sxs-lookup"><span data-stu-id="cbf50-122">This index is used to access a link.</span></span>

## <a name="link-attributes"></a><span data-ttu-id="cbf50-123">Attributi di collegamento</span><span class="sxs-lookup"><span data-stu-id="cbf50-123">Link Attributes</span></span>

<span data-ttu-id="cbf50-124">È possibile impostare gli attributi di ogni collegamento all'interno del tag di ancoraggio per ogni collegamento o inviando il messaggio di [**\_ elemento**](lm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="cbf50-124">Each link's attributes can be set either within the anchor tag for each link or by sending the [**LM\_SETITEM**](lm-setitem.md) message.</span></span> <span data-ttu-id="cbf50-125">Se si imposta un attributo specificandone il valore all'interno della stringa di inizializzazione, viene semplicemente inizializzato.</span><span class="sxs-lookup"><span data-stu-id="cbf50-125">Setting an attribute by specifying it within the initialization string merely initializes the value.</span></span> <span data-ttu-id="cbf50-126">È possibile modificare il valore di un attributo tramite l'uso successivo del messaggio di **\_ elemento** .</span><span class="sxs-lookup"><span data-stu-id="cbf50-126">You can change the value of an attribute through subsequent use of the **LM\_SETITEM** message.</span></span>

## <a name="link-states"></a><span data-ttu-id="cbf50-127">Stati di collegamento</span><span class="sxs-lookup"><span data-stu-id="cbf50-127">Link States</span></span>

<span data-ttu-id="cbf50-128">Gli elementi del collegamento possono trovarsi in uno dei tre stati, rappresentati dai flag nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="cbf50-128">Link items can be in any one of three states, represented by the flags in the following table.</span></span>



| <span data-ttu-id="cbf50-129">Flag di stato</span><span class="sxs-lookup"><span data-stu-id="cbf50-129">State flag</span></span>   | <span data-ttu-id="cbf50-130">Aspetto e significato</span><span class="sxs-lookup"><span data-stu-id="cbf50-130">Appearance and meaning</span></span>                                            |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="cbf50-131">LIS con stato \_ attivo</span><span class="sxs-lookup"><span data-stu-id="cbf50-131">LIS\_FOCUSED</span></span> | <span data-ttu-id="cbf50-132">Il collegamento ha lo stato attivo della tastiera e premendo invio lo attiva.</span><span class="sxs-lookup"><span data-stu-id="cbf50-132">The link has the keyboard focus, and pressing Enter activates it.</span></span> |
| <span data-ttu-id="cbf50-133">LIS \_ abilitato</span><span class="sxs-lookup"><span data-stu-id="cbf50-133">LIS\_ENABLED</span></span> | <span data-ttu-id="cbf50-134">Il collegamento è abilitato.</span><span class="sxs-lookup"><span data-stu-id="cbf50-134">The link is enabled.</span></span>                                              |
| <span data-ttu-id="cbf50-135">LIS \_ visitato</span><span class="sxs-lookup"><span data-stu-id="cbf50-135">LIS\_VISITED</span></span> | <span data-ttu-id="cbf50-136">L'utente ha già visitato l'URL rappresentato dal collegamento.</span><span class="sxs-lookup"><span data-stu-id="cbf50-136">The user has already visited the URL represented by the link.</span></span>     |



 

## <a name="limitations-on-bidirectional-text-display"></a><span data-ttu-id="cbf50-137">Limitazioni sulla visualizzazione del testo bidirezionale</span><span class="sxs-lookup"><span data-stu-id="cbf50-137">Limitations on Bidirectional Text Display</span></span>

<span data-ttu-id="cbf50-138">Alcuni linguaggi, come l'arabo o l'ebraico, sono scritti da destra a sinistra (RTL); L'inglese è scritto da sinistra a destra (LTR).</span><span class="sxs-lookup"><span data-stu-id="cbf50-138">Some languages, such as Arabic or Hebrew, are written right-to-left (RTL); English is written left-to-right (LTR).</span></span> <span data-ttu-id="cbf50-139">La combinazione di RTL con LTR viene chiamata testo bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="cbf50-139">Combining RTL with LTR is called bidirectional text.</span></span> <span data-ttu-id="cbf50-140">La combinazione di costrutti di markup direzionali LTR e RTL Unicode o HTML in stringhe di risorsa, come marcatori di flusso bidirezionali per controllare il flusso di stringhe, potrebbe non produrre il risultato previsto quando si usa un controllo SysLink.</span><span class="sxs-lookup"><span data-stu-id="cbf50-140">Mixing LTR and RTL Unicode or HTML directional markup constructs in resource strings, as bidirectional flow markers to control the flow of strings, may not produce the expected result when using a SysLink control.</span></span> <span data-ttu-id="cbf50-141">Ad esempio, una frase con contrassegno LTR potrebbe non essere visualizzata correttamente nel contesto di RTL.</span><span class="sxs-lookup"><span data-stu-id="cbf50-141">For instance, an LTR-marked sentence may not display correctly in RTL context.</span></span>

> [!Note]  
> <span data-ttu-id="cbf50-142">I controlli SysLink non supportano la visualizzazione bidirezionale in tutti gli scenari.</span><span class="sxs-lookup"><span data-stu-id="cbf50-142">SysLink controls do not support bidirectional display under all scenarios.</span></span> <span data-ttu-id="cbf50-143">Usare un controllo SysLink solo se si è certi che un semplice layout di LTR o RTL è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="cbf50-143">Use a SysLink control only if you know that a simple LTR or RTL layout is adequate.</span></span> <span data-ttu-id="cbf50-144">In caso contrario, prendere in considerazione l'utilizzo di una tecnologia più avanzata, ad esempio [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cbf50-144">Otherwise, consider using a more advanced technology such as [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span></span>

 

 

 