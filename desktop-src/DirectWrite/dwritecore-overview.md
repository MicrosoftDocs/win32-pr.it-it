---
title: Panoramica di DWriteCore
description: DWriteCore è l'implementazione Project Implementation di DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: 49681f434fa4eef99e9775b2c3800f48f15915a2
ms.sourcegitcommit: 8a31a21726d4a8ebfddfa71f02f1bfffea459277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/20/2021
ms.locfileid: "110208712"
---
# <a name="dwritecore-overview"></a>Panoramica di DWriteCore

DWriteCore è l'implementazione [project-of-project](/windows/apps/project-reunion/) di [DirectWrite (DirectWrite](./direct-write-portal.md) è l'API DirectX per il rendering di testo di alta qualità, i tipi di carattere del contorno indipendenti dalla risoluzione e il supporto completo di layout e testo Unicode). DWriteCore è una forma di DirectWrite che viene eseguita nelle versioni di Windows fino a Windows 10, versione 1809 (10.0; Build 17763) e apre la porta per l'uso multipiattaforma.

Questo argomento introduttivo descrive che cos'è DWriteCore e illustra come installarlo nell'ambiente di sviluppo e programmarlo con esso.

## <a name="the-value-proposition-of-dwritecore"></a>Proposta di valore di DWriteCore

[DirectWrite](./direct-write-portal.md) stesso supporta una vasta gamma di funzionalità che lo rendono lo strumento di rendering dei caratteri preferito in Windows per la maggior parte delle app, sia tramite chiamate dirette &mdash; che tramite [Direct2D.](../direct2d/direct2d-portal.md) DirectWrite include un sistema di layout di testo indipendente dal dispositivo, rendering del testo [ClearType Microsoft ClearType](/typography/cleartype/) di qualità elevata, testo con accelerazione hardware, testo in più formati, funzionalità tipografiche [OpenType avanzate®](/typography/opentype/) supporto di lingue wide e layout e rendering compatibili con [GDI.](../gdi/windows-gdi.md) DirectWrite è disponibile a partire da Windows Vista SP2 e si è evoluto nel corso degli anni per includere funzionalità più avanzate, ad esempio i tipi di carattere variabili, che consentono di applicare stili, pesi e altri attributi a un tipo di carattere con una sola risorsa tipo di carattere.

A causa della lunga durata di DirectWrite, tuttavia, i progressi nello sviluppo hanno tendenziamente lasciato indietro le versioni precedenti di Windows. Inoltre, lo stato di DirectWrite come tecnologia di rendering del testo premier è limitato solo a Windows, lasciando alle applicazioni multipiattaforma di scrivere il proprio stack di rendering del testo o di basarsi su soluzioni di terze parti.

DWriteCore risolve i problemi fondamentali dell'orfano delle funzionalità della versione e della compatibilità multipiattaforma rimuovendo la libreria dal sistema e selezionando come destinazione tutti i possibili endpoint supportati. A tale scopo, DWriteCore è stato integrato in Project Reunion.

Il valore principale che DWriteCore offre, in quanto sviluppatore, in Project Reunion è che fornisce l'accesso a molte (e infine a tutte) funzionalità DirectWrite. Tutte le funzionalità di DWriteCore funzioneranno allo stesso modo in tutte le versioni di livello inferiore senza differenze in merito alle funzionalità che potrebbero funzionare su quali versioni.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>The DWriteCore demo app &mdash; DWriteCoreGallery

DWriteCore viene illustrato tramite l'app di esempio [DWriteCoreGallery,](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) che è ora disponibile per il download e lo studio.

## <a name="get-started-with-dwritecore"></a>Introduzione a DWriteCore

DWriteCore fa parte di [Project Reunion 0.5.](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0) Questa sezione descrive come configurare l'ambiente di sviluppo per la programmazione con DWriteCore.

### <a name="install-the-project-reunion-05-vsix"></a>Installare Project Reunion 0.5 VSIX

In Visual Studio fare clic su **Estensioni**  >  **Gestisci estensioni,** cercare *Project Reunion* e scaricare l'estensione Project Reunion. Chiudere e riaprire Visual Studio e seguire le istruzioni per installare l'estensione.

Per altre informazioni, vedere [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)e Configurare l'ambiente di [sviluppo (per Project Reunion).](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment)

### <a name="create-a-new-project"></a>Creare un nuovo progetto

In Visual Studio creare un nuovo progetto dal modello di progetto App vuota in pacchetto **(WinUI 3 in Desktop).** È possibile trovare il modello di progetto scegliendo il linguaggio: *C++;* platform: *Project Reunion*; Tipo di progetto: *Desktop*.

Per altre informazioni, vedere [Introduzione a WinUI 3 per le app desktop.](/windows/apps/winui/winui3/get-started-winui3-for-desktop)

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a>Installare il pacchetto NuGet Microsoft.ProjectReunion.DWrite

In Visual Studio fare clic  su Project Manage NuGet Packages... Browse (Gestisci pacchetti NuGet) e digitare o incollare \>  \>  **Microsoft.ProjectReunion.DWrite** nella casella di ricerca, selezionare l'elemento nei risultati della ricerca e quindi fare clic **su Installa** per installare il pacchetto per il progetto.

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a>In alternativa, iniziare con l'app di esempio DWriteCoreGallery

In alternativa, è possibile programmare con DWriteCore iniziando con il progetto di app di esempio [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) e basando lo sviluppo su tale progetto. È quindi possibile rimuovere qualsiasi codice sorgente (o file) esistente dal progetto di esempio e aggiungere qualsiasi nuovo codice sorgente (o file) al progetto.

### <a name="use-dwritecore-in-your-project"></a>Usare DWriteCore nel progetto

Per altre informazioni sulla programmazione con DWriteCore, vedere la [sezione Programmazione con DWriteCore](#programming-with-dwritecore) più avanti in questo argomento.

## <a name="the-release-phases-of-dwritecore"></a>Fasi di rilascio di DWriteCore

La portabilità di DirectWrite in DWriteCore è un progetto sufficientemente grande da estendersi su più cicli di rilascio di Windows. Il progetto è suddiviso in fasi, ognuna delle quali corrisponde a un blocco di funzionalità fornito in una versione.

### <a name="features-in-the-current-release-of-dwritecore"></a>Funzionalità nella versione corrente di DWriteCore

La versione di DWriteCore attualmente disponibile fa parte [di ProjectScrivono 0.5.](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0) Contiene gli strumenti di base che gli sviluppatori devono usare DWriteCore, incluse le funzionalità seguenti.

- Enumerazione dei tipi di carattere.
- API del tipo di carattere.
- Modellatura.
- API di rendering di basso livello. Questa operazione è parziale nella fase &mdash; corrente. DWriteCore non interagisce con [Direct2D,](../direct2d/direct2d-portal.md)ma è possibile usare [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget.**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)
- Funzionalità di layout di testo di base.
- API per il rendering del testo.
- Destinazione di rendering bitmap.
- Tipi di carattere a colori.
- Ottimizzazioni varie (pulizia della cache dei tipi di carattere, caricatore dei tipi di carattere in memoria e così via).

Una funzionalità banner è tipi di carattere a colori. I tipi di carattere a colori consentono di eseguire il rendering dei tipi di carattere con funzionalità di colore più sofisticate oltre ai semplici colori singoli. Ad esempio, i tipi di carattere a colori sono ciò che consente di eseguire il rendering dei tipi di carattere emoji e delle icone della barra degli strumenti (il secondo dei quali viene usato da Office, ad esempio). I tipi di carattere a colori sono stati introdotti per la prima volta Windows 8.1, ma la funzionalità è stata ampiamente ampliata in Windows 10 versione 1607 (aggiornamento dell'anniversario).

Le operazioni di pulizia della cache dei tipi di carattere e del caricatore dei tipi di carattere in memoria consentono un caricamento più rapido dei tipi di carattere e miglioramenti della memoria.

Con queste funzionalità, è possibile iniziare immediatamente a sfruttare alcune delle funzionalità di base moderne di &mdash; DirectWrite, ad esempio i tipi di carattere variabili. I tipi di carattere variabili sono una delle funzionalità più importanti per i clienti DirectWrite.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>L'invito all'utente come sviluppatore DirectWrite

DWriteCore, insieme ad altri componenti di Project Reunion, verrà sviluppato con apertura al feedback degli sviluppatori. Microsoft invita a iniziare a esplorare DWriteCore e a fornire informazioni dettagliate o richieste sullo sviluppo di funzionalità nel [repository GitHub di Project Reunion.](https://github.com/microsoft/ProjectReunion/)

## <a name="programming-with-dwritecore"></a>Programmazione con DWriteCore

Proprio come con [DirectWrite,](./direct-write-portal.md)si programma con DWriteCore tramite la relativa API com-light, tramite [**l'interfaccia IDWriteFactory.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)

Per usare DWriteCore, è necessario includere il `dwrite_core.h` file di intestazione.

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

Il `dwrite_core.h` file di intestazione definisce innanzitutto il token *DWRITE_CORE* e quindi include il file `dwrite_3.h` di intestazione. Il *DWRITE_CORE* token è importante, perché indica a tutte le intestazioni incluse successivamente di rendere disponibili tutte le API DirectWrite. Dopo che il progetto ha incluso , è possibile continuare a `dwrite_core.h` scrivere codice, compilare ed eseguire.

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>API nuove o diverse per DWriteCore

La superficie dell'API DWriteCore è in gran parte la stessa di [directwrite.](/windows/win32/api/_directwrite/) Esiste tuttavia un numero ridotto di nuove API attualmente presenti solo in DWriteCore.

#### <a name="create-a-factory-object"></a>Creare un oggetto factory

La [**funzione gratuita DWriteCoreCreateFactory**](/windows/win32/directwrite/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) crea un oggetto factory che viene usato per la creazione successiva di singoli oggetti DWriteCore.

**DWriteCoreCreateFactory** è funzionalmente uguale alla funzione [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) esportata dalla versione di sistema di DirectWrite. La funzione DWriteCore ha un nome diverso per evitare ambiguità.

#### <a name="create-a-restricted-factory-object"></a>Creare un oggetto factory con restrizioni

L DWRITE_FACTORY_TYPE enumezione ha una nuova costante [](./dwrite/ne-dwrite-dwrite_factory_type.md) &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, che indica una factory con restrizioni. Una factory con restrizioni è più bloccata rispetto a una factory isolata. Non interagisce in alcun modo con una cache dei tipi di carattere multi-processo né persistente. Inoltre, la raccolta di tipi di carattere di sistema restituita da questa factory include solo tipi di carattere noti. Ecco come è possibile usare **DWRITE_FACTORY_TYPE_ISOLATED2** per creare un oggetto factory con restrizioni quando si chiama la funzione [**gratuita DWriteCoreCreateFactory.**](/windows/win32/directwrite/dwrite_core/nf-dwrite_core-dwritecorecreatefactory)

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

Se si passa **DWRITE_FACTORY_TYPE_ISOLATED2** a una versione precedente di DirectWrite che non la **supporta,** **DWriteCreateFactory** restituisce E_INVALIDARG .

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Disegno di glifi in una bitmap della memoria di sistema

DirectWrite ha un'interfaccia di destinazione di rendering bitmap che supporta il rendering dei glifi in una bitmap nella memoria di sistema. Tuttavia, attualmente l'unico modo per ottenere l'accesso ai dati pixel sottostanti è passare attraverso GDI e quindi l'API non è utilizzabile multipiattaforma. Questo problema si può risolvere facilmente aggiungendo un metodo per recuperare i dati pixel.

DWriteCore introduce quindi [**l'interfaccia IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) e il relativo [**metodo IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md). Tale metodo accetta un parametro di tipo (puntatore a) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), che è un nuovo struct.

L'applicazione crea una destinazione di rendering bitmap chiamando [IDWriteGdiInterop::CreateBitmapRenderTarget.](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) In Windows, una destinazione di rendering bitmap incapsula un controller di dominio di memoria GDI con una bitmap GDI indipendente dal dispositivo (DIB) selezionata. [IDWriteBitmapRenderTarget::D rawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) esegue il rendering dei glifi nella dib. DirectWrite esegue il rendering dei glifi stessi senza passare attraverso GDI. L'applicazione può quindi ottenere **l'HDC** dalla destinazione di rendering bitmap e usare [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) per copiare i pixel in **una finestra HDC.**

Nelle piattaforme non Windows, l'applicazione può comunque creare una destinazione di rendering bitmap, ma incapsula semplicemente una matrice di memoria di sistema senza **HDC** e senza DIB. Senza **hdc,** l'applicazione deve ottenere i pixel della bitmap in modo che possa copiarli o usarli in altro modo. Anche in Windows, a volte è utile ottenere i dati pixel effettivi e viene illustrato il modo corrente per eseguire questa operazione nell'esempio di codice seguente.

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a>Altre differenze dell'API tra DWriteCore e DirectWrite

Esistono alcune API che sono solo stub o si comportano in modo leggermente diverso nelle piattaforme non Windows. Ad esempio, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) restituisce **E_NOTIMPL** su piattaforme non Windows, poiché non esiste un **HDC** senza [GDI.](../gdi/windows-gdi.md)

Infine, esistono alcune altre API di Windows che vengono in genere usate insieme a DirectWrite (Direct2D è un esempio di grande impatto). Tuttavia, attualmente Direct2D e DWriteCore non interoperativizzano. Ad esempio, se si crea un [**oggetto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando DWriteCore e lo si passa a [**D2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), la chiamata avrà esito negativo.
