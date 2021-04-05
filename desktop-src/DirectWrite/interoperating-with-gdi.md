---
title: Interoperabilità con GDI
description: DirectWrite fornisce un percorso di migrazione da e alcune interoperabilità con il modello del tipo di carattere di GDI, oltre a interfacce per il rendering del testo in una bitmap che può essere disegnata in una finestra.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- DirectWrite, interoperatività GDI
- DirectWrite, interoperabilità
- interoperabilità
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046786"
---
# <a name="interoperating-with-gdi"></a>Interoperabilità con GDI

[DirectWrite](direct-write-portal.md) fornisce un percorso di migrazione da e alcune interoperabilità con il modello del tipo di carattere di GDI, oltre a interfacce per il rendering del testo in una bitmap che può essere disegnata in una finestra.

Questa panoramica include le parti seguenti:

-   [Introduzione](#introduction)
-   [Parte 1: IDWriteGdiInterop](#part-1-idwritegdiinterop)
-   [Parte 2: oggetti Font](#part-2-font-objects)
-   [Parte 3: rendering](#part-3-rendering)

## <a name="introduction"></a>Introduzione

[DirectWrite](direct-write-portal.md) fornisce metodi per la conversione tra la struttura LOGFONT di GDI e le interfacce del tipo di carattere DirectWrite. In questo modo è possibile utilizzare GDI per alcune o tutte le enumerazioni e la selezione dei tipi di carattere, sfruttando al contempo le funzionalità e le prestazioni migliorate di DirectWrite. DirectWrite dispone inoltre di interfacce per il rendering in una bitmap se si desidera visualizzare il testo su una superficie GDI.

## <a name="part-1-idwritegdiinterop"></a>Parte 1: IDWriteGdiInterop

L'interfaccia [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) viene utilizzata per eseguire la conversione tra le strutture del tipo di carattere GDI e le interfacce del tipo di carattere [DirectWrite](direct-write-portal.md) e per creare un oggetto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) . Ottenere un oggetto **IDWriteGdiInterop** usando il metodo [**IDWriteFactory archiviata nei:: GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) , come illustrato nel codice seguente.


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a>Parte 2: oggetti Font

GDI utilizza la struttura LOGFONT per archiviare le informazioni sul tipo di carattere e lo stile del testo. Il metodo [**IDWriteGdiInterop:: CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) converte una struttura LOGFONT in un oggetto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) , come illustrato nel codice seguente.


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



Tuttavia, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) non incapsula tutte le informazioni che un LOGFONT esegue. Una struttura LOGFONT contiene le dimensioni del carattere, il peso, lo stile, la sottolineatura, l'attacco, il nome del tipo di carattere e altre informazioni. Gli oggetti **IDWriteFont** contengono informazioni su un tipo di carattere e il relativo spessore e stile, ma non le dimensioni del carattere, la sottolineatura e così via. Con [DirectWrite](direct-write-portal.md), gli elementi di informazioni di formattazione, ad esempio, sono incapsulati da un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o, per intervalli specifici di testo, un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

È possibile eseguire la conversione di un [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) in un LOGFONT usando [**IDWriteGdiInterop:: ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).

## <a name="part-3-rendering"></a>Parte 3: rendering

Per eseguire il rendering del testo DirectWrite in una superficie GDI si utilizza un renderer di testo personalizzato. Vedere l'argomento [eseguire il rendering in una superficie GDI](render-to-a-gdi-surface.md) .

 

 