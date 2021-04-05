---
title: Novità di DirectWrite
description: Di seguito sono riportate alcune delle nuove aggiunte a DirectWrite.
ms.assetid: 2512D222-C6EB-4C2D-80A6-7978FED56F7A
ms.topic: article
ms.date: 09/23/2019
ms.openlocfilehash: bf1a62917e18dcda7e7c4e3f1b05731b60628967
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2020
ms.locfileid: "103739687"
---
# <a name="whats-new-in-directwrite"></a>Novità di DirectWrite

Questo argomento descrive le novità di [DirectWrite](direct-write-portal.md) per le varie versioni di Windows 10.

## <a name="project-reunion-01-prerelease"></a>Progetto Reunion 0,1 versione preliminare

[Progetto Reunion](/windows/apps/project-reunion/) introduce una nuova versione di DirectWrite, denominata DWriteCore, che viene eseguita nelle versioni di Windows fino a Windows 8 e apre la porta per l'uso multipiattaforma. Per altri dettagli, vedere [Panoramica di DWriteCore](dwritecore-overview.md).

## <a name="windows-10-may-2019-update"></a>Aggiornamento di Windows 10 di maggio 2019

Non sono state aggiunte funzionalità né API né aggiornate per Windows 10, versione 1903 (10,0; Build 18362) &mdash; Nota anche come Windows 10 May 2019 Update.

## <a name="windows-10-october-2018-update"></a>Aggiornamento di Windows 10 (ottobre 2018)

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10, versione 1809 (10,0; Build 17763) &mdash; Nota anche come aggiornamento di Windows 10 ottobre 2018.

### <a name="new"></a>Nuova

- Enumerazione [**DWRITE_FONT_SOURCE_TYPE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type)
- Interfaccia [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) e relativi metodi

## <a name="windows-10-april-2018-update"></a>Aggiornamento di Windows 10 (aprile 2018)

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10, versione 1803 (10,0; Build 17134) &mdash; Nota anche come aggiornamento di Windows 10 aprile 2018.

### <a name="new"></a>Nuova

- Interfaccia [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) e relativi metodi
- Interfaccia [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) e relativi metodi
- Interfaccia [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) e relativi metodi

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10, versione 1709 (10,0; Build 16299) &mdash; Nota anche come Windows 10 Fall Creators Update.

### <a name="new"></a>Nuova

- Enumerazione [**DWRITE_AUTOMATIC_FONT_AXES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes)
- Enumerazione [**DWRITE_FONT_AXIS_ATTRIBUTES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes)
- Enumerazione [**DWRITE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag)
- Enumerazione [**DWRITE_FONT_FAMILY_MODEL**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model)
- Interfaccia [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) e relativi metodi
- Interfaccia [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) e relativi metodi
- Interfaccia [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) e relativi metodi
- Interfaccia [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) e relativi metodi
- Interfaccia [**IDWriteFontFallback1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfallback1) e relativi metodi
- Interfaccia [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) e relativi metodi
- Interfaccia [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) e relativi metodi
- Interfaccia [**IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) e relativi metodi
- Interfaccia [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) e relativi metodi
- Interfaccia [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) e relativi metodi
- Interfaccia [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) e relativi metodi
- Interfaccia [**IDWriteTextLayout4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextlayout4) e relativi metodi
- [**DWRITE_MAKE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/nf-dwrite_3-dwrite_make_font_axis_tag) macro
- Struttura [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)
- Struttura [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value)

### <a name="moved"></a>Spostato

Enumerazione [**DWRITE_GLYPH_IMAGE_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) spostata da `dwrite_3.h` a `dcommon.h` .

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10, versione 1703 (10,0; Build 15063) &mdash; Nota anche come Windows 10 Creators Update.

### <a name="expanded-api-support-for-cloud-fonts-and-custom-font-sets"></a>Supporto delle API espanse per i tipi di carattere cloud e set di caratteri personalizzati

Windows 10 includeva API che consentono alle app di accedere facilmente ai tipi di carattere da un servizio Windows. In Windows 10 Creators Update, le API per i tipi di carattere remoti vengono estese per consentire un facile accesso ai tipi di carattere da altre origini sul Web a cui è possibile accedere tramite HTTP o HTTPS. 

Le nuove API dei tipi di carattere remote possono essere utilizzate con servizi Web pubblici o privati. Inoltre, possono essere usati per accedere a file di tipi di carattere OpenType non elaborati (con estensione ttf, OTF., TTC, OTC) o a tipi di carattere inclusi nei formati di contenitore [WOFF](https://www.w3.org/TR/WOFF/) o [WOFF2](https://www.w3.org/TR/WOFF2/) . Le nuove API vengono usate insieme alle API esistenti per accodare le richieste per scaricare i dati del tipo di carattere remoto e per gestire il processo di download effettivo.

Altre nuove API semplificano l'utilizzo delle app con i tipi di carattere personalizzati archiviati nel file system locale o caricati in un buffer di memoria.

Per ulteriori informazioni sulle nuove API per l'utilizzo di tipi di carattere remoti, set di caratteri personalizzati o formati di contenitore WOFF/WOFF2, vedere l'argomento seguente:

[Set di caratteri personalizzati](custom-font-sets-win10.md)

Vedere anche i collegamenti agli argomenti di riferimento per le API disponibili in questo argomento.  L'uso di API nuove ed esistenti per l'utilizzo di tipi di carattere personalizzati è illustrato anche nell' [esempio di set di caratteri personalizzati DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). In questo esempio viene illustrata l'implementazione del codice per diversi scenari, inclusi i tipi di carattere locali su disco, i tipi di carattere remoti sul Web, i dati di tipo carattere in memoria e i tipi di carattere nei formati WOFF o WOFF2 compressi.

### <a name="initial-support-for-opentype-font-variations"></a>Supporto iniziale per le variazioni dei tipi di carattere OpenType

La versione 1,8 della specifica del formato del tipo di carattere OpenType ha introdotto un'interessante nuova estensione nel formato noto come variazioni dei tipi di carattere OpenType. DirectWrite è stato aggiornato in Windows 10 Creators Update per supportare le istanze denominate di tipi di carattere variabili. Per altre informazioni, vedere l'argomento seguente:

[Tipi di carattere di variabili OpenType](opentype-variable-fonts.md)

## <a name="windows-10-anniversary-update"></a>Aggiornamento dell'anniversario di Windows 10

Le funzionalità e le API seguenti sono state aggiunte o aggiornate per Windows 10, versione 1607 (10,0; Build 14393) &mdash; Nota anche come aggiornamento dell'anniversario di Windows 10.

### <a name="improved-support-for-color-fonts"></a>Supporto migliorato per i tipi di carattere a colori

A partire dall'aggiornamento dell'anniversario di Windows 10, DirectWrite offre supporto incorporato per una varietà più ampia di formati di tipi di carattere colori, consentendo agli sviluppatori di usare più tipi di caratteri nelle app basate su DirectWrite che mai. È incluso il supporto di:

-   Tabella OpenType ' COLR ', che consente il contenuto di un vettore compatto nei tipi di carattere. (Supportato da Windows 8.1.)
-   Tabella OpenType ' SVG ', che consente il contenuto SVG nei tipi di carattere.
-   Tabella OpenType ' CBDT ', che consente il contenuto della bitmap di colore nei tipi di carattere.
-   Tabella OpenType ' sbix ', che consente il contenuto della bitmap di colore nei tipi di carattere.

[Direct2D](../direct2d/direct2d-portal.md), che usa DirectWrite per il rendering del testo, supporta automaticamente questi formati dei tipi di carattere colore quando il flag d2d1 per il [**\_ \_ testo \_ \_ \_ \_**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) è abilitato. Per altre informazioni, vedere i seguenti argomenti:

-   [Caratteri a colori](color-fonts.md)
-   [Esempio di glifo colori DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="support-for-adobe-typekit-and-other-font-service-clients"></a>Supporto per Adobe Typekit e altri client del servizio del tipo di carattere

Alcuni servizi per i tipi di carattere, ad esempio Adobe Typekit, dispongono di utilità lato client che consentono a un utente di caricare i tipi di carattere dal servizio e di usarli in applicazioni diverse sul proprio computer Windows. Queste utilità in genere funzionano effettuando chiamate in fase di esecuzione a GDI per caricare tipi di carattere aggiuntivi, anziché installare in modo permanente i tipi di carattere nel sistema. A causa di tale progettazione, nelle versioni precedenti di Windows, i tipi di carattere sarebbero utilizzabili nelle applicazioni basate su GDI, ma non nelle applicazioni DirectWrite. A partire dall'aggiornamento dell'anniversario di Windows 10, i tipi di carattere caricati da tali utilità saranno disponibili anche in DirectWrite e in GDI.

I tipi di carattere caricati da un'utilità di servizio del tipo di carattere sono visibili nella raccolta di tipi di carattere del sistema ottenuta chiamando il metodo [**IDWriteFactory archiviata nei:: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Poiché i servizi dei tipi di carattere seguono in genere un modello di gestione delle licenze per utente, i tipi di carattere caricati da queste utilità vengono gestiti in base ai singoli utenti. Di conseguenza, le applicazioni DirectWrite esistenti possono utilizzare i tipi di carattere ottenuti dagli utenti finali utilizzando tali servizi, senza apportare modifiche al codice nell'applicazione, offrendo un'esperienza più trasparente per gli utenti.

### <a name="support-for-opentype-collections-using-cff-outlines"></a>Supporto per le raccolte OpenType con le strutture CFF

I formati dei tipi di carattere OpenType e TrueType sono supportati a lungo per consentire l'inclusione di più tipi di carattere in un unico file del tipo di carattere, noto come "raccolta di tipi di carattere". La specifica OpenType ha sempre consentito ai tipi di carattere di usare formati TrueType o CFF per i dati della struttura del glifo. Fino a poco tempo fa, tuttavia, la specifica è consentita solo per le raccolte in cui le strutture dei glifi utilizzano il formato TrueType. La versione 1,7 di OpenType consente ora alle raccolte di usare formati TrueType o CFF per i dati della struttura del glifo. A partire dall'aggiornamento dell'anniversario di Windows 10, DirectWrite supporterà le raccolte OpenType usando i dati della struttura CFF.

## <a name="windows-10"></a>Windows 10

### <a name="windows-font-service-integration"></a>Integrazione del servizio font Windows

A partire da Windows 10, i tipi di carattere inclusi in Windows sono disponibili in un servizio online e sono accessibili tramite DirectWrite su qualsiasi dispositivo Windows 10. Si applica a tutte le edizioni di Windows 10, tra cui Windows 10 Mobile, Xbox e HoloLens, nonché il client desktop. Questo consente alle applicazioni di visualizzare il contenuto usando qualsiasi tipo di carattere di Windows anche se il tipo di carattere non è attualmente installato nel dispositivo.

Il supporto per i meccanismi di servizio del tipo di carattere DirectWrite è stato implementato nel framework XAML, il che significa che tutte le applicazioni che usano XAML non richiedono modifiche al codice per sfruttare il servizio del tipo di carattere. L' [esempio di codice per i tipi di carattere scaricabile (XAML)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/XamlCloudFontIntegration) illustra questa operazione. Le applicazioni che chiamano direttamente le API DirectWrite dovranno usare le nuove API per usare i meccanismi del servizio del tipo di carattere. Per altre informazioni, vedere i seguenti argomenti:

-   Metodo [**IDWriteFactory3:: GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection)
-   Interfaccia [**IDWriteTextLayout3**](idwritetextlayout3.md)
-   Interfaccia [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue)
-   Interfaccia [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener)

L' [esempio di codice dei tipi di carattere scaricabili (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont) illustra l'uso di molte delle nuove API.

### <a name="font-set-apis"></a>API dei set di caratteri

Le interfacce di raccolta dei tipi di carattere di DirectWrite forniscono una visualizzazione a una raccolta di tipi di carattere organizzati in base a famiglie di caratteri, usando il peso, l'estensione e lo stile come attributi secondari. Internamente, DirectWrite implementa l'interfaccia della raccolta di tipi di carattere usando un elenco semplice di tipi di carattere con diversi attributi. Questo approccio è più flessibile in quanto in può supportare l'enumerazione di famiglie di peso/stretch/stile, ma può supportare anche l'esecuzione di query e il filtro usando altri attributi del tipo di carattere.

In Windows 10 questo meccanismo di gestione dei tipi di carattere più flessibile viene reso disponibile per le applicazioni tramite IDWriteFontSet e le API correlate. È possibile usare le API del set di caratteri, ad esempio, per creare un'interfaccia utente personalizzata per la selezione dei tipi di carattere usando le proprietà dei tipi di carattere personalizzate dell'applicazione in un set di caratteri personalizzato.

Per altre informazioni, vedere i seguenti argomenti:

-   Interfaccia [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   Interfaccia [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   [**DWrite \_ Enumerazione \_ \_ ID proprietà carattere**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id)
-   Metodo [**IDWriteFontFactory3:: GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset)

### <a name="new-text-layout-line-spacing-modes"></a>Nuove modalità di spaziatura delle righe di layout di testo

Il formato del testo e le interfacce del layout del testo di DirectWrite supportano le nuove modalità di spaziatura riga. Nelle versioni precedenti, l'implementazione del layout del testo di DirectWrite è consentita per l'interlinea in cui l'altezza di ogni riga è stata impostata automaticamente in base all'elemento più alto all'interno di una riga (modalità "predefinita") o all'interlinea con tutte le righe impostate su un'altezza uniforme determinata dall'applicazione (modalità "uniforme"). In Windows 10 è supportata una modalità di spaziatura riga "proporzionale" aggiuntiva che offre alle applicazioni più opzioni per il comportamento di spaziatura riga. Per altre informazioni, vedere i seguenti argomenti:

-   Interfaccia [**IDWriteTextLayout3**](idwritetextlayout3.md)
-   Metodo [**IDWriteTextLayout3:: SetLineSpacing**](idwritetextlayout3-setlinespacing.md)
-   [**DWrite \_ Struttura di \_ spaziatura riga**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)
-   [**DWrite \_ Enumerazione \_ del \_ metodo di SPAZIatura riga**](/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method)
-   [**DWrite \_ Enumerazione \_ \_ \_ utilizzo Gap riga carattere**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage)
-   Metodo [**IDWriteTextLayout3:: GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)
-   [**DWrite \_ Struttura \_ METRICS1 linea**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1)

L' [esempio di codice di interlinea (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteLineSpacingModes) illustra l'uso di molte delle nuove API e fornisce anche una visualizzazione di tutte le diverse modalità di spaziatura riga che rendono più semplice comprendere le varie opzioni di spaziatura riga disponibili.

### <a name="gdi-interop"></a>Interoperabilità GDI

Fin dalla sua introduzione in Windows 7, DirectWrite ha fornito un percorso di migrazione per le applicazioni originariamente implementate usando il modello di tipo di carattere di GDI, il layout del testo e il rendering. Questo è stato fornito tramite l' \[ \[ \] \] interfaccia IDWriteGdiInterop. In Windows 10, le API aggiuntive offrono funzionalità aggiuntive di interoperabilità GDI. Per ulteriori informazioni, vedere l'argomento seguente:

-   Interfaccia [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1)

## <a name="windows-81"></a>Windows 8.1

### <a name="rendering-color-fonts"></a>Tipi di carattere colore rendering

A partire da Windows Windows 8.1, DirectWrite fornisce supporto per i tipi di carattere a colori. [Direct2D](../direct2d/direct2d-portal.md), che usa DirectWrite per il rendering del testo, ha aggiunto il valore enum d2d1 \_ Draw \_ Text \_ Options \_ Abilita il \_ \_ tipo di carattere colore per abilitare questa funzionalità durante il disegno del testo. Per altre informazioni, vedere i seguenti argomenti:

-   [**D2d1 \_ Enumerazione \_ delle \_ Opzioni di testo di estrazione**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options)
-   Metodo [**IDWriteFactory2:: TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)

## <a name="windows-8"></a>Windows 8

Nuova interfaccia Factory, [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1), per la creazione di interfacce aggiuntive disponibili.

Proprietà del tipo di carattere aggiuntive, ad esempio: Super/Indice, inclinazione del cursore, PANOse e intervalli Unicode.

-   [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
-   [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)

Miglioramenti della spaziatura, ad esempio la spaziatura del carattere di controllo, le coppie di crenatura legacy e la giustificazione. Per altre informazioni, vedere l'argomento [giustificazione, crenatura e spaziatura](justification--kerning--and-spacing.md) .

-   [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Miglioramento di destinazioni e parametri di rendering.

-   [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)
-   [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1)

Miglioramenti dell'analisi della complessità del testo.

-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Nuove proprietà dello script, nuovo supporto per gli script (Unicode 6), aggiunte di fallback dei tipi di carattere, parentesi abbinate e incremento di bidi.

Miglioramenti delle prestazioni della cache dei tipi di carattere. A partire da Windows 8, la cache dei tipi di carattere è globale e viene avviata all'avvio del computer.

Nuove modalità di rendering.

A partire da Windows 8, [DirectWrite](direct-write-portal.md) supporta una serie di funzionalità che consentono di creare app per il mercato mondiale.

Di seguito sono riportate diverse aree che consentono di implementare app di testo RTF che possono essere personalizzate per i clienti in tutto il mondo.

### <a name="chinese-japanese-and-korean-extensions-c--d"></a>Estensioni cinese, giapponese e coreano C & D

A intervalli di anni, il Consorzio Unicode rilascia un elenco standardizzato di aggiunte al blocco di ideogrammi unificato cinese, giapponese e coreano. Con la revisione Unicode 6,0, i blocchi di estensione C e D sono stati rilasciati. Questi blocchi di ideogrammi si trovano nell'estensione del sito Web Unicode [C](https://www.unicode.org/charts/PDF/U2A700.pdf) ed [estensione D](https://www.unicode.org/charts/PDF/U2B740.pdf).

A partire da Windows 8, [DirectWrite](direct-write-portal.md) supporta i punti di riferimento Unicode per questi nuovi blocchi di ideogrammi CJK standardizzati, in modo che sia possibile usarli nelle app DirectWrite.

### <a name="indian-rupee-symbol"></a>Simbolo Rupee indiano

Nel marzo del 2005 il governo indiano ha annunciato un concorso per scegliere un simbolo per la valuta della rupia indiana. Dopo la maggior parte della concorrenza, il 15 luglio 2010, il governo indiano ha scelto il progetto creato da D. Udaya Kumar e [DirectWrite](direct-write-portal.md) include il supporto per il punto di riferimento Unicode associato al simbolo. Quindi, le app DirectWrite supportano ora questo simbolo di valuta.

### <a name="emoji"></a>Emoji

[DirectWrite](direct-write-portal.md) supporta ora l'uso di emoji nelle app. Nelle versioni precedenti di DirectWrite, viene visualizzata una casella di glifo mancante se si è tentato di eseguire il rendering di un ideogramma emoji. A partire da Windows 8, DirectWrite supporta il CodeBlock Unicode associato a emoji, quindi se l'app usa i punti di codifica Unicode standard per emoji, Visualizza i glifi appropriati.

### <a name="myanmar-tiffinagh-and-old-hangul-languages"></a>Myanmar, Tiffinagh e lingue hangul precedenti

A partire da Windows 8, [DirectWrite](direct-write-portal.md) supporta il blocco di punti di codifica Unicode che corrispondono ai glifi nei linguaggi di Myanmar, Tiffinagh e hangul precedenti, quindi è possibile creare app che includono testo da queste tre lingue. Oltre a supportare questi caratteri, DirectWrite supporta il modo univoco in cui l'Hangul precedente gestisce le interruzioni di riga.

### <a name="new-scripts"></a>Nuovi script

A partire da Windows 8, il metodo [**GetScriptProperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties) restituisce informazioni per un numero di nuovi script. Di seguito è riportato l'elenco di script supportati da [DirectWrite](direct-write-portal.md) in Windows 8 e successive.

-   Avestico
-   Bamum
-   Batak
-   Brahmi
-   Geroglifici egiziani
-   Aramaico imperiale
-   Pahlavi iscrizione
-   Partial iscrizione
-   Giavanese
-   Kaithi
-   Lisu (Fraser)
-   Mandaico
-   Dei Meetei
-   Vecchio sud arabo
-   Vecchio turco (Orkhon)
-   Samaritano
-   Tai Tham (Lanna)
-   Tai Viet