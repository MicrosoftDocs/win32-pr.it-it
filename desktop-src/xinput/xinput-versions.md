---
title: Versioni di XInput
description: XInput è un'API multipiattaforma che è stata fornita per l'uso in Xbox e Windows.
ms.assetid: e89a6c81-f170-4385-f942-3606f9747244
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3d3624b8ea12872058ed1d874aa242a5806aec2
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "103885926"
---
# <a name="xinput-versions"></a>Versioni di XInput

XInput è un'API multipiattaforma che è stata fornita per l'uso in Xbox e Windows. In Xbox XInput viene fornito come una libreria statica compilata nell'eseguibile del gioco principale. In Windows, XInput viene fornito come una DLL installata nelle cartelle di sistema del sistema operativo.

Attualmente sono disponibili tre versioni correnti della DLL XInput. Scegliere la versione appropriata di XInput in base alle funzionalità di XInput in uso e alle versioni di Windows che si intende supportare.

- XInput 1,4: XInput 1,4 viene fornito come parte di Windows 10. Usare questa versione per la compilazione di app UWP.
- XInput 9.1.0: XInput 9.1.0 è incluso in Windows Vista, Windows 7 e Windows 8. Usare questa versione se l'applicazione desktop è progettata per l'esecuzione in queste versioni di Windows e si usa la funzionalità XInput di base.
- XInput 1,3: XInput 1,3 viene fornito come componente ridistribuibile in DirectX SDK con supporto per Windows Vista, Windows 7 e Windows 8. Usare questa versione se l'app desktop è progettata per l'esecuzione in queste versioni di Windows ed è necessaria una funzionalità non supportata da XInput 9.1.0.

## <a name="xinput-14"></a>XInput 1,4

XInput 1,4 viene attualmente fornito come componente di sistema in Windows 8 come XINPUT1 \_4.DLL. È disponibile "posta in arrivo" e non richiede la ridistribuzione con un'applicazione. Windows Software Development Kit (SDK) contiene l'intestazione e la libreria di importazione per il collegamento statico a XINPUT1 \_4.DLL. Per scaricare Windows 8 SDK, vedere [download per lo sviluppo di applicazioni desktop](https://developer.microsoft.com/windows/downloads/).

XInput 1,4 presenta questi vantaggi principali rispetto ad altre versioni di XInput:

-   Questa è l'unica versione che può essere usata nelle app di Windows Store C++/DirectX.
-   La nuova funzione [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) fornisce una stringa di ID dispositivo audio che è possibile usare per aprire una voce di XAudio2 mastering o un dispositivo audio per una cuffia collegata a un controller comune di Xbox. La funzione [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) non è disponibile in questa versione.
-   Offre funzionalità migliorate per la creazione di report, tra cui XINPUT \_ Caps \_ wireless, XINPUT \_ Caps \_ FFB \_ supportati, XINPUT \_ Caps \_ PMD \_ supportati e XINPUT \_ Caps \_ senza \_ flag di navigazione e report più accurati di XINPUT \_ Caps \_ Voice \_ supportati. Questi flag vengono combinati nel membro **Flags** della struttura delle [**\_ funzionalità XINPUT**](/windows/desktop/api/XInput/ns-xinput-xinput_capabilities) . La funzione [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) restituisce **le \_ funzionalità di XINPUT**.

### <a name="xinput-910"></a>9.1.0 XInput

Analogamente a XInput 1,4, XInput 9.1.0 viene fornito oggi come componente di sistema in Windows 10, Windows 8. x, Windows 7 e Windows Vista come XINPUT9 \_ 1 \_0.DLL. Viene gestita principalmente per garantire la compatibilità con le applicazioni esistenti. Il set di funzioni è ridotto, quindi è consigliabile usare XInput 1,4, se possibile. Tuttavia, è utile usare per le applicazioni che devono essere eseguite nelle versioni di livello inferiore di Windows, ma non sono necessarie le funzionalità audio aggiuntive fornite da XInput 1,4 o XInput 1,3.

Il Windows SDK contiene l'intestazione e la libreria di importazione per il collegamento statico a XINPUT9 \_ 1 \_0.DLL.

XInput 9.1.0 presenta questi svantaggi rispetto ad altre versioni di XInput:

-   Per motivi di compatibilità con le versioni precedenti, [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) in questa versione di XInput restituisce informazioni sulle funzionalità fisse. Indipendentemente dal dispositivo controller comune Xbox collegato, **XInputGetCapabilities** in XInput 9.1.0 segnalerà sempre un sottotipo di dispositivo del gamepad. Non restituisce il \_ \_ bit della funzionalità wireless XINPUT Caps anche se è connesso un dispositivo wireless.
-   Non è possibile determinare la cuffia per un ID utente specificato. La funzione [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) non è disponibile e la funzione [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) non restituisce alcun risultato in Windows 8. x o Windows 10.
-   Le funzioni [**XInputEnable**](/windows/desktop/api/XInput/nf-xinput-xinputenable), [**XInputGetBatteryInformation**](/windows/desktop/api/XInput/nf-xinput-xinputgetbatteryinformation)e [**XInputGetKeystroke**](/windows/desktop/api/XInput/nf-xinput-xinputgetkeystroke) non sono disponibili.

### <a name="xinput-13"></a>XInput 1,3

Alcune versioni precedenti di XInput sono state fornite come DLL ridistribuibili in DirectX SDK. La prima versione ridistribuibile di XInput, XInput 1,1, è stata inclusa nella versione aprile 2006 di DirectX SDK. L'ultima versione da distribuire in DirectX SDK è XInput 1,3, disponibile nella versione di giugno 2010 del Legacy DirectX SDK. *DirectX SDK non è più disponibile nei download Microsoft*.

È possibile usare XInput 1,3 per le applicazioni che supportano le versioni di livello inferiore di Windows e richiedono la funzionalità non fornita da XInput 9.1.0, ovvero la creazione di report di sottotipi corretti, il supporto audio, il supporto esplicito per la creazione di report della batteria e così via.
