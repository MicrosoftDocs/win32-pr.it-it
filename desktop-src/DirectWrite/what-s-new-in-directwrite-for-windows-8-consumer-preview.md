---
title: Novità di DirectWrite
description: Ecco alcune delle nuove aggiunte a DirectWrite.
ms.assetid: 2512D222-C6EB-4C2D-80A6-7978FED56F7A
ms.topic: article
ms.date: 09/23/2019
ms.openlocfilehash: 6b54a7f671ab6472ee2e412c2797d80bf7de245e
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349960"
---
# <a name="whats-new-in-directwrite"></a>Novità di DirectWrite

Questo argomento descrive le novità di [DirectWrite](direct-write-portal.md) per diverse versioni di Windows 10.

## <a name="project-reunion-01-prerelease"></a>Project Reunion 0.1 Versione preliminare

[Project Reunion](/windows/apps/project-reunion/) introduce una nuova versione di DirectWrite, denominata DWriteCore, che viene eseguita nelle versioni di Windows fino a Windows 8 e apre la porta per l'uso multipiattaforma. Per altre informazioni, vedere [Panoramica di DWriteCore.](dwritecore-overview.md)

## <a name="windows-10-may-2019-update"></a>Aggiornamento di Windows 10 di maggio 2019

Nessuna funzionalità o API è stata aggiunta né aggiornata per Windows 10 versione 1903 (10.0; Build 18362) &mdash; nota anche come Aggiornamento di Windows 10 (maggio 2019).

## <a name="windows-10-october-2018-update"></a>Aggiornamento di Windows 10 (ottobre 2018)

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10, versione 1809 (10.0; Build 17763) &mdash; nota anche come Aggiornamento di Windows 10 (ottobre 2018).

### <a name="new"></a>Nuova

- [**DWRITE_FONT_SOURCE_TYPE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type) enumerazione
- [**Interfaccia IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) e relativi metodi

## <a name="windows-10-april-2018-update"></a>Aggiornamento di Windows 10 (aprile 2018)

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10 versione 1803 (10.0; Build 17134) &mdash; nota anche come Aggiornamento di Windows 10 (aprile 2018).

### <a name="new"></a>Nuova

- [**Interfaccia IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) e relativi metodi
- [**Interfaccia IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) e relativi metodi
- [**Interfaccia IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) e relativi metodi

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10 versione 1709 (10.0; Build 16299) &mdash; nota anche come Windows 10 Fall Creators Update.

### <a name="new"></a>Nuova

- [**DWRITE_AUTOMATIC_FONT_AXES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes) enumerazione
- [**DWRITE_FONT_AXIS_ATTRIBUTES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes) enumerazione
- [**DWRITE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag) enumerazione
- [**DWRITE_FONT_FAMILY_MODEL**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model) enumerazione
- [**Interfaccia IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) e relativi metodi
- [**Interfaccia IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) e relativi metodi
- [**Interfaccia IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) e relativi metodi
- [**Interfaccia IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) e relativi metodi
- [**Interfaccia IDWriteFontFallback1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfallback1) e relativi metodi
- [**Interfaccia IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) e relativi metodi
- [**Interfaccia IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) e relativi metodi
- [**Interfaccia IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) e relativi metodi
- [**Interfaccia IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) e relativi metodi
- [**Interfaccia IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) e relativi metodi
- [**Interfaccia IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) e relativi metodi
- [**Interfaccia IDWriteTextLayout4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextlayout4) e relativi metodi
- [**DWRITE_MAKE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/nf-dwrite_3-dwrite_make_font_axis_tag) macro
- [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) struttura
- [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) struttura

### <a name="moved"></a>trasferito

L DWRITE_GLYPH_IMAGE_FORMATS enumere è stata spostata da a [](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) `dwrite_3.h` `dcommon.h` .

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10 versione 1703 (10.0; Build 15063) &mdash; nota anche come Windows 10 Creators Update.

### <a name="expanded-api-support-for-cloud-fonts-and-custom-font-sets"></a>Supporto api espanso per i tipi di carattere cloud e i set di caratteri personalizzati

Windows 10 api incluse che consentono alle app di accedere facilmente ai tipi di carattere da un servizio di caratteri di Windows. Nel Windows 10 Creators Update, le API per i tipi di carattere remoti vengono estese per consentire un facile accesso ai tipi di carattere da altre origini sul Web a cui è possibile accedere tramite HTTP o HTTPS. 

Le nuove API remote-font possono essere usate con servizi Web pubblici o privati. Possono inoltre essere usati per accedere ai file dei tipi di carattere OpenType non elaborati (con estensione ttf, otf., ttc, otc) o ai tipi di carattere in pacchetto nei formati contenitore [WOFF](https://www.w3.org/TR/WOFF/) o [WOFF2.](https://www.w3.org/TR/WOFF2/) Le nuove API vengono usate insieme alle API esistenti per l'accodamento delle richieste di download dei dati dei tipi di carattere remoti e per la gestione del processo di download effettivo.

Altre nuove API semplificano il funzionamento delle app con tipi di carattere personalizzati archiviati nel file system locale o caricati in un buffer di memoria.

Per altre informazioni sulle nuove API per l'uso di tipi di carattere remoti, set di caratteri personalizzati o formati contenitore WOFF/WOFF2, vedere l'argomento seguente:

[Set di caratteri personalizzati](custom-font-sets-win10.md)

Vedere anche i collegamenti agli argomenti di riferimento sulle API forniti in tale argomento.  L'uso di API nuove ed esistenti per l'uso di tipi di carattere personalizzati è illustrato anche nell'esempio [DirectWrite Custom Font Sets](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). Questo esempio illustra l'implementazione del codice per diversi scenari, tra cui tipi di carattere locali su disco, tipi di carattere remoti sul Web, dati dei tipi di carattere in memoria e tipi di carattere in formati WOFF o WOFF2 imballati.

### <a name="initial-support-for-opentype-font-variations"></a>Supporto iniziale per le varianti del tipo di carattere OpenType

La versione 1.8 della specifica del formato del tipo di carattere OpenType ha introdotto una nuova e interessante estensione per il formato noto come Variazioni del tipo di carattere OpenType. DirectWrite è stato aggiornato nel Windows 10 Creators Update per supportare istanze denominate di tipi di carattere variabili. Per altre informazioni, vedere l'argomento seguente:

[Tipi di carattere di variabili OpenType](opentype-variable-fonts.md)

## <a name="windows-10-anniversary-update"></a>Aggiornamento dell'anniversario di Windows 10

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10 versione 1607 (10.0; Build 14393) &mdash; nota anche come Aggiornamento dell'anniversario di Windows 10.

### <a name="improved-support-for-color-fonts"></a>Supporto migliorato per i tipi di carattere a colori

A partire da Aggiornamento dell'anniversario di Windows 10, DirectWrite offre il supporto predefinito per una più ampia gamma di formati di carattere a colori, consentendo agli sviluppatori di usare più tipi di carattere nelle app basate su DirectWrite che mai. È incluso il supporto di:

-   Tabella OpenType "COLR", che consente contenuto vettoriale compatto nei tipi di carattere. (Supportato da Windows 8.1.)
-   Tabella OpenType 'SVG', che abilita il contenuto SVG nei tipi di carattere.
-   Tabella OpenType "CBDT", che consente il contenuto bitmap a colori nei tipi di carattere.
-   Tabella OpenType "sbix", che consente il contenuto bitmap a colori nei tipi di carattere.

[Direct2D](../direct2d/direct2d-portal.md), che usa DirectWrite per il rendering del testo, supporta automaticamente questi formati di carattere a colori quando è abilitato il flag [**D2D1 \_ DRAW TEXT OPTIONS ENABLE COLOR \_ \_ \_ \_ \_ FONT.**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) Per altre informazioni, vedere i seguenti argomenti:

-   [Caratteri a colori](color-fonts.md)
-   [Esempio di glifo a colori DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="support-for-adobe-typekit-and-other-font-service-clients"></a>Supporto per Adobe Typekit e altri client del servizio di caratteri

Alcuni servizi di tipi di carattere, ad esempio Adobe Typekit, dispongono di utilità lato client che consentono a un utente di caricare i tipi di carattere dal servizio e usarli in applicazioni diverse nel computer Windows. Queste utilità in genere funzionano effettuando chiamate in fase di esecuzione a GDI per caricare tipi di carattere aggiuntivi, anziché installare in modo permanente i tipi di carattere nel sistema. A causa di tale progettazione, nelle versioni precedenti di Windows i tipi di carattere sarebbero utilizzabili nelle applicazioni basate su GDI, ma non nelle applicazioni DirectWrite. A partire dal Aggiornamento dell'anniversario di Windows 10, i tipi di carattere caricati da tali utilità saranno disponibili anche in DirectWrite e in GDI.

I tipi di carattere caricati da un'utilità del servizio di caratteri sono visibili nella raccolta di tipi di carattere di sistema ottenuta chiamando il [**metodo IDWriteFactory::GetSystemFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) Poiché i servizi dei tipi di carattere in genere seguono un modello di licenza per utente, i tipi di carattere caricati da queste utilità vengono gestiti in base all'utente. Di conseguenza, le applicazioni DirectWrite esistenti possono usare tipi di carattere ottenuti dagli utenti finali usando tali servizi, senza alcuna modifica del codice necessaria nell'applicazione, offrendo un'esperienza più semplice per gli utenti.

### <a name="support-for-opentype-collections-using-cff-outlines"></a>Supporto per raccolte OpenType con strutture CFF

I formati di carattere OpenType e TrueType supportano da tempo la possibilità di creare un pacchetto di più tipi di carattere in un singolo file di tipo di carattere, noto come "raccolta di tipi di carattere". La specifica OpenType ha sempre consentito ai tipi di carattere di usare i formati TrueType o CFF per i dati di struttura del glifo. Fino a poco tempo fa, tuttavia, la specifica è consentita solo per le raccolte in cui le strutture dei glifi usano il formato TrueType. OpenType versione 1.7 consente ora alle raccolte di usare i formati TrueType o CFF per i dati di struttura del glifo. A partire dal Aggiornamento dell'anniversario di Windows 10, DirectWrite supporterà le raccolte OpenType usando i dati di struttura CFF.

## <a name="windows-10"></a>Windows 10

### <a name="windows-font-service-integration"></a>Integrazione del servizio di tipi di carattere Windows

A partire Windows 10, i tipi di carattere inclusi in Windows sono disponibili in un servizio online e sono accessibili tramite DirectWrite in qualsiasi Windows 10 dispositivo. Questo vale per tutte le Windows 10, tra cui Windows 10 Mobile, Xbox e HoloLens, nonché per il client desktop. Ciò consente alle applicazioni di visualizzare il contenuto usando qualsiasi tipo di carattere di Windows anche se il tipo di carattere non è attualmente installato nel dispositivo.

Il supporto per i meccanismi del servizio di caratteri DirectWrite è stato implementato nel framework XAML, il che significa che tutte le applicazioni che usano XAML non richiedono modifiche al codice per sfruttare i vantaggi del servizio di tipi di carattere. [L'esempio di codice XAML (Downloadable Fonts)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/XamlCloudFontIntegration) illustra questa operazione. Le applicazioni che chiamano direttamente le API DirectWrite dovranno usare nuove API per usare i meccanismi del servizio di caratteri. Per altre informazioni, vedere i seguenti argomenti:

-   [**Metodo IDWriteFactory3::GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection)
-   [**Interfaccia IDWriteTextLayout3**](idwritetextlayout3.md)
-   [**Interfaccia IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue)
-   [**Interfaccia IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener)

[L'esempio di codice Downloadable Fonts (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont) illustra l'uso di diverse nuove API.

### <a name="font-set-apis"></a>API del set di caratteri

Le interfacce di raccolta dei tipi di carattere di DirectWrite forniscono una visualizzazione a una raccolta di tipi di carattere organizzati in base alle famiglie di caratteri, usando spessore, estensione e stile come attributi della famiglia secondaria. Internamente, DirectWrite implementa l'interfaccia di raccolta dei tipi di carattere usando un elenco semplice di tipi di carattere con vari attributi. Questo approccio è più flessibile in quanto può supportare l'enumerazione delle famiglie di spessore/estensione/stile, ma può anche supportare l'esecuzione di query e il filtro usando anche altri attributi del tipo di carattere.

In Windows 10, questo meccanismo di gestione dei caratteri più flessibile viene reso disponibile alle applicazioni tramite IDWriteFontSet e le API correlate. Le API del set di caratteri possono essere usate, ad esempio, per creare un'interfaccia utente di selezione dei caratteri personalizzata sfruttando le proprietà dei tipi di carattere personalizzate dell'applicazione in un set di caratteri personalizzato.

Per altre informazioni, vedere i seguenti argomenti:

-   [**Interfaccia IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   [**Interfaccia IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   [**DWRITE \_ Enumerazione \_ \_ DELL'ID PROPRIETÀ FONT**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id)
-   [**Metodo IDWriteFontFactory3::GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset)

### <a name="new-text-layout-line-spacing-modes"></a>Nuove modalità di spaziatura tra righe con layout di testo

Le interfacce di formattazione del testo e layout di testo di DirectWrite supportano nuove modalità di interlinea. Nelle versioni precedenti, l'implementazione del layout di testo di DirectWrite consentiva l'interlinea in cui l'altezza di ogni riga è stata impostata automaticamente in base all'elemento più alto all'interno di una riga (modalità "predefinita") o all'interlinea con tutte le righe impostate su un'altezza uniforme determinata dall'applicazione (modalità "uniforme"). In Windows 10 è supportata una modalità di interlinea "proporzionale" aggiuntiva che offre alle applicazioni più opzioni per il comportamento dell'interlinea. Per altre informazioni, vedere i seguenti argomenti:

-   [**Interfaccia IDWriteTextLayout3**](idwritetextlayout3.md)
-   [**Metodo IDWriteTextLayout3::SetLineSpacing**](idwritetextlayout3-setlinespacing.md)
-   [**DWRITE \_ Struttura LINE \_ SPACING**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)
-   [**DWRITE \_ Enumerazione LINE \_ SPACING \_ METHOD**](/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method)
-   [**DWRITE \_ Enumerazione FONT \_ LINE \_ GAP \_ USAGE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage)
-   [**Metodo IDWriteTextLayout3::GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)
-   [**DWRITE \_ Struttura LINE \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1)

L'esempio di codice [Interlinea (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteLineSpacingModes) illustra l'uso di diverse nuove API e offre anche una visualizzazione di tutte le diverse modalità di interlinea che semplificano la comprensione delle varie opzioni di interlinea disponibili.

### <a name="gdi-interop"></a>Interoperabilità GDI

Dalla sua introduzione in Windows 7, DirectWrite ha fornito un percorso di migrazione per le applicazioni originariamente implementate usando il modello di carattere, il layout del testo e il rendering di GDI. Questo è stato fornito tramite \[ \[ l'interfaccia IDWriteGdiInterop. \] \] In Windows 10, api aggiuntive forniscono funzionalità di interoperabilità GDI aggiuntive. Per altre informazioni, vedere l'argomento seguente:

-   [**Interfaccia IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1)

## <a name="windows-81"></a>Windows 8.1

### <a name="rendering-color-fonts"></a>Rendering dei tipi di carattere a colori

A partire da Windows Windows 8.1, DirectWrite fornisce il supporto per i tipi di carattere a colori. [Direct2D](../direct2d/direct2d-portal.md), che usa DirectWrite per il rendering del testo, ha aggiunto il valore di enumerazione D2D1 DRAW TEXT OPTIONS ENABLE COLOR FONT per abilitare questa funzionalità durante il disegno \_ \_ del \_ \_ \_ \_ testo. Per altre informazioni, vedere i seguenti argomenti:

-   [**D2D1 \_ Enumerazione DRAW \_ TEXT \_ OPTIONS**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options)
-   [**Metodo IDWriteFactory2::TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)

## <a name="windows-8"></a>Windows 8

Nuova interfaccia factory, [**IDWriteFactory1,**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)per la creazione di interfacce aggiuntive disponibili.

Proprietà del carattere aggiuntive, ad esempio: apice/pedice, pendenza del punto di caret, PANOSE e intervalli Unicode.

-   [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
-   [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)

Miglioramenti della spaziatura, ad esempio: spaziatura dei caratteri di controllo, coppie di crenatura legacy e giustificazione. Per altre [informazioni, vedere l'argomento Giustificazione, crenatura e](justification--kerning--and-spacing.md) spaziatura.

-   [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Destinazioni e parametri di rendering migliorati.

-   [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)
-   [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1)

Miglioramenti dell'analisi della complessità del testo.

-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Nuove proprietà dello script, nuovo supporto script (Unicode 6), aggiunte di fallback dei tipi di carattere, parentesi abbinate e aumento delle offerte.

Miglioramenti delle prestazioni della cache dei caratteri. A partire da Windows 8 la cache dei caratteri è globale e viene avviata all'avvio del computer.

Nuove modalità di rendering.

A partire Windows 8, [DirectWrite](direct-write-portal.md) supporta una serie di funzionalità che consentono di creare app per il mercato mondiale.

Ecco alcune aree che consentono di implementare app di testo rtf che possono essere personalizzate per i clienti di tutto il mondo.

### <a name="chinese-japanese-and-korean-extensions-c--d"></a>Estensioni in cinese, giapponese e coreano C & D

Ogni pochi anni, il consorzio Unicode rilascia un elenco standardizzato di aggiunte al blocco Ideografo unificato cinese, giapponese e coreano. Con la revisione Unicode 6.0, hanno rilasciato blocchi di estensione C e D. Questi blocchi di ideografi sono disponibili nel sito Web Unicode [Estensione C](https://www.unicode.org/charts/PDF/U2A700.pdf) ed [Estensione D](https://www.unicode.org/charts/PDF/U2B740.pdf).

A partire da Windows 8, [DirectWrite](direct-write-portal.md) supporta i punti di codice Unicode per questi nuovi blocchi di ideografi CJK standardizzati, in modo da poterli usare nelle app DirectWrite.

### <a name="indian-rupee-symbol"></a>Simbolo di rupia india

Nel marzo del 2005 il governo dell'India ha annunciato un concorso per scegliere un simbolo per la valuta della rupia indiana. Dopo molti concorsi, il 15 luglio 2010 il governo dell'India ha scelto il progetto creato da D. Udaya Kumar e [DirectWrite](direct-write-portal.md) include il supporto per il punto di codice Unicode associato al simbolo. Le app DirectWrite supportano quindi questo simbolo di valuta.

### <a name="emoji"></a>Emoji

[DirectWrite](direct-write-portal.md) supporta ora l'uso di emoji nelle app. Versioni precedenti di DirectWrite, presentate con una casella di glifo mancante se si tentava di eseguire il rendering di un ideogramma emoji. A partire da Windows 8, DirectWrite supporta il blocco di codice Unicode associato all'emoji, quindi se l'app usa i punti di codice standard Unicode per emoji, visualizza i glifi appropriati.

### <a name="myanmar-tiffinagh-and-old-hangul-languages"></a>Lingue Myanmar, Tiffinagh e Old Hangul

A partire da Windows 8, [DirectWrite](direct-write-portal.md) supporta il blocco di punti di codice Unicode che corrispondono ai glifi nelle lingue Myanmar, Tiffinagh e Hangul precedente, in modo da poter creare app che includono testo da queste tre lingue. Oltre a supportare questi caratteri, DirectWrite supporta il modo univoco in cui Old Hangul gestisce l'interruzione di riga.

### <a name="new-scripts"></a>Nuovi script

A partire Windows 8, il [**metodo GetScriptProperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties) restituisce informazioni per diversi nuovi script. Di seguito è riportato l'elenco di script supportati da [DirectWrite](direct-write-portal.md) Windows 8 e dopo.

-   Avestico
-   Bamum
-   Batak
-   Brahmi
-   Geroglifici egizi
-   Aramaico imperiale
-   Pahlavi discrizione
-   Partigiano discrizione
-   Giavanese
-   Kaithi
-   Lisu (Fraser)
-   Mandaic
-   Meetei Mayek
-   Arabo meridionale
-   Turco vecchio (Orkhon)
-   Samaritano
-   Tai Tham (Lanna)
-   Tai Viet
