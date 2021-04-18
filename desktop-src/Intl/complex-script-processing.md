---
description: "Di seguito sono riportate le opzioni per la visualizzazione e l'elaborazione correlata del testo per supportare effetti tipografici o script complessi: Text functionsEdit controlsRich Edit controlsUniscribe"
ms.assetid: 337bc798-e75d-4389-8fea-577eb82a0ed5
title: Elaborazione di script complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e4be6295bff949c8e29036ef3af496c673575e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312878"
---
# <a name="complex-script-processing"></a>Elaborazione di script complessi

Di seguito sono riportate le opzioni per la visualizzazione e l'elaborazione correlata del testo per supportare effetti tipografici o script complessi:

-   Funzioni di testo
-   Controlli di modifica
-   Controlli Rich Edit
-   Uniscribe

Le opzioni scelte dipendono dai fattori seguenti:

-   Tipo di testo o script.
-   Modello di implementazione, ad esempio il layout del testo e la gestione di interruzioni di riga da parte dell'applicazione.
-   Aggiornamento di un'applicazione esistente rispetto alla creazione di una nuova applicazione.

In generale, un'applicazione che esegue un'elaborazione di script relativamente semplice può scegliere qualsiasi opzione per l'elaborazione di script complessi. Tuttavia, per il controllo più completo dell'elaborazione di script complessi, è consigliabile usare Uniscribe.

## <a name="complex-script-processing-using-text-functions"></a>Elaborazione di script complessi con funzioni di testo

Le applicazioni che usano per lo più testo normale, ovvero testo che usa lo stesso carattere tipografico, peso, colore e così via, hanno scritto tradizionalmente testo e lunghezze di riga misurate usando funzioni di testo standard, ad esempio [**Text**](/windows/win32/api/wingdi/nf-wingdi-textouta)out, [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)e [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa). Queste funzioni supportano l'elaborazione di script complessi e di effetti tipografici accurati. Per ulteriori informazioni, vedere [tipi di carattere e testo](../gdi/fonts-and-text.md).

In generale, il supporto di testo standard è trasparente per le applicazioni che elaborano script complessi. Tuttavia, è necessario tenere presenti alcune regole specifiche da seguire per la scrittura di applicazioni che supportano la tipografia e l'elaborazione di script complessi:

-   L'applicazione deve salvare i caratteri in un buffer e visualizzare un'intera riga di testo in una sola volta anziché, ad esempio, chiamare [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) per ogni carattere così come viene digitato dall'utente. Questo meccanismo consente ai moduli avanzati di shaping del testo di usare il contesto per riordinare e generare correttamente i [glifi](uniscribe-glossary.md) .
-   L'applicazione deve usare [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) per determinare la lunghezza della riga, anziché calcolare le lunghezze di riga dalle larghezze dei caratteri memorizzati nella cache, perché la larghezza di un glifo può variare in base al contesto.
-   Facoltativamente, l'applicazione deve aggiungere il supporto per l'ordine di lettura da destra a sinistra e l'allineamento a destra.
-   Il riordino e l'elaborazione contestuale necessari per alfabeti complessi o per la tipografia fine richiedono un aumento significativo dell'elaborazione sulla visualizzazione di testo di base per gli script semplici. Pertanto, per evitare problemi di prestazioni, l'applicazione non deve elaborare grandi quantità di testo prima di visualizzare i risultati e restituire il controllo all'utente.

## <a name="complex-script-processing-using-edit-controls"></a>Elaborazione di script complessi mediante i controlli di modifica

I controlli di modifica standard di Windows sono stati estesi per supportare testo multilingue e script complessi. Il supporto esteso include l'input e la visualizzazione, nonché lo spostamento corretto del cursore sui cluster di caratteri, ad esempio negli script Thai e devangat. Per altre informazioni, vedere [modificare i controlli](../controls/edit-controls.md).

## <a name="complex-script-processing-using-rich-edit-controls"></a>Elaborazione di script complessi con controlli Rich Edit

Rich Edit 3,0 è una raccolta di interfacce di livello superiore che sfrutta i vantaggi di Uniscribe per isolare le applicazioni di layout del testo dalle complessità di determinati script. Rich Edit è il modo più semplice per le applicazioni di visualizzare script complessi anche se lo scopo principale non è necessariamente il layout del testo. Rich Edit offre una modifica rapida e versatile del testo multilingue Unicode RTF e del testo normale semplice. Sono incluse interfacce di messaggi e COM estese, modifica del testo, formattazione, interruzioni di riga, layout di tabella semplice, layout del testo verticale, layout del testo bidirezionale, supporto di lingue indiane e Thai, un'interfaccia utente di modifica simile a Microsoft Word e interfacce del modello a oggetti di testo.

Insieme alle interfacce Rich Edit, le applicazioni possono usare la funzione Rich Edit [**Text**](/windows/win32/api/wingdi/nf-wingdi-textouta) out per analizzare, modellare, posizionare e interrompere automaticamente le linee. Per ulteriori informazioni, vedere [controlli Rich Edit](../controls/rich-edit-controls.md).

## <a name="complex-script-processing-using-uniscribe"></a>Elaborazione di script complessi con Uniscribe

[Uniscribe](uniscribe.md) offre il supporto più completo per l'elaborazione di testo che interessa gli effetti tipografici e gli script complessi. Supporta le regole complesse presenti negli script, ad esempio arabo, devangal e Thai. Gestisce gli script scritti da destra a sinistra, come l'arabo e l'ebraico, e supporta la combinazione di script. Uniscribe espone anche le funzionalità dei tipi di carattere [OpenType](opentype-font-format.md) che possono essere utilizzate dalle applicazioni per controllare gli effetti tipografici. Per ulteriori informazioni, vedere [elaborazione di script complessi](processing-complex-scripts.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Uniscribe](about-uniscribe.md)
</dt> <dt>

[Elaborazione di script complessi](processing-complex-scripts.md)
</dt> </dl>

 

 
