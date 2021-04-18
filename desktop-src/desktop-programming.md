---
description: Inizia a imparare le nozioni di base sulla creazione di applicazioni desktop eccezionali in questa sezione.
ms.assetid: 15690E05-9AF7-41A3-AF7C-8DB7C5FB9BE4
title: Introduzione
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84879e6373f4bfeb5a7e4b6a6138423d7688afe2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305124"
---
# <a name="get-started-with-desktop-windows-apps-that-use-the-win32-api"></a>Introduzione alle app desktop di Windows che usano l'API Win32

L'API Win32 (detta anche API Windows) è la piattaforma originale per applicazioni Windows native con linguaggio C/C++ che richiedono l'accesso diretto a Windows e all'hardware. Offre un'esperienza di sviluppo di prima classe senza dipendere da un ambiente di runtime gestito come .NET e WinRT (per app UWP per Windows 10). Per questo motivo l'API Win32 è la piattaforma ideale per le applicazioni che hanno bisogno del massimo livello di prestazioni e dell'accesso diretto all'hardware di sistema.

> [!NOTE]
> Questa documentazione illustra come creare app desktop di Windows con l'API Win32. L'API Win32 è una delle diverse piattaforme di app che è possibile usare per creare app desktop di Windows. Per altre informazioni sulle altre piattaforme app, vedere [scegliere la piattaforma](/windows/apps/desktop/choose-your-platform).

## <a name="get-set-up"></a>Esegui la configurazione

Seguire queste istruzioni e iniziare a creare applicazioni desktop per Windows 10 che usano l'API Win32.

1. Scaricare o aggiornare Visual Studio 2019. Se non si dispone di Visual Studio 2019, è possibile installare la versione gratuita di Microsoft Visual Studio Community 2019. Quando si installa Visual Studio, assicurarsi di selezionare l'opzione **sviluppo di applicazioni desktop con C++** . Per i collegamenti di download, vedere la pagina [download](https://developer.microsoft.com/windows/downloads) .

    > [!NOTE]
    > Quando si installa Visual Studio, è possibile selezionare facoltativamente le opzioni sviluppo per **desktop .NET** e **sviluppo piattaforma UWP (Universal Windows Platform)** per l'accesso ad altri tipi di progetto e piattaforme di app per la creazione di applicazioni desktop di Windows.

2. Se si vuole compilare l'app desktop in un [pacchetto MSIX](/windows/msix/desktop/desktop-to-uwp-root) e testare o eseguire il debug dell'app in pacchetto nel computer di sviluppo, è necessario [abilitare la modalità sviluppatore nel computer](/windows/uwp/get-started/enable-your-device-for-development).

> [!NOTE]
> Per gli script che è possibile usare per configurare il computer di sviluppo e installare altre funzionalità o pacchetti, vedere [questo progetto GitHub](https://github.com/Microsoft/windows-dev-box-setup-scripts).

## <a name="learn-how-to-create-desktop-apps-using-the-win32-api"></a>Informazioni su come creare app desktop usando l'API Win32

Se non si ha familiarità con la creazione di app desktop tramite l'API Win32, le esercitazioni e gli articoli seguenti aiuteranno a iniziare.

| Argomento        | Descrizione      |
|---------------|-----------------|
| [Creare la prima app Win32 C++](LearnWin32/learn-to-program-for-windows.md)    | Questa esercitazione illustra come scrivere un programma Windows in C++ usando le API Win32 e COM.  |
| [Creare la prima app usando DirectX](direct3dgetstarted/building-your-first-directx-app.md) | Questa esercitazione di base consentirà di iniziare a sviluppare app DirectX.            |
| [Guida alla programmazione per Windows a 64 bit](WinProg64/programming-guide-for-64-bit-windows.md)    | Viene descritta la programmazione per le versioni a 64 bit del sistema operativo Windows. |
| [Uso delle intestazioni di Windows](WinProg/using-the-windows-headers.md)     | Viene fornita una panoramica di alcune delle convenzioni utilizzate nei file di intestazione di Windows. |

È anche possibile esplorare gli [esempi di app desktop](https://github.com/Microsoft/Windows-classic-samples).

## <a name="modernize-your-desktop-apps-for-windows-10"></a>Modernizza le tue app desktop per Windows 10

Se si dispone di un'app Win32 per desktop esistente, nel piattaforma UWP (Universal Windows Platform) (UWP) sono disponibili numerose funzionalità che è possibile utilizzare per offrire la migliore esperienza possibile in Windows 10. Ad esempio, a partire da Windows 10, versione 1903, è possibile ospitare i controlli UWP XAML nell'app Win32 Desktop usando una funzionalità denominata isole XAML.

La maggior parte di queste funzionalità di UWP sono disponibili come componenti modulari che è possibile adottare nell'app desktop in modo autonomo senza dover riscrivere l'intera applicazione. È possibile migliorare l'app desktop esistente scegliendo le parti di Windows 10 e UWP da adottare.

Per altre informazioni, vedi [Modernizzare le app desktop](/windows/apps/desktop/modernize).

## <a name="cwinrt"></a>C++/WinRT

Facoltativamente, è possibile configurare il computer di sviluppo per l'utilizzo di [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/). C++/WinRT è una proiezione del linguaggio C++ 17 completamente standard che consente di usare facilmente API Windows Runtime API Windows Runtime (WinRT) dall'applicazione desktop Win32 di C++. C++/WinRT viene implementato come libreria basata su file di intestazione.

Per configurare il progetto per C++/WinRT:

* Per i nuovi progetti, puoi installare l'[Estensione di Visual Studio C++/WinRT (VSIX)](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264) e usare uno dei modelli di progetto C++/WinRT inclusi in questa estensione.
* Per i progetti di applicazioni desktop di Windows esistenti, è possibile installare il pacchetto NuGet [Microsoft. Windows. CppWinRT](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/) nel progetto.

Per altre informazioni su queste opzioni, vedi [questo articolo](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package).

## <a name="whats-new-for-win32-apis-in-windows-10"></a>Novità delle API Win32 in Windows 10

Per informazioni sulle nuove API Win32 introdotte in Windows 10 [, vedere Novità](whats-new.md).

## <a name="get-started-with-win32-features-and-technologies"></a>Inizia a usare le funzionalità e le tecnologie Win32

Sono disponibili API Win32 per molte funzionalità e tecnologie di Windows 10, tra cui l'interfaccia utente principale e le API windowing, l'audio e la grafica e la rete. Per istruzioni e esempi di codice relativi all'uso di queste API, [vedere l'indice delle funzionalità e delle tecnologie](desktop-app-technologies.md).

## <a name="related-topics"></a>Argomenti correlati

* [Sviluppare app desktop](/windows/apps/desktop)
* [Informazioni di riferimento sulle API Windows](/windows/desktop/api/)
* [Indice di API Windows](/windows/desktop/apiindex/api-index-portal)
* [Riferimento Windows Runtime C++](/windows/desktop/winrt/reference)
