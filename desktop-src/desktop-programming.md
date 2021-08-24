---
description: Introduzione alle nozioni di base per la creazione di app desktop di grande livello in questa sezione.
ms.assetid: 15690E05-9AF7-41A3-AF7C-8DB7C5FB9BE4
title: Introduzione
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f791589d73447798a7721c52164a2002b48a792959c698b835039293ce6004d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755011"
---
# <a name="get-started-with-desktop-windows-apps-that-use-the-win32-api"></a>Introduzione alle app Windows desktop che usano l'API Win32

L'API Win32 (detta anche API Windows) è la piattaforma originale per applicazioni Windows native con linguaggio C/C++ che richiedono l'accesso diretto a Windows e all'hardware. Offre un'esperienza di sviluppo di prima classe senza dipendere da un ambiente di runtime gestito come .NET e WinRT (per le app UWP per Windows 10). Per questo motivo l'API Win32 è la piattaforma ideale per le applicazioni che hanno bisogno del massimo livello di prestazioni e dell'accesso diretto all'hardware di sistema.

> [!NOTE]
> Questa documentazione illustra come creare app desktop Windows con l'API Win32. L'API Win32 è una delle diverse piattaforme di app che è possibile usare per creare app Windows desktop. Per altre informazioni sulle altre piattaforme per le app, vedere [Scegliere la piattaforma.](/windows/apps/desktop/choose-your-platform)

## <a name="get-set-up"></a>Completare la configurazione

Seguire queste istruzioni e iniziare a creare app desktop per Windows 10 che usano l'API Win32.

1. Scaricare o aggiornare Visual Studio 2019. Se non si dispone di Visual Studio 2019, è possibile installare la versione gratuita di Microsoft Visual Studio Community 2019. Quando si installa Visual Studio, assicurarsi di selezionare l'opzione **Sviluppo di applicazioni desktop con C++.** Per i collegamenti di download, vedere la [pagina Download.](https://developer.microsoft.com/windows/downloads)

    > [!NOTE]
    > Quando si installa Visual Studio, è possibile selezionare facoltativamente le opzioni **Sviluppo per desktop .NET** e Sviluppo per la piattaforma **Universal Windows** per l'accesso ad altri tipi di progetto e piattaforme di app per la creazione di app Windows desktop.

2. Se si vuole compilare l'app desktop in un pacchetto [MSIX](/windows/msix/desktop/desktop-to-uwp-root) ed eseguire il test o il debug dell'app in pacchetto nel computer di sviluppo, è necessario abilitare la modalità [sviluppatore nel computer](/windows/uwp/get-started/enable-your-device-for-development).

> [!NOTE]
> Per gli script che è possibile usare per configurare il computer di sviluppo e installare altre funzionalità o pacchetti, vedere questo [GitHub progetto](https://github.com/Microsoft/windows-dev-box-setup-scripts).

## <a name="learn-how-to-create-desktop-apps-using-the-win32-api"></a>Informazioni su come creare app desktop usando l'API Win32

Se non si ha esperienza con la creazione di app desktop con l'API Win32, le esercitazioni e gli articoli seguenti consentono di iniziare.

| Argomento        | Descrizione      |
|---------------|-----------------|
| [Creare la prima app Win32 C++](LearnWin32/learn-to-program-for-windows.md)    | Questa esercitazione illustra come scrivere un programma Windows in C++ usando Win32 e le API COM.  |
| [Creare la prima app con DirectX](direct3dgetstarted/building-your-first-directx-app.md) | Questa esercitazione di base consente di iniziare a usare lo sviluppo di app DirectX.            |
| [Guida alla programmazione per Windows a 64 bit](WinProg64/programming-guide-for-64-bit-windows.md)    | Descrive la programmazione per le versioni a 64 bit del Windows operativo. |
| [Uso delle intestazioni Windows](WinProg/using-the-windows-headers.md)     | Viene fornita una panoramica di alcune delle convenzioni utilizzate nei file Windows di intestazione. |

È anche possibile esplorare gli esempi [di app desktop](https://github.com/Microsoft/Windows-classic-samples).

## <a name="modernize-your-desktop-apps-for-windows-10"></a>Modernizzare le app desktop per Windows 10

Se si dispone di un'app Win32 desktop esistente, sono disponibili molte funzionalità della piattaforma UWP (Universal Windows Platform) che è possibile usare per offrire la migliore esperienza possibile in Windows 10. Ad esempio, a partire da Windows 10 versione 1903, puoi ospitare controlli XAML UWP nell'app Win32 desktop usando una funzionalità denominata Isole XAML.

La maggior parte di queste funzionalità UWP è disponibile come componenti modulari che è possibile adottare nell'app desktop al proprio ritmo senza dover riscrivere l'intera applicazione. È possibile migliorare l'app desktop esistente scegliendo le parti Windows 10 e UWP da adottare.

Per altre informazioni, vedi [Modernizzare le app desktop](/windows/apps/desktop/modernize).

## <a name="cwinrt"></a>C++/WinRT

Facoltativamente, è possibile configurare il computer di sviluppo per [l'uso di C++/WinRT.](/windows/uwp/cpp-and-winrt-apis/) C++/WinRT è una proiezione di linguaggio C++17 moderna completamente standard che consente di usare facilmente le API di runtime Windows Windows Runtime (WinRT) dall'applicazione desktop Win32 C++. C++/WinRT viene implementato come libreria basata su file di intestazione.

Per configurare il progetto per C++/WinRT:

* Per i nuovi progetti, puoi installare l'[Estensione di Visual Studio C++/WinRT (VSIX)](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264) e usare uno dei modelli di progetto C++/WinRT inclusi in questa estensione.
* Per i Windows di applicazioni desktop esistenti, è possibile installare [Microsoft.Windows. CppWinRT NuGet](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/) pacchetto nel progetto.

Per altre informazioni su queste opzioni, vedi [questo articolo](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package).

## <a name="whats-new-for-win32-apis-in-windows-10"></a>Novità delle API Win32 in Windows 10

Per informazioni sulle nuove API Win32 introdotte in Windows 10, vedere [novità di](whats-new.md).

## <a name="get-started-with-win32-features-and-technologies"></a>Introduzione alle funzionalità e alle tecnologie Win32

Le API Win32 sono disponibili per molte funzionalità e tecnologie in Windows 10, tra cui l'interfaccia utente di base e le API di windowing, audio, grafica e rete. Per indicazioni ed esempi di codice sull'uso di queste API, vedere [l'indice delle funzionalità e delle tecnologie.](desktop-app-technologies.md)

## <a name="related-topics"></a>Argomenti correlati

* [Sviluppare app desktop](/windows/apps/desktop)
* [Windows Informazioni di riferimento sulle API](/windows/desktop/api/)
* [Indice di API Windows](/windows/desktop/apiindex/api-index-portal)
* [Windows Informazioni di riferimento sul runtime C++](/windows/desktop/winrt/reference)
