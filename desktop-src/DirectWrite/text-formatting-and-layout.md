---
title: Formattazione e layout del testo
description: DirectWrite fornisce due interfacce per la formattazione del testo IDWriteTextFormat e IDWriteTextLayout.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite,formattazione del testo
- DirectWrite,layout
- DirectWrite,INTERFACCIA IDWriteTextFormat
- DirectWrite,INTERFACCIA IDWriteTextLayout
- Interfaccia IDWriteTextFormat
- Interfaccia IDWriteTextLayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e67b4c59a7e8ba47a2811021b54ebe1e5b8867b30d07e143163c3d03ac3cdf22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329351"
---
# <a name="text-formatting-and-layout"></a>Formattazione e layout del testo

[DirectWrite](direct-write-portal.md) fornisce due interfacce per la formattazione del testo: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). **IDWriteTextFormat** descrive solo il formato per il testo e viene usato nei casi in cui un'intera stringa deve avere le stesse dimensioni, lo stesso stile, lo stesso spessore e così via. D'altra parte, **IDWriteTextLayout** incapsula sia una stringa di testo che la formattazione per gli intervalli specificati della stringa. Questo documento descrive ogni interfaccia e i relativi utilizzi. Per altre informazioni sulla creazione e sui metodi di queste interfacce, vedere le pagine di riferimento [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

Questo documento contiene le parti seguenti:

-   [IDWriteTextFormat](#modifying-an-idwritetextformat)
    -   [Modifica di un oggetto IDWriteTextFormat](#modifying-an-idwritetextformat)
-   [IDWriteTextLayout](#idwritetextlayout)
    -   [Formattazione di un intervallo di testo](#formatting-a-range-of-text)
    -   [Opzioni di rendering](#rendering-options)

## <a name="idwritetextformat"></a>IDWriteTextFormat

Un [**oggetto IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) viene usato per:

-   Descrivere il formato di un'intera stringa durante il rendering. Per eseguire il rendering di una stringa con più formati, usare un [**oggetto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
-   Specificare il formato di testo predefinito quando si crea un [**oggetto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

Per creare un [**oggetto IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) usare il metodo [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) e specificare la famiglia di caratteri, la raccolta di caratteri, lo spessore del carattere, le dimensioni del carattere (in DIP), il nome delle impostazioni locali.

### <a name="modifying-an-idwritetextformat"></a>Modifica di un oggetto IDWriteTextFormat

Dopo aver [**creato un'interfaccia IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) alcuni valori non possono essere modificati: la famiglia di caratteri, la raccolta, il peso e le dimensioni, nonché il nome delle impostazioni locali. Per modificare questi valori, è necessario creare un nuovo **oggetto IDWriteTextFormat.**

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) consente di modificare le proprietà precedenti senza ricreare alcun elemento. [**IDWriteTextFormat consente**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) di apportare modifiche al formato che si applicano all'intero testo, ad esempio l'allineamento del testo. Se si vuole applicare la formattazione a intervalli di caratteri specifici, è consigliabile usare **idWriteTextLayout**.

[**IDWriteTextFormat fornisce**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) metodi per impostare l'allineamento del testo, la direzione del flusso, la tabulazione incrementale, l'interlinea, l'allineamento del paragrafo, il trimming e il ritorno a capo automatico. Queste proprietà possono essere modificate in qualsiasi momento dopo la creazione **dell'oggetto IDWriteTextFormat.**

## <a name="idwritetextlayout"></a>IDWriteTextLayout

[**L'interfaccia IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) a differenza [**di IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), rappresenta sia un blocco di testo che la formattazione associata. **IDWriteTextFormat rappresenta le** informazioni di formattazione iniziali. L'esempio seguente illustra come creare un **oggetto IDWriteTextLayout** usando [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).


```C++
// Create a text layout using the text format.
if (SUCCEEDED(hr))
{
    RECT rect;
    GetClientRect(hwnd_, &rect); 
    float width  = rect.right  / dpiScaleX_;
    float height = rect.bottom / dpiScaleY_;

    hr = pDWriteFactory_->CreateTextLayout(
        wszText_,      // The string to be laid out and formatted.
        cTextLength_,  // The length of the string.
        pTextFormat_,  // The text format to apply to the string (contains font information, etc).
        width,         // The width of the layout box.
        height,        // The height of the layout box.
        &pTextLayout_  // The IDWriteTextLayout interface pointer.
        );
}

```



Il testo in un [**oggetto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) non può essere modificato dopo la creazione dell'oggetto. Per modificare il testo, è necessario eliminare l'oggetto esistente e creare un nuovo **oggetto IDWriteTextLayout.**

È possibile usare [**idWriteTextLayout per**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) formattare intervalli di testo specificati. **IDWriteTextLayout fornisce anche** metodi per modificare lo stile e lo spessore del carattere e aggiungere funzionalità del tipo di carattere OpenType e hit testing. Per altre informazioni e un elenco completo dei metodi, vedere la pagina di riferimento [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

### <a name="formatting-a-range-of-text"></a>Formattazione di un intervallo di testo

[**IDWriteTextLayout fornisce**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) diversi metodi per formattare intervalli di testo. Ognuno di questi metodi accetta una [**struttura DWRITE \_ TEXT \_ RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) come parametro per specificare la posizione iniziale del testo all'interno della stringa e la lunghezza dell'intervallo da formattare. Nell'esempio seguente viene illustrato come impostare lo spessore del carattere di un intervallo di testo su grassetto.


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a>Opzioni di rendering

Il rendering del testo con formattazione descritta solo da un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) può essere eseguito con [Direct2D,](../direct2d/direct2d-portal.md)tuttavia sono disponibili altre opzioni per il rendering di un [**oggetto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

È possibile eseguire il rendering della stringa descritta da un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando i metodi seguenti.

1.  [Eseguire il rendering con Direct2D.](rendering-by-using-direct2d.md)
2.  [Eseguire il rendering usando un renderer di testo personalizzato.](how-to-implement-a-custom-text-renderer.md)
3.  [Eseguire il rendering su una superficie GDI.](render-to-a-gdi-surface.md)

 

 
