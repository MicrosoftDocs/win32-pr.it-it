---
title: Panoramica di DWriteCore
description: DWriteCore è l'implementazione del progetto di riunione di DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 12/09/2020
ms.openlocfilehash: 605cab8d0cd0511b5ca3b0b14d517cdc3f290573
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351036"
---
# <a name="dwritecore-overview"></a>Panoramica di DWriteCore

DWriteCore è l'implementazione del [progetto di riunione](/windows/apps/project-reunion/) di [DirectWrite](./direct-write-portal.md). DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme.

In questo argomento introduttivo viene descritto che cos'è DWriteCore e viene illustrato come installarlo nel proprio ambiente di sviluppo e come programma.

## <a name="the-value-proposition-of-dwritecore"></a>Proposta di valore di DWriteCore

[DirectWrite](./direct-write-portal.md) supporta una vasta gamma di funzionalità che lo rendono lo strumento di rendering dei tipi di carattere preferito in Windows per la maggior parte delle app &mdash; , sia tramite chiamate dirette che tramite [Direct2D](../direct2d/direct2d-portal.md). DirectWrite include un sistema di layout del testo indipendente dal dispositivo, un sottopixel di qualità elevata per il rendering del testo di [Microsoft ClearType](/typography/cleartype/) , un testo con accelerazione hardware, testo in più formati, funzionalità [OpenType®](/typography/opentype/) tipografiche avanzate, supporto del linguaggio Wide e layout e rendering compatibili con [GDI](../gdi/windows-gdi.md). DirectWrite è stato disponibile a partire da Windows Vista SP2 e si è evoluto nel corso degli anni per includere funzionalità più avanzate, ad esempio tipi di carattere variabili, che consentono agli sviluppatori di applicare stili, pesi e altri attributi a un tipo di carattere con una sola risorsa del tipo di carattere.

A causa della durata prolungata di DirectWrite, tuttavia, gli anticipi nello sviluppo hanno avuto la tendenza a lasciare le versioni precedenti di Windows. Inoltre, lo stato di DirectWrite come tecnologia di rendering del testo Premier è limitato solo a Windows, lasciando le applicazioni multipiattaforma a scrivere il proprio stack di rendering del testo o a utilizzare soluzioni di terze parti.

DWriteCore risolve i problemi fondamentali di isolamento delle funzionalità di versione e compatibilità multipiattaforma rimuovendo la libreria dal sistema e indirizzando tutti i possibili endpoint supportati. A tal fine, DWriteCore è stato integrato in Project Reunion con un'API pubblica supportata su tutti gli endpoint di Windows fino a Windows 8 e apre la porta per l'uso multipiattaforma.

Il valore principale che DWriteCore fornisce, come sviluppatore, in Project Reunion è che fornisce l'accesso a tutte le funzionalità di DirectWrite correnti, fino a Windows 8. Tutte le funzionalità di DWriteCore funzioneranno in tutte le versioni di livello inferiore. in altre parole, tutte le funzionalità correnti funzioneranno in Windows 8, 8,1 e in tutte le versioni di Windows 10, senza alcuna disparità in merito alle funzionalità che possono funzionare per le versioni.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>App demo DWriteCore &mdash; DWriteCoreGallery

DWriteCore viene illustrato tramite l'app di esempio [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , disponibile per il download e lo studio.

## <a name="get-started-with-dwritecore"></a>Introduzione a DWriteCore

Per la versione preliminare del progetto Reunion 0,1, attualmente non è supportata l'installazione del pacchetto NuGet di riunione del progetto nei propri progetti. Al contrario, l'opzione attualmente supportata per la programmazione personalizzata con DWriteCore consiste nell'iniziare con il progetto di app di esempio [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) e basare lo sviluppo su tale progetto.

È quindi possibile rimuovere qualsiasi codice sorgente (o file) esistente dal progetto di esempio e aggiungere eventuali nuovi codici sorgente (o file) al progetto. Per ulteriori informazioni sulla programmazione con DWriteCore, vedere la sezione [Programming with DWriteCore](#programming-with-dwritecore) più avanti in questo argomento.

## <a name="the-release-phases-of-dwritecore"></a>Fasi di rilascio di DWriteCore

Il porting di DirectWrite a DWriteCore è un progetto sufficientemente grande per estendere più cicli di rilascio di Windows. Il progetto è suddiviso in fasi, ciascuna delle quali corrisponde a un blocco di funzionalità fornito in una versione.

### <a name="features-in-the-current-release-of-dwritecore"></a>Funzionalità nella versione corrente di DWriteCore

La versione di DWriteCore attualmente disponibile contiene gli strumenti di base che gli sviluppatori hanno bisogno di utilizzare DWriteCore, incluse le funzionalità seguenti.

- Enumerazione del tipo di carattere.
- API del tipo di carattere.
- Shaping.
- API per il rendering di basso livello. Questa operazione è parziale alla fase corrente &mdash; DWriteCore non interagisce con [Direct2D](../direct2d/direct2d-portal.md), ma è possibile usare [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).
- Funzionalità di layout del testo di base.
- API per il rendering del testo.
- Destinazione di rendering bitmap.
- Tipi di carattere colore.
- Ottimizzazioni varie (pulizia della cache dei tipi di carattere, caricatore del tipo di carattere in memoria e così via).

La funzionalità banner in questa fase è il colore dei tipi di carattere. I tipi di carattere colori consentono di eseguire il rendering dei tipi di carattere con funzionalità di colore più sofisticate, oltre a semplici colori singoli Ad esempio, i tipi di carattere a colori sono la capacità di eseguire il rendering dei tipi di carattere emoji e dell'icona della barra degli strumenti, ad esempio il secondo utilizzato da Office. I tipi di carattere di colore sono stati introdotti per la prima volta in Windows 8.1, ma la funzionalità è stata notevolmente espansa in Windows 10, versione 1607 (aggiornamento dell'anniversario).

Il lavoro di pulizia della cache dei tipi di carattere e del caricatore del tipo di carattere in memoria consente un caricamento più rapido dei tipi di carattere e i miglioramenti della memoria.

Grazie a queste funzionalità, è possibile iniziare subito a sfruttare alcune delle funzionalità di base moderne di DirectWrite, &mdash; ad esempio i tipi di carattere variabili &mdash; di livello inferiore a Windows 8. Questa iterazione della libreria può essere usata anche in [Android](https://www.android.com/)e **Linux**. I tipi di carattere variabili sono una delle funzionalità più importanti per i clienti di DirectWrite. sono stati introdotti in Windows 10, versione 1709 (Fall Creators Update), quindi l'accesso alle versioni precedenti è una grande vantaggio per gli sviluppatori.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>Il nostro invito per gli sviluppatori DirectWrite

DWriteCore, insieme ad altri componenti di riunione del progetto, verranno sviluppati con apertura al feedback degli sviluppatori. Ti invitiamo a iniziare a esplorare DWriteCore e a fornire informazioni dettagliate o richieste per lo sviluppo di funzionalità nel [repository GitHub del progetto Reunion](https://github.com/microsoft/ProjectReunion/).

## <a name="programming-with-dwritecore"></a>Programmazione con DWriteCore

Come già indicato, per la versione preliminare del progetto Reunion 0,1, l'opzione attualmente supportata per la programmazione personalizzata con DWriteCore consiste nell'iniziare con il progetto di app di esempio [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

Analogamente a quanto avviene con [DirectWrite](./direct-write-portal.md), è possibile programmare con DWriteCore tramite la relativa API Light com, tramite l'interfaccia [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .

**DWriteCoreGallery** include già il `dwrite_core.h` file di intestazione. Tale intestazione definisce innanzitutto il token *DWRITE_CORE* e quindi include `dwrite_3.h` . Il token *DWRITE_CORE* è importante, perché indirizza le intestazioni incluse successivamente per rendere disponibili tutte le API DirectWrite. Una volta incluso un progetto `dwrite_core.h` , è possibile procedere e scrivere codice, compilare ed eseguire.

```cppwinrt
// pch.h
...
#include <dwrite_core.h>
```

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>API nuove o diverse per DWriteCore

La superficie dell'API DWriteCore è sostanzialmente identica a quella di [DirectWrite](/windows/win32/api/_directwrite/). Tuttavia, esiste un numero ridotto di nuove API che sono presenti solo in DWriteCore.

#### <a name="create-a-restricted-factory-object"></a>Creare un oggetto factory con restrizioni

L'enumerazione [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) dispone di una nuova &mdash; **DWRITE_FACTORY_TYPE_RESTRICTED** costante. Una factory con restrizioni è più bloccata rispetto a una factory isolata. Non interagisce in alcun modo con una cache dei tipi di carattere incrociata o persistente. Inoltre, la raccolta di tipi di carattere del sistema restituita da questa Factory include solo tipi di carattere noti. Ecco come è possibile usare **DWRITE_FACTORY_TYPE_RESTRICTED** per creare un oggetto Factory limitato quando si chiama la funzione [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) free.

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCreateFactory(
    DWRITE_FACTORY_TYPE_RESTRICTED,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

Se si passa **DWRITE_FACTORY_TYPE_RESTRICTED** a una versione precedente di DirectWrite che non la supporta, **DWriteCreateFactory** restituisce **E_INVALIDARG**.

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Disegno di glifi in una bitmap di memoria di sistema

DirectWrite dispone di un'interfaccia di destinazione di rendering bitmap che supporta il rendering di glifi in una bitmap nella memoria di sistema. Attualmente, tuttavia, l'unico modo per ottenere l'accesso ai dati pixel sottostanti consiste nel passare attraverso GDI, quindi l'API non è utilizzabile tra piattaforme diverse. Per ovviare a questo problema, è possibile aggiungere un metodo per recuperare i dati pixel.

Quindi DWriteCore introduce l'interfaccia [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) e il relativo metodo [**IDWriteBitmapRenderTarget2:: getbitmapdata**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md). Tale metodo accetta un parametro di tipo (puntatore a) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), che è un nuovo struct.

L'applicazione crea una destinazione di rendering bitmap chiamando [IDWriteGdiInterop:: CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget). In Windows una destinazione di rendering bitmap incapsula un controller di dominio di memoria GDI con una bitmap indipendente dal dispositivo GDI (DIB). [IDWriteBitmapRenderTarget::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) esegue il rendering dei GLIFI in DIB. DirectWrite esegue il rendering dei glifi senza passare attraverso GDI. L'applicazione può quindi ottenere l' **HDC** dalla destinazione di rendering bitmap e usare [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) per copiare i pixel in una finestra **HDC**.

Sulle piattaforme non Windows, l'applicazione può comunque creare una destinazione di rendering bitmap, ma incapsula semplicemente una matrice di memoria di sistema senza **HDC** e nessuna DIB. Senza un **HDC**, è necessario un altro modo per consentire all'applicazione di ottenere i pixel della bitmap in modo che possano copiarli o usarli in altro modo. Anche in Windows, è talvolta utile ottenere i dati effettivi dei pixel e viene illustrato il modo corrente per eseguire questa operazione nell'esempio di codice riportato di seguito.

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a>Altre differenze di API tra DWriteCore e DirectWrite

Esistono alcune API che sono solo Stub o si comportano in modo diverso nelle piattaforme non Windows. Ad esempio, [IDWriteGdiInterop:: CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) restituisce **E_NOTIMPL** su piattaforme non Windows, dal momento che non esiste alcuna cosa come un **HDC** senza [GDI](../gdi/windows-gdi.md).

Infine, esistono alcune altre API Windows che vengono in genere usate insieme a DirectWrite (Direct2D è un esempio importante). Attualmente, Direct2D e DWriteCore, tuttavia, non interagiscono. Se ad esempio si crea un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) con DWriteCore e lo si passa a [**D2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), la chiamata avrà esito negativo.