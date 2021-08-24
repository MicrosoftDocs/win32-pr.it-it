---
description: "Di seguito sono riportate le opzioni per la visualizzazione e l'elaborazione correlata del testo per supportare effetti tipografici fine o script complessi: Funzioni di testoModifica controlliRichiedi controlli di modificaScrivi"
ms.assetid: 337bc798-e75d-4389-8fea-577eb82a0ed5
title: Elaborazione di script complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15671aed99e0c596d83bd65a2f4a0925ff61293cf90ed37e2aed371f23f114fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754911"
---
# <a name="complex-script-processing"></a>Elaborazione di script complessi

Di seguito sono riportate le opzioni per la visualizzazione e l'elaborazione correlata del testo per supportare effetti tipografici o script complessi:

-   Funzioni di testo
-   Controlli di modifica
-   Controlli Rich Edit
-   Uniscribe

Le opzioni selezionate dipendono dai fattori seguenti:

-   Tipo di testo o script.
-   Modello di implementazione, ad esempio il layout del testo e la gestione dell'interruzione di riga da parte dell'applicazione.
-   Aggiornamento di un'applicazione esistente rispetto alla creazione di una nuova applicazione.

In generale, un'applicazione che esegue un'elaborazione di script relativamente semplice può scegliere qualsiasi opzione per l'elaborazione di script complessi. Tuttavia, per il controllo più completo dell'elaborazione di script complessi, è consigliabile scegliere Uniscribe.

## <a name="complex-script-processing-using-text-functions"></a>Elaborazione di script complessi tramite funzioni di testo

Le applicazioni che usano principalmente testo normale, ad esempio testo che usa lo stesso carattere tipografico, spessore, colore e così via, hanno in genere scritto testo e lunghezze di riga misurate usando funzioni di testo standard, ad esempio [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)e [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa). Queste funzioni supportano l'elaborazione di script complessi ed effetti tipografici fine. Per altre informazioni, vedere [Tipi di carattere e testo.](../gdi/fonts-and-text.md)

In generale, il supporto del testo standard è trasparente per le applicazioni che elaborano script complessi. È tuttavia necessario tenere presenti alcune regole specifiche da seguire per la scrittura di applicazioni che supportano la tipografia fine ed elaborano script complessi:

-   L'applicazione deve salvare i caratteri in un buffer e visualizzare un'intera riga di testo contemporaneamente anziché, ad esempio, chiamare [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) su ogni carattere digitato dall'utente. Questo meccanismo consente ai moduli avanzati di data shaping del testo di usare il contesto per riordinare e generare [correttamente i glifi.](uniscribe-glossary.md)
-   L'applicazione deve usare [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) per determinare la lunghezza della riga, invece di calcolare le lunghezze di riga dalle larghezze dei caratteri memorizzate nella cache, poiché la larghezza di un glifo può variare in base al contesto.
-   L'applicazione deve facoltativamente aggiungere il supporto per l'ordine di lettura da destra a sinistra e l'allineamento a destra.
-   Il riordinamento e l'elaborazione contestuale necessari per script complessi o tipografia fine richiedono un aumento significativo dell'elaborazione rispetto alla visualizzazione di testo di base per script semplici. Pertanto, per evitare problemi di prestazioni, l'applicazione non deve elaborare grandi quantità di testo prima di visualizzare i risultati e restituire il controllo all'utente.

## <a name="complex-script-processing-using-edit-controls"></a>Elaborazione di script complessi tramite controlli di modifica

I controlli Windows di modifica standard sono stati estesi per supportare testo multilingue e script complessi. Il supporto esteso include l'input e la visualizzazione, nonché il corretto spostamento del cursore sui cluster di caratteri, ad esempio negli script thai e Devanagari. Per altre informazioni, vedere [Edit Controls](../controls/edit-controls.md).

## <a name="complex-script-processing-using-rich-edit-controls"></a>Elaborazione di script complessi tramite controlli Rich Edit

Rich Edit 3.0 è una raccolta di interfacce di livello superiore che sfrutta Uniscribe per isolare le applicazioni di layout di testo dalle complessità di determinati script. Rich Edit è il modo più semplice per le applicazioni di visualizzare script complessi anche se lo scopo principale non è necessariamente il layout di testo. Rich Edit offre una modifica rapida e versatile del testo multilingue Unicode e del testo normale semplice. Include interfacce COM e messaggi estese, modifica del testo, formattazione, interruzione di riga, layout di tabella semplice, layout di testo verticale, layout di testo bidirezionale, supporto indic e thai, un'interfaccia utente di modifica molto simile a Microsoft Word e le interfacce del modello a oggetti di testo.

Insieme alle interfacce Rich Edit, le applicazioni possono usare la funzione [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta) Rich Edit per analizzare, modellare, posizionare e interrompere automaticamente le righe. Per altre informazioni, vedere [Controlli Rich Edit.](../controls/rich-edit-controls.md)

## <a name="complex-script-processing-using-uniscribe"></a>Elaborazione di script complessi tramite Uniscribe

[Uniscribe offre](uniscribe.md) il supporto più completo per l'elaborazione di testo che include effetti tipografici fine e script complessi. Supporta le regole complesse presenti negli script, ad esempio arabo, Devanagari e Thai. Gestisce gli script scritti da destra a sinistra, ad esempio arabo ed ebraico, e supporta la combinazione di script. Uniscribe espone anche le funzionalità dei tipi di carattere [OpenType](opentype-font-format.md) che possono essere usate dalle applicazioni per controllare gli effetti tipografici fine. Per altre informazioni, vedere [Elaborazione di script complessi.](processing-complex-scripts.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Uniscribe](about-uniscribe.md)
</dt> <dt>

[Elaborazione di script complessi](processing-complex-scripts.md)
</dt> </dl>

 

 
