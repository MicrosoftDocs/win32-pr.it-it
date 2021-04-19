---
description: XAudio2 è un'API multipiattaforma che è stata fornita per l'uso in Xbox 360, oltre che nelle versioni di Windows, tra cui Windows XP, Windows Vista, Windows 7 e Windows 8.
ms.assetid: 875b44c4-30d6-8a6e-0cfc-9beb8c46f1b4
title: Versioni di XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c9facfe357c323bd8f7b607460a8f59bd062fe
ms.sourcegitcommit: 010f524cd6098a5941de77907d4d6ae7871f8af1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "106320199"
---
# <a name="xaudio2-versions"></a>Versioni di XAudio2

XAudio2 è un'API multipiattaforma che è stata fornita per l'uso in Xbox 360, oltre che nelle versioni di Windows, tra cui Windows XP, Windows Vista, Windows 7 e Windows 8. In Xbox 360, XAudio2 viene fornito come una libreria statica compilata nell'eseguibile del gioco principale. In Windows, XAudio2 viene fornito come libreria a collegamento dinamico (DLL) installata nelle cartelle di sistema del sistema operativo.

## <a name="xaudio-29-windows-10-and-redistributable-for-windows-7-and-windows-8x"></a>XAudio 2,9 (Windows 10 e ridistribuibile per Windows 7 e Windows 8. x)

XAudio2 versione 2,9 viene fornito come parte di Windows 10, XAUDIO2 \_9.DLL, insieme a XAudio 2,8 per supportare le applicazioni meno recenti. È disponibile anche una [versione ridistribuibile di XAudio 2,9](xaudio2-redistributable.md) per Windows 7 SP1, Windows 8 e Windows 8.1.

XAudio 2.9 è stato aggiornato con le modifiche seguenti:

-   Nuovi flag di creazione: \_ \_ motore di debug XAUDIO2, \_ motore di arresto XAUDIO2 \_ \_ quando \_ inattivo, XAUDIO2 \_ 1024 \_ Quantum
-   il supporto di xWMA è disponibile in questa versione di XAudio2.
-   La funzione [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) è supportata nella versione Windows 10 di xaudio 2,9.
-   [**XAUDIO2FX \_ I \_ parametri del riverbero**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) ora includono il valore *SideDelay* per i sistemi 7,1.
-   La funzione [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative) include ora il parametro booleano *sevenDotOneReverb* che abilita il riverbero 7,1.

## <a name="xaudio-28-windows-8x"></a>XAudio 2,8 (Windows 8. x)

XAudio2 versione 2,8 è attualmente disponibile come componente di sistema in Windows 8, XAUDIO2 \_8.DLL. È disponibile "posta in arrivo" e non richiede la ridistribuzione con un'app. Si consiglia di utilizzare Windows Software Development Kit (SDK) per Windows 8 per lo sviluppo con XAudio2. Il Windows SDK per Windows 8 contiene l'intestazione e la libreria di importazione necessari per il collegamento statico a XAUDIO2 \_8.DLL.

XAudio2 2,8 è stato aggiornato con le modifiche seguenti:

-   Questa versione supporta lo sviluppo di applicazioni Windows Store. l'API XAudio2 può essere usata nelle app di Windows Store C++/DirectX.
-   [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) è una chiamata API Win32 flat e non crea più un CLSID XAudio2. Il supporto per la creazione di un'istanza di XAudio2 da CoCreateInstance è stato rimosso.
-   La funzione Initialize viene ora chiamata in modo implicito dal processo di creazione ed è stata rimossa dall'interfaccia [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .
-   La funzionalità di enumerazione del dispositivo è stata rimossa da XAudio2; le funzioni GetDeviceDetails e GetDeviceCount sono state rimosse dall'interfaccia [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) . Le app che vogliono eseguire il rendering in altri dispositivi audio del sistema devono passare una stringa dell'identificatore del dispositivo a [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) anziché a un indice del dispositivo. Il dispositivo di rendering audio predefinito può comunque essere creato senza enumerazione.
-   [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) dispone di una funzione aggiuntiva [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) per che restituisce la maschera del canale per il dispositivo di output di destinazione.
-   Le librerie [X3DAudio](x3daudio.md) e [XAPOFX](xapofx-overview.md) vengono unite in XAudio2. Il codice dell'app usa ancora intestazioni separate, X3DAUDIO. H e XPOFX. H, ma ora si collega a una singola libreria di importazione, XAUDIO2 \_ 8. lib.
-   il supporto per xWMA non è disponibile in questa versione di XAudio2; xWMA non sarà supportato come formato di buffer audio durante la chiamata di CreateSourceVoice. È ora consigliabile usare l'oggetto lettore di origine Media Foundation per la decodifica di un'ampia varietà di formati multimediali in buffer PCM in memoria.
-   [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) ora accetta quattro parametri anziché due. I parametri più recenti specificano i dati iniziali come parte della creazione di [XAPOFX](xapofx-overview.md) .

## <a name="xaudio-27-and-earlier-windows-7"></a>XAudio 2,7 e versioni precedenti (Windows 7)

Tutte le versioni precedenti di XAudio2 per l'uso nelle app sono state fornite come DLL ridistribuibili in DirectX SDK. La prima versione di XAudio2, XAudio2 2,0, è stata fornita nella versione di marzo 2008 di DirectX SDK. L'ultima versione da distribuire in DirectX SDK è XAudio2 2,7, disponibile nell'ultima versione di DirectX SDK nel giugno 2010.

Legacy DirectX SDK non è più disponibile nei download Microsoft a causa del ritiro di tutti i contenuti con firma SHA-1. Il 2010 giugno è stato il rilascio di fine vita.

Le versioni precedenti di XAudio2 non possono essere usate per compilare app di Windows Store per Windows 8.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> <dt>

[Concetti chiave di XAudio2](xaudio2-key-concepts.md)
</dt> </dl>

[Guida per gli sviluppatori per la versione ridistribuibile di XAudio 2,9](xaudio2-redistributable.md)
</dt> </dl>
 

 
