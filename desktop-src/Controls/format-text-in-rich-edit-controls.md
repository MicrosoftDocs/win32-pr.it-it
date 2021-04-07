---
title: Come formattare il testo nei controlli Rich Edit
description: Un'applicazione può inviare messaggi a un controllo Rich Edit per formattare i caratteri e i paragrafi e recuperare le informazioni di formattazione.
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724283"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a><span data-ttu-id="d0d8e-103">Come formattare il testo nei controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="d0d8e-103">How to Format Text in Rich Edit Controls</span></span>

<span data-ttu-id="d0d8e-104">Un'applicazione può inviare messaggi a un controllo Rich Edit per formattare i caratteri e i paragrafi e recuperare le informazioni di formattazione.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-104">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="d0d8e-105">Gli attributi di formattazione dei paragrafi includono l'allineamento, le tabulazioni, i rientri, la numerazione e le tabelle semplici.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-105">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="d0d8e-106">Per i caratteri, è possibile specificare il nome, la dimensione, il colore e gli effetti del tipo di carattere, ad esempio grassetto, corsivo e protetto.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-106">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d0d8e-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="d0d8e-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d0d8e-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="d0d8e-108">Technologies</span></span>

-   [<span data-ttu-id="d0d8e-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="d0d8e-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d0d8e-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="d0d8e-110">Prerequisites</span></span>

-   <span data-ttu-id="d0d8e-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d0d8e-111">C/C++</span></span>
-   <span data-ttu-id="d0d8e-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="d0d8e-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d0d8e-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="d0d8e-113">Instructions</span></span>

### <a name="format-text-in-a-rich-edit-control"></a><span data-ttu-id="d0d8e-114">Formattare il testo in un controllo Rich Edit</span><span class="sxs-lookup"><span data-stu-id="d0d8e-114">Format Text in a Rich Edit Control</span></span>

<span data-ttu-id="d0d8e-115">È possibile applicare la formattazione dei paragrafi usando il messaggio [**\_ SETPARAFORMAT em**](em-setparaformat.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d8e-115">You can apply paragraph formatting by using the [**EM\_SETPARAFORMAT**](em-setparaformat.md) message.</span></span> <span data-ttu-id="d0d8e-116">Per determinare la formattazione del paragrafo corrente per il testo selezionato, utilizzare il messaggio [**\_ GETPARAFORMAT em**](em-getparaformat.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d8e-116">To determine the current paragraph formatting for the selected text, use the [**EM\_GETPARAFORMAT**](em-getparaformat.md) message.</span></span> <span data-ttu-id="d0d8e-117">La struttura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) o [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) viene utilizzata con entrambi i messaggi per specificare gli attributi di formattazione dei paragrafi.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-117">The [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) or [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure is used with both messages to specify paragraph formatting attributes.</span></span>

<span data-ttu-id="d0d8e-118">È possibile applicare la formattazione dei caratteri tramite il messaggio [**\_ SETCHARFORMAT em**](em-setcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d8e-118">You can apply character formatting by using the [**EM\_SETCHARFORMAT**](em-setcharformat.md) message.</span></span> <span data-ttu-id="d0d8e-119">Per determinare la formattazione dei caratteri corrente per il testo selezionato, è possibile usare il messaggio [**\_ GETCHARFORMAT em**](em-getcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d8e-119">To determine the current character formatting for the selected text, you can use the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span> <span data-ttu-id="d0d8e-120">La struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) o [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) viene utilizzata con entrambi i messaggi per specificare gli attributi carattere.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-120">The [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) or [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure is used with both messages to specify character attributes.</span></span>

<span data-ttu-id="d0d8e-121">È anche possibile usare i messaggi [**em \_ SETCHARFORMAT**](em-setcharformat.md) e [**em \_ GETCHARFORMAT**](em-getcharformat.md) per impostare e recuperare la formattazione dei caratteri del punto di inserimento, ovvero la formattazione applicata a tutti i caratteri inseriti successivamente.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-121">You can also use [**EM\_SETCHARFORMAT**](em-setcharformat.md) and [**EM\_GETCHARFORMAT**](em-getcharformat.md) messages to set and retrieve the character formatting of the insertion point, which is the formatting that is applied to any subsequently inserted characters.</span></span> <span data-ttu-id="d0d8e-122">Se, ad esempio, un'applicazione imposta la formattazione dei caratteri predefinita su grassetto e l'utente digita un carattere, il carattere è in grassetto.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-122">For example, if an application sets the default character formatting to bold and the user then types a character, that character is bold.</span></span>

<span data-ttu-id="d0d8e-123">La formattazione dei caratteri del punto di inserimento viene applicata al testo appena inserito solo se la selezione corrente è vuota (se la selezione corrente è un punto di inserimento).</span><span class="sxs-lookup"><span data-stu-id="d0d8e-123">The character formatting of the insertion point is applied to newly inserted text only if the current selection is empty (if the current selection is an insertion point).</span></span> <span data-ttu-id="d0d8e-124">In caso contrario, il nuovo testo presuppone la formattazione dei caratteri del testo che sostituisce.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-124">Otherwise, the new text assumes the character formatting of the text it replaces.</span></span> <span data-ttu-id="d0d8e-125">Se la selezione viene modificata, la formattazione dei caratteri predefinita cambia in base al primo carattere della nuova selezione.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-125">If the selection changes, the default character formatting changes to match the first character in the new selection.</span></span>

<span data-ttu-id="d0d8e-126">L'effetto carattere protetto è univoco in quanto non modifica l'aspetto del testo.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-126">The protected character effect is unique in that it does not change the appearance of text.</span></span> <span data-ttu-id="d0d8e-127">Se l'utente tenta di modificare il testo protetto, un controllo Rich Edit invia alla finestra padre un codice di notifica [it \_ protetto](en-protected.md) , consentendo alla finestra padre di consentire o impedire la modifica.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-127">If the user attempts to modify protected text, a rich edit control sends its parent window an [EN\_PROTECTED](en-protected.md) notification code, allowing the parent window to allow or prevent the change.</span></span> <span data-ttu-id="d0d8e-128">Per ricevere il codice di notifica, è necessario abilitarlo usando il [**messaggio \_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d8e-128">To receive this notification code, you must enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="d0d8e-129">Il colore di primo piano è sempre un attributo di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-129">Foreground color is always a character attribute.</span></span> <span data-ttu-id="d0d8e-130">In Microsoft Rich Edit 1,0, il colore di sfondo è solo una proprietà del controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d0d8e-130">In Microsoft Rich Edit 1.0, background color is only a property of the rich edit control.</span></span> <span data-ttu-id="d0d8e-131">Per impostare il colore di sfondo predefinito, usare il messaggio [**\_ SETBKGNDCOLOR em**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d8e-131">To set the default background color, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span> <span data-ttu-id="d0d8e-132">Si noti che Rich Edit non supporta il messaggio [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d8e-132">Note that Rich Edit does not support the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0d8e-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0d8e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0d8e-134">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="d0d8e-134">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="d0d8e-135">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="d0d8e-135">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




