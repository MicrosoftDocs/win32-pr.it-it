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
# <a name="how-to-format-text-in-rich-edit-controls"></a>Come formattare il testo nei controlli Rich Edit

Un'applicazione può inviare messaggi a un controllo Rich Edit per formattare i caratteri e i paragrafi e recuperare le informazioni di formattazione. Gli attributi di formattazione dei paragrafi includono l'allineamento, le tabulazioni, i rientri, la numerazione e le tabelle semplici. Per i caratteri, è possibile specificare il nome, la dimensione, il colore e gli effetti del tipo di carattere, ad esempio grassetto, corsivo e protetto.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="format-text-in-a-rich-edit-control"></a>Formattare il testo in un controllo Rich Edit

È possibile applicare la formattazione dei paragrafi usando il messaggio [**\_ SETPARAFORMAT em**](em-setparaformat.md) . Per determinare la formattazione del paragrafo corrente per il testo selezionato, utilizzare il messaggio [**\_ GETPARAFORMAT em**](em-getparaformat.md) . La struttura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) o [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) viene utilizzata con entrambi i messaggi per specificare gli attributi di formattazione dei paragrafi.

È possibile applicare la formattazione dei caratteri tramite il messaggio [**\_ SETCHARFORMAT em**](em-setcharformat.md) . Per determinare la formattazione dei caratteri corrente per il testo selezionato, è possibile usare il messaggio [**\_ GETCHARFORMAT em**](em-getcharformat.md) . La struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) o [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) viene utilizzata con entrambi i messaggi per specificare gli attributi carattere.

È anche possibile usare i messaggi [**em \_ SETCHARFORMAT**](em-setcharformat.md) e [**em \_ GETCHARFORMAT**](em-getcharformat.md) per impostare e recuperare la formattazione dei caratteri del punto di inserimento, ovvero la formattazione applicata a tutti i caratteri inseriti successivamente. Se, ad esempio, un'applicazione imposta la formattazione dei caratteri predefinita su grassetto e l'utente digita un carattere, il carattere è in grassetto.

La formattazione dei caratteri del punto di inserimento viene applicata al testo appena inserito solo se la selezione corrente è vuota (se la selezione corrente è un punto di inserimento). In caso contrario, il nuovo testo presuppone la formattazione dei caratteri del testo che sostituisce. Se la selezione viene modificata, la formattazione dei caratteri predefinita cambia in base al primo carattere della nuova selezione.

L'effetto carattere protetto è univoco in quanto non modifica l'aspetto del testo. Se l'utente tenta di modificare il testo protetto, un controllo Rich Edit invia alla finestra padre un codice di notifica [it \_ protetto](en-protected.md) , consentendo alla finestra padre di consentire o impedire la modifica. Per ricevere il codice di notifica, è necessario abilitarlo usando il [**messaggio \_ SETEVENTMASK em**](em-seteventmask.md) .

Il colore di primo piano è sempre un attributo di tipo carattere. In Microsoft Rich Edit 1,0, il colore di sfondo è solo una proprietà del controllo Rich Edit. Per impostare il colore di sfondo predefinito, usare il messaggio [**\_ SETBKGNDCOLOR em**](em-setbkgndcolor.md) . Si noti che Rich Edit non supporta il messaggio [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




